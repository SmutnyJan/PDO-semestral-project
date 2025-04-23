# Papírová letadla
Tento scénář ověřuje funkčnost pohybu papírových vlaštovek, jejich interakci s hráčem a reakci na zásah předmětem Propiska.

## Herní stav:
```json
{
    "SpawnScene": 11,
    "GameState": 1,
    "Money": 48,
    "Items": [
        {
            "ItemType": 0,
            "Amount": 50
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
            "x": 259.5791015625,
            "y": -0.8139311075210571,
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
        "MoneyRevert": 48
    }
}
```

## Popis testovacího scénáře
1. Po spuštění hry zvolte v hlavním menu možnost *Načíst hru*, čímž se načte připravený herní stav.
2. Načte se první level (na budově G). V inventáři se nachází 50 kusů předmětu *Kreslířův pomocník* (inventář lze otevřít klávesou *Tab*).
3. V inventáři klikněte na ikonu propisky, čímž se předmět nastaví jako aktivní.
4. Inventář zavřete stisknutím tlačítka *Zavřít* nebo opětovným stisknutím klávesy *Tab*.
5. Stisknutím klávesy *E* předmět použijte – postava hodí propisku směrem před sebe.
6. Pokračujte v levelu směrem doprava, dokud nenarazíte na papírová letadla.
7. Na libovolné **jedno** letadlo hoďte propisku. Pokud se trefíte, letadlo zmizí a na jeho místě se objeví předmět s herní měnou, který lze sebrat.
8. Po jeho sebrání se aktualizuje ukazatel peněz (vpravo nahoře).
9. Následně přistupte k libovolnému ze zbývajících letadel a nechte ho, aby se vás dotklo.
10. Po kontaktu s letadlem se vaše postava objeví na posledním aktivovaném kontrolním bodě (stejné, jako když spadnete z plošiny).