# ClimatePlots DaysOver: Heiße Tage pro gewähltem Standort

ClimatePlots DaysOver generiert "Heiße Tage" für einzelne, frei wählbare Wetter-Stationen.  
Quelle Daten: [MeteoStat](https://meteostat.net/de).

Vorschau auf ein mögliches Ergebnis:

<img width="1000px" height="1000px" alt="Grafik mit exponentiell Wachsenden Kurven der Tage pro Jahr mit Temperaturen über 30, 31, 32, 33, 34 und 35°C. Start 1900 bis 2025." src="/media/wetter_trend_special_alle_schwellwerte.png" />



## Wie nutzen?

### [ 0 ] Acount via MeteoStat anlegen

Vorbereiten: 

- kostenlosen Basic-Account auf RapidAPI erstellen.
- API-Key erzeugen: https://dev.meteostat.net/api
- RapidAPIKey in `getData.py` anpassen

---

### [ 1 ] Daten holen

#### Daten einer konkreten, offiziellen Wetter-Station

Wenn Daten einer konkreten offiziellen Wetter-Station verwendet werden sollen:

Nummer der Station auf [meteostat.net/de](https://meteostat.net/de/) herausfinden und
in `getData.py` eintragen:
- URL: `https://meteostat.p.rapidapi.com/stations/daily`  
- Query-String: Stationsnummer  

#### Daten eines beliebigen geografischen Orts und umliegende Wetter-Stationen interpolieren

Wenn stattdessen Daten verwendet werden sollen, die für einen beliebigen geografischen Ort aus den umliegenden Wetter-Stationen interpoliert werden, folgendes in `getData.py` eintragen:
- URL: `https://meteostat.p.rapidapi.com/point/daily`
- Query-String: Geolocation des Orts

---

### [ 2 ] Gewünschte Einstellungen für Ergebnis-Plot

Einstellungen in `days_over.py` anpassen  

---

### [ 3 ] Scripte ausführen

1. getData.py  
2. mergeData.py  
3. days_over.py 


## Lizenz

Bitte ergänzen  
