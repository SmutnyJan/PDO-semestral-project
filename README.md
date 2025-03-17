# Návod k testování TULtimátní hry

## Inicializace hry a otevření složky s logy a savy
### Inicializace hry
**Rozsah:** 0.5 strany  
- Stažení zipu z Google Disku (zip obsahuje vybuilděnou hru v `.exe` a složku s herními savy a presety nastavení v podobě souborů JSON pro jednodušší a přesnější testování)
- Spuštění hry pro prvotní ověření funkčnosti  

### Otevření složky s logy a savy
- Otevření cesty `dataPersistentPath`, ověření, že uživatel vidí soubory JSON  

## Technicko-herní wiki
**Rozsah:** 5-6 strany  
Popis všech herních aspektů ze strany technické funkcionality.

### Prvotní testování hry
- Tester by měl projít hru sám, bez jakéhokoliv návodu/pomoci
- Zhodnocení herního zážitku, smysluplnosti příběhu a intuitivnosti herních funkcí  

### Technické aspekty hry
- **Herní flow z pohledu scén**  
  - Jaká scéna se načte jako první?
  - Do jaké scény se načtu, když vejdu sem a sem?
  - V jaké scéně se odehrává finální cutscéna?
- **Save system a formát souborů JSON**  
  - Co znamenají konkrétní atributy v souboru `settings.json`?
  - Kdy se načítá obsah souborů?
  - Kdy se do souborů ukládá?
  - Jak vypadá mapování scén a předmětů na čísla?
  - Jak se ukládá herní postup v rámci levelu?
- **Herní předměty**  
  - Za jak dlouho se vypne efekt zvýšení rychlosti?
- **Herní inventář**  
  - Co se stane, když použiji předmět a hned si ho „odvybavím“?
- **Herní nastavení**  
  - Co se má stát, když zapnu VSync?
  - Jak si zvolím sběr zvuku z jiného mikrofonu?
  - Kdy se nastavení uloží (tlačítko „Zpět“ bez stisknutí tlačítka „Uložit“ nastavení obnoví do původní podoby)?
- **Měnění ročního období**  
  - Jaké všechny věci mění (collidery, fyzické vlastnosti)?
  - Kdy se provede?
- …  

## Ustanovení použitých pojmů v testovacích scénářích
**Rozsah:** maximálně 1 strana  
Vysvětlení pojmů:
- **Vytvořit novou hru** - spustit hru a kliknout na tlačítko „Nová hra“
- **Načíst hru** - spustit hru a kliknout na tlačítko „Načíst“
- **Udělat nový save** - Smazat všechny soubory JSON (soubor s nastavením se při spuštění nové hry nemaže)
- **Načíst save -název savu-** - nahrání obsahu uvedeného souboru JSON do specifikovaného save souboru  
  - `Načti save settingsA.json do settings.json`
  - `Načti save final_level.json do progress.json`
- **Shodit hru** - vypnout hru jinak než přes herní UI (Správce úloh, ALT + F4, vypnutí PC, BSOD atd.)
- **Jít do levelu -jméno levelu-** - dojít na místo, které způsobí načtení daného levelu  

## Kategorizace bugů dle závažnosti
**Rozsah:** 0.5 strany  
### Neintuitivní chování
- Nejedná se o bug, ale chování je neočekávané
- **Příklady:**
  - Hráč by nečekal, že když v testu nezaškrtne žádné políčko a dá „Odeslat“, tak se test odešle
  - Cutscény lze přeskočit i pomocí kláves `E` nebo `NUM ENTER`

### Lehký bug
- Hráč může pokračovat ve hře, ale bug lehce narušuje hratelnost
- **Příklady:**
  - Hráč se krátce zasekne v textuře
  - Tlačítko reaguje až na druhé kliknutí

### Těžký bug
- Hráči nedovoluje pokračovat, narušuje hratelnost, ale hra stále běží
- **Příklady:**
  - Hráč se nemůže dostat z levelu
  - Tlačítko nereaguje na stisknutí
  - Hráč může používat neomezené množství itemů
  - Hra se neukládá
  - Přestala hrát hudba

### Kritická chyba
- Hra spadne
- **Příklady:**
  - Hráč použije item a hra spadne
  - Hráč klikne na tlačítko a hra spadne

## Odeslání zprávy o bugu pomocí Google Forms/GitHub Issues
**Rozsah:** 1-2 strany  

### Google Forms
- **Poskytnout URL**
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

### GitHub Issues
- **Poskytnout URL**
- **Sjednocený styl zprávy u bugu**

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
