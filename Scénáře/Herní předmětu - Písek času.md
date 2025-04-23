# Herní předmět - Písek času
Scénář ověřuje funkčnost předmětu Písek času, který lze použít v libovolném levelu.

## Herní stav:
```json
{
    "SpawnScene": 11,
    "GameState": 1,
    "Money": 99,
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
            "Amount": 100
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
            "x": -30.549999237060548,
            "y": 5.28000020980835,
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
                "Amount": 100
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
        "MoneyRevert": 99
    }
}
```

## Popis testovacího scénáře
1. Po spuštění hry zvolte v hlavním menu možnost *Načíst hru*, čímž se načte připravený herní stav.

2. Načte se scéna s levelem v budově G. Pomocí klávesy *Tab* si zobrazte inventář.
3. V inventáři se 100 kusů předmětu „*Písek času*“.
4. Klikněte na jeho ikonu (přesýpací hodiny) a zavřete inventář pomocí klávesy *Tab* nebo tlačítkem *Zavřít*.
5. Ve scéně se objeví oranžová tečka, která reprezentuje hráčovu pozici před pěti vteřinami.
6. *Písek času* dokáže hráče vrátit na pozici, na které se nacházel před pěti vteřinami (na pozici tečky).
7. Předmět vyzkoušejte. Pomocí WASD nebo pomocí šipek pokračujte v levelu směrem doleva.
8. V libovolné vhodné chvíli předmět aktivujte klávesou *E*. Vhodná situace může být například tehdy, když se vám nepodaří doskočit na plošinu a začnete padat.
9. Po stisknutí klávesy *E* se hráč vrátí na pozici tečky.