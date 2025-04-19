# Pohyb a navigace k budově G
Scénář ověřuje funkčnost pohybu v lobby, navigace a přechodu mezi scénami v herním lobby.
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
4. Nad hráčem je černá šipka, která hráči ukazuje, kam má jít (v tomto herním stavu hráče vede ke dveřím budovy G).
5. Šipka má dva vnitřní stavy:
    - Pokud se hráč nachází ve stejné scéně, jako dveře do budovy, do které má hráč jít, šipka ukazuje právě na tyto dveře.
    - Pokud se hráč nenachází ve stejné scéně, šipka ukazuje na východ z aktuální scény a vede hráče do scény, ve které se dveře nacházejí (v tomto případě vede šipka hráče do scény, kde je budova G)
6. Šipka nyní míří do levého dolního rohu.
7. Běžte ke dveřím menzy (budova před hráčem).
8. Z pohledu příběhu má menza ještě zavřeno, takže se nic nestane.
9. Jděte podle navigační šipky do levého dolního rohu scény (vchod do scény, ve které je budova G).
10. Šipka ukazuje na dveře do budovy G.
11. Jděte ke dveřím budovy G. Načte se herní level.
