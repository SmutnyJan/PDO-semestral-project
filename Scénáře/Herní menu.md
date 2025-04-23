# Herní menu
Scénář ověřuje funkčnost herního menu (menu v levelu), správného ukládání postupu jakožto i jeho korektní mazání.
## Herní stav:
```json
{
    "SpawnScene": 4,
    "GameState": 1,
    "Money": 0,
    "Items": [
        {
            "ItemType": 0,
            "Amount": 5
        },
        {
            "ItemType": 1,
            "Amount": 1
        },
        {
            "ItemType": 2,
            "Amount": 1
        },
        {
            "ItemType": 3,
            "Amount": 2
        },
        {
            "ItemType": 4,
            "Amount": 2
        },
        {
            "ItemType": 5,
            "Amount": 2
        }
    ],
    "LevelConfig": {
        "Scene": 0,
        "SpawnPoint": {
            "x": 0.0,
            "y": 0.0,
            "z": 0.0
        },
        "ChestsOpenedIndexes": [],
        "PlanesDestroyedIndexes": [],
        "ItemsRevert": [],
        "MoneyRevert": 0
    }
}
```

## Popis testovacího scénáře
1. Po spuštění hry zvolte v hlavním menu možnost *Načíst hru*, čímž se načte připravený herní stav.

2. Načte se scéna, ve které stojí hráč před Menzou.
3. Pohybovat se lze pomocí kláves WSAD nebo pomocí šipek.
4. Nad hráčem je černá šipka, která hráči ukazuje, kam má jít (v tomto herním stavu hráče vede ke dveřím budovy G).
5. Následujte šipku až do budovy G.
6. Po vstupu do budovy se načte level s budovou G.
7. Vlevo dole se ukáže dialog, který hráči vysvětluje používání předmětů a základy pohybu.
8. Zmáčkněte *Tab* a klikněte na ikonu propisky. Menu zavřete (pomocí tlačítka *Zavřít* nebo pomocí opětovného stisknutí *Tab*).
9. Stiskněte opakovaně klávesu *E*, dokud z levého dolního rohu nezmizí ikona propisky (tím spotřebujete všechny propisky).
10. Proskákejte k dalšímu kontrolnímu bodu (pokračujte pořád doprava).
11. Po dosažení dalšího kontrolního bodu se opět ukáže dialog, který vysvětluje, jak lze získat peníze a předměty. Dále přestavuje pohyblivé plošiny.
12. Po stisknutí klávesy *Escape* se objeví menu.
13. Menu nabízí tyto položky:
    - *Restart levelu*,
    - *Zpět do lobby*,
    - *Zpět do menu*,
    - *Zavřít*.
14. Stiskněte klávesu *Escape*. Menu se zavře.
15. Opět menu otevřete pomocí klávesy *Escape*.
16. Stiskněte možnost *Restart levelu*.
17. Objevíte se opět na začátku levelu a máte opět plný počet propisek (5 kusů). Inventář otevřete klávesou *Tab*.
18. Opět přeskákejte k druhému kontrolnímu bodu.
19. Přibližte se k truhle vpravo od kontrolního bodu. Z truhly začnou vypadávat věci.
20. Věci, které vypadly z truhly, lze po několika sekundách sebrat (seberte je).
21. Po sebrání se zvýší počet příslušných předmětů (každý o +1) a hodnota peněz (o +1).
22. Pokračujte k dalšímu kontrolnímu bodu.
23. Po projití kontrolním bodem si prohlédněte obsah inventáře a stav peněz (případně si tento stav zapište).
24. Opět vyvolejte menu pomocí klávesy *Escape*.
25. V menu zvolte možnost *Zpět do lobby*.
26. V hlavním menu zvolte možnost *Načíst hru*.
27. Objevíte se opět na budově G, stav inventáře a peněz se musí shodovat s tím, který jste si zapsali po kroku 23.
