# Menza
Scénář ověřuje funkčnost obchodu s předměty - jejich nákup a přidávání do inventáře.

## Herní stav:
```json
{
    "SpawnScene": 3,
    "GameState": 3,
    "Money": 999,
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
        "Scene": 11,
        "SpawnPoint": {
            "x": 354.92999267578127,
            "y": 5.001999855041504,
            "z": 0.0
        },
        "ChestsOpenedIndexes": [],
        "PlanesDestroyedIndexes": [],
        "ItemsRevert": [
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
        "MoneyRevert": 999
    }
}
```

## Popis testovacího scénáře
1. Po spuštění hry zvolte v hlavním menu možnost *Načíst hru*, čímž se načte připravený herní stav.

2. Načte se scéna, ve které se nachází hráč před budovou G. Vložený herní stav popisuje situaci, kdy hráč dokončil level G a má za úkol dojít do menzy.
3. Pomocí kláves WASD nebo šipek se vydejte směrem, kterým ukazuje černá šipka nad hráčem – k vchodu do lobby scény před menzou.
4. Po načtení této scény pokračujte podle šipky ke vstupu do budovy menzy.
5. Po načtení scény s menzou zamiřte k prodejnímu pultu vpravo nahoře a postavte se před něj.
6. Zobrazí se menu představující nabídku obchodu a hráčův inventář.
7. Klikněte na libovolnou ikonu předmětu. V pravém panelu obchodu se zobrazí jeho název, popis a cena.
8. Klikněte na tlačítko Koupit v postranním panelu.
9. Počet kusů zvoleného předmětu v inventáři se zvýší o 1. Současně se sníží množství hráčovy herní měny o cenu daného předmětu.
