# Nastavení
Scénář ověřuje základní funkčnost nabídky nastavení. Kontroluje správnou odezvu a funkčnost všech ovládacích prvků, včetně změny hlasitosti, výběru aktivního mikrofonu, přepnutí do celoobrazového režimu, aktivace nebo deaktivace vertikální synchronizace a zobrazení ukazatele FPS. Zároveň ověřuje, zda se tyto změny korektně uloží a projeví v chování hry.


## Popis testovacího scénáře
1. Po spuštění hry zvolte v hlavním menu možnost *Nastavení*.

2. Nastavení nabízí následující položky:
    - *Režim celé obrazovky*,
    - *Ukazatel FPS*,
    - *V-Sync*,
    - *Hlasitost SFX*,
    - *Hlasitost hudby*,
    - *Použitý mikrofon*.
3. Na celou vykreslenou scénu je aplikovaný CRT filtr.
4. Klikněte na možnost *Zobrazit FPS*. Po kliknutí se zobrazí v pravém horním rohu číslo ukazující snímky za sekundu.
5. Posuňte kruh na posuvníku u hlasitosti zvukových efektů (SFX) do středu posuvníku.
6. Posuňte kruh na posuvníku u hlasitosti hudby do středu posuvníku.
7. Při změně posuvníhu hlasitosti hudby lze slyšet rozdíl v hlasitosti hudby, která v nastavení hraje. 
8. V rozklikávací nabídce u možnosti *Použitý mikrofon* jsou vypsány všechny dostupné mikrofony.
9. Po kliknutí na *Uložit* se ozve zvuk potvrzení a zobrazí se hlavní menu.
10. Opět zvolte možnost *Nastavení* a posuvník u hudby posuňte úplně doleva.
11. Hudba nejde vůbec slyšet.
12. Klikněte na tlačítko *Zpět*.
13. Nastavení se neuložilo a hudba jde tím pádem opět slyšet.
14. Pro potvrzení přejděte opět do nastavení.
15. Posuvník ukazující hlasitost hudby je ve stavu, který odpovídá aktuální hlasitosti (nezůstal úplně vlevo).
