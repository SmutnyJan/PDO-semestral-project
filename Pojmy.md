# Ustanovení použitých pojmů v testovacích scénářích

- **Save** - Soubor JSON, který v sobě uchovává informace o nastavení (hlasitost zvuků a hudby, zobrazení FPS, ...) a o herním postupu (stav inventáře, naposledný uložený kontrolní bod)
- **Vytvořit novou hru** - Spustit hru a kliknout na tlačítko „Nová hra“.
- **Načíst hru** - Spustit hru a kliknout na tlačítko „Načíst“.
- **Udělat nový save** - Smazat oba soubory JSON (*progress.json*, *settings.json*)
- **Načíst save/nastavení -název savu-** - Nahrání obsahu uvedeného souboru JSON do *progress.json* (v případě načtení savu) nebo do *settings.json* (v případě načtení nastavení).
  - `Načti nastavení invalid_microphone.json`.
  - `Načti save final_level.json`.
- **Shodit hru** - vypnout hru jinak, než přes herní UI (Správce úloh, ALT + F4, vypnutí PC, BSOD atd.)
- **Jít do levelu -jméno levelu-** - Dojít na místo, které způsobí načtení daného levelu.