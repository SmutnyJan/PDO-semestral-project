# Lobby menu
Scénář ověřuje funkčnost všech tlačítek v menu, které lze zobrazit v lobby.
## Herní stav:
```json
{
    "SpawnScene": 4,
    "GameState": 1,
    "Money": 1000,
    "Items": [
        {
            "ItemType": 0,
            "Amount": 5
        },
        {
            "ItemType": 1,
            "Amount": 50
        },
        {
            "ItemType": 2,
            "Amount": 10
        },
        {
            "ItemType": 3,
            "Amount": 10
        },
        {
            "ItemType": 4,
            "Amount": 10
        },
        {
            "ItemType": 5,
            "Amount": 10
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
4. Zmáčknutím klávesy *Escape* vyvolejte menu.
5. Menu nabízí tyto položky:
    - *Zpět do menu*,
    - *Zavřít*.
6. Klikněte na možnost *Zavřít*. Menu zmizí.
7. Opět stiskněte klávesu *Escape*. Menu se opět objeví.
8. Opět stiskněte klávesu *Escape*. Menu opět zmizí.
9. Opět stiskněte klávesu *Escape*.
10. Klikněte na *Zpět do menu*.
11. Načte se hlavní menu.
12. V hlavním menu zvolte možnost *Načíst hru*.
13. Načetla se lobby scéna, ve které je hráč před menzou.
14. Z lokace před menzou jděte po cestě doleva, dokud se nenačte scéna s budovou G. Černá šipka ukazuje směr.
15. Ve scéně s budovou G opět vyvolejte menu.
16. Zvolte možnost *Zpět do menu*.
17. V hlavním menu zvolte opět možnost *Načíst hru*.
18. Načte se scéna, ve které je hráč opět před menzou.

