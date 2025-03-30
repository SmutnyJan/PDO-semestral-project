# TULtimární hra - příručka pro testery

## Jak začít?
### Minimální systémové požadavky pro testování
- Operační systém: Windows 10
- Procesor: Intel Core i5-8350U, AMD Ryzen 5 2500U
- Operační paměť: 4 GB
- Grafická karta: NVIDIA GeForce MX110, AMD Radeon 530
- Volné místo na disku: 165 MB


### Spuštění hry
1. Z [GitHub repozitáře](https://github.com/SmutnyJan/BP-Unity-Smutny/tree/release) si stáhněte kopii ve formátu ZIP.
> ⚠️ **Upozornění:** Ujistěte se, že se nacházíte na větvi „release“, která obsahuje aktuální plnou verzi hry.
![Github větev release](images/github_release.png)
2. Soubor ZIP vybalte do libovolného adresáře (například „Plocha“ pro snadný přístup).
3. Ve vybalené složce se nachází složka *BP-UnityGame*, soubor *avg_fps.py* a složka *Build*. Ve složce *Build* je soubor *TULtimátní hra.exe*, což je spustitelná hra.
4. Spusťte soubor *TULtimátní hra.exe*. Zobrazí se hlavní menu a díky prvotnímu spuštění se vygenerují i debug logy. Hru nyní vypnětě.


### Otevření složky s debug logy a herními savy
K pohodlnému testování je potřeba otevřít ještě složku, ve které se nachází debug logy (jsou součástí zprávy o herní chybě a o úspěšném testování) a herní savy (představují fázi hry, ve které se hráč nachází), které se budou u jednotlivých testovacích scénářů měnit na předdefinované hodnoty pro rychlejší testování.

Tuto složku lze najít na *C:\\{jméno uživatele}\smutn\AppData\LocalLow\FM TUL Smutny Strecanska\TULtimátní hra*.
1. Pro zobrazení složky s herními savy nejprve otevřete složku *AppData* (nejsnadnější způsob je vyhledat „%AppData%“ pomocí vyhledávání Windows 10/11).
2. Ve složce *AppData* vyberte *LocalLow*, dále *FM TUL Smutny Strecanska* a *TULtimátní hra*. Tato složka obsahuje soubory *Player.log*, *progress.json*, *settings.json* (za předpokladu, že hra byla alespoň jednou zapnuta).
> ⚠️ **Upozornění:** Po potvrzení volby „%AppData%“ ve vyhledávači se otevře složka *Roaming*, která je potomkem složky *AppData*. Je tedy potřeba „jít“ o jednu složkovou úroveň výše.


## Ustanovení použitých pojmů v testovacích scénářích
V popisu jednotlivých testovacích scénářů jsou použita různá slova a slovní spojení, která by mohla působit nejasně či nejednoznačně. Využití těchto pojmů ale značně zmenšuje robustnost celého návodu.
Vysvětlení pojmů:
- **Vytvořit novou hru** - Spustit hru a kliknout na tlačítko „Nová hra“.
- **Načíst hru** - Spustit hru a kliknout na tlačítko „Načíst“.
- **Udělat nový save** - Smazat oba soubory JSON (*progress.json*, *settings.json*)
- **Načíst save/nastavení -název savu-** - Nahrání obsahu uvedeného souboru JSON do *progress.json* (v případě načtení savu) nebo do *settings.json* (v případě načtení nastavení).
  - `Načti nastavení invalid_microphone.json`.
  - `Načti save final_level.json`.
- **Shodit hru** - vypnout hru jinak, než přes herní UI (Správce úloh, ALT + F4, vypnutí PC, BSOD atd.)
- **Jít do levelu -jméno levelu-** - Dojít na místo, které způsobí načtení daného levelu.

## Kategorizace bugů dle závažnosti
### Neintuitivní chování
- Nejedná se o bug, ale chování je neočekávané.
- **Příklady:**
  - Hráč by nečekal, že když v testu nezaškrtne žádné políčko a dá „Odeslat“, tak se test odešle.
  - Cutscény lze přeskočit i pomocí kláves `E` nebo `NUM ENTER`.
  - Po použití všech kusů daného předmětu předmět z inventáře zmizí.

### Lehký bug
- Hráč může pokračovat ve hře, ale bug lehce narušuje hratelnost.
- **Příklady:**
  - Hráč se krátce zasekne v textuře.
  - Tlačítko reaguje až na druhé kliknutí.
  - Hráč se nemůže hýbat, pokud ale vyskočí, hybat se může.

### Těžký bug
- Hráč nemůže pokračovat, narušuje hratelnost, ale hra stále běží (nespadla).
- **Příklady:**
  - Hráč se nemůže dostat z levelu.
  - Tlačítko nereaguje na stisknutí.
  - Hráč může používat neomezené množství itemů.
  - Hra se neukládá.
  - Přestala hrát hudba.

### Kritická chyba
- Hra spadne
- **Příklady:**
  - Hráč použije item a hra spadne.
  - Hráč klikne na tlačítko a hra spadne.

## Zprávy o chybách a o úspěšném testování
Informace o testování a nalezených chybách mi prosím posílejte pomocí formulářů Google, jejichž struktura je následující:

### Protokol o úspěchu testovacího scénáře
Formulář [zde](https://forms.gle/h2ScRxJ8PcTQHiRw8).
- **Kolonky:**
  - Název testera
  - Hardware (CPU, GPU, RAM)
  - Datum
  - Číslo verze
  - Závažnost bugu
  - Popis bugu (co je špatně)
  - Očekávané chování
  - Jak bug vyvolat
  - Přílohy (obrázek, video)

### Protokol o chybě
Formulář [zde](https://forms.gle/y7WAztFuzfxBB5s16).
- **Kolonky:**
  - Název testera
  - Hardware (CPU, GPU, RAM)
  - Datum
  - Číslo verze
  - Závažnost bugu
  - Popis bugu (co je špatně)
  - Očekávané chování
  - Jak bug vyvolat
  - Přílohy (obrázek, video)  


## Testovací scénáře
**Rozsah:** minimálně 4 strany  
Popis jednotlivých scénářů, využití pojmů z kapitoly o pojmech.

### Struktura scénáře
- **Podrobný popis toho, co udělat** (kliknout sem, jít tam, použít tohle, nahrát tento save atd.)
- **Očekávané chování**

### Příklady scénářů
- **Odeslání FPS logu** (testování výkonu)
  - Jak spustit v nastavení zobrazovač FPS a logger
  - Co vyplnit do zprávy o bugu
- **Testování itemu „Perla“**
  - Načíst `progress.json`, kde má hráč perlu 1000×
  - Zkoušet perlu házet na různá místa
- **Testování přehlcení skrz použití itemu**
  - Rychlé volání funkce `UseItem()` opětovným mačkáním klávesy

… *(další scénáře dle potřeby)*
