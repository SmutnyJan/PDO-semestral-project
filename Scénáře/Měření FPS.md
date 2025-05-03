# Měření FPS
Tento scénář slouží k měření výkonu hry v různých částech – v hlavním menu, v nastavení a přímo ve hře. Hodnoty FPS se automaticky zaznamenávají do logu, který bude následně použit k analýze průměrné snímkové frekvence.
Cílem testu je získat představu o náročnosti hry na běžném hardwaru. Je důležité během testu nijak nerušit běh hry (nepřepínat okna, nemačkat klávesy), aby byly výsledky co nejpřesnější.
## Herní stav:
```json
{
    "SpawnScene": 0,
    "GameState": 0,
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
        "ItemsRevert": []
    }
}
```

## Popis testovacího scénáře
> ⚠️ **Upozornění:** Pokud hru testujete na notebooku, mějte ho, prosím, připojený k napájení. Alternativně se ujistěte, že nemáte v rámci úspory baterie omezený výkon.
1. Po spuštění hry přejděte do nastavení a zaškrtněte „Ukazatel FPS“ a „Režim celé obrazovky“. Po zaškrtnutí se ukáže v levém horním rohu hodnota FPS. Klikněte na tlačítko „Uložit“.

2. Po zapnutí logování FPS hru vypněte (ať už v hlavním menu nebo pomocí *ALT + F4*), aby se resetovaly logy.
3. Hru zapněte.
> ⚠️ **Varování:** Během sběru hodnot FPS ze hry „nepřeklikávejte“ ani nepoužívejte zkratky ALT + TAB. Narušilo by to integritu testování.
4. Po spuštění hry zůstaňte 10 vteřin v hlavním menu, poté přejděte do nastavení a počkejte zde stejně dlouhou dobu (**nevypínejte ukazatel FPS ani nezapínejte VSync**).

    Poté v hlavní nabídce klikněte na *Nová hra*. Spustí se cutscény, které lze přeskočit klávesou *Escape* a test, který libovolně vyplňte. Poté se objevíte v lobby. Pomocí kláves WSAD se přesuňte po cestě k levému kraji scény (černá šipka ukazuje směr). Po dosažení levého okraje se objevíte u druhé budovy. Vkročte do dveří, na které ukazuje šipka.
5. Po vkročení do dveří budovy G se objevíte v herním levelu. Zde zůstaňte 30 vteřin. S hrou nijak neinteragujte (nemačkejte žádné klávesy).
6. Po uplynutí této doby se pomocí klávesy *Escape* a tlačítka *Zpět do menu* vraťte do hlavního menu.
7. Hru vypněte pomocí tlačítka „Ukončit hru“, čímž zapíšete hodnoty FPS do logů.