# Změna ročního období
Scénář ověřuje funkčnost změny vizuálního stylu platforem podle aktuálního ročního období, aktivaci fullscreen shaderu pro námrazu a particle efektu pro padání listí a sněhových vloček

> ⚠️ **Upozornění**: K provedení tohoto testu musíte mít připojený mikrofon.



## Herní stav:
```json
{
    "SpawnScene": 11,
    "GameState": 1,
    "Money": 9,
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
            "x": 28.969999313354493,
            "y": 3.986999988555908,
            "z": 0.0
        },
        "ChestsOpenedIndexes": [],
        "PlanesDestroyedIndexes": [
            0
        ],
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
        "MoneyRevert": 9
    }
}
```

## Popis testovacího scénáře
1. Po spuštění hry přejděte do nastavení a ujistěte se, že máte zvolený správný mikrofon (ten, který budete pro testování používat).

2. Vraťte se zpět do hlavního menu (nezapomeňte nastavení uložit) a zvolte možnost *Načíst hru*, čímž se načte připravený herní stav.
3. Načte se scéna, ve které se hráč nachází u jednoho z kontrolních bodů levelu G. Výchozím ročním obdobím je jaro.
4. Vydejte do mikrofonu hlasitý zvuk a sledujte změnu ročního období (změní se vzhled plošin).
5. Počkejte 15 vteřin a vydejte další hlasitý zvuk.
6. Roční období se přepne na podzim (listopad) – obrazovkou budou padat oranžové listy s čistě vizuálním efektem.
7. Vydejte ještě jeden hlasitý zvuk a sledujte přepnutí na zimu – začne padat sníh a kolem obrazovky se objeví námraza. I tyto efekty jsou pouze vizuální.
