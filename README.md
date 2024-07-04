[[DE]](README.md)/[[EN]](README_en.md)

# Tagesschau API

Die Tagesschau ist eine Nachrichtensendung der ARD (Abkürzung für Arbeitsgemeinschaft der öffentlich-rechtlichen Rundfunkanstalten der Bundesrepublik Deutschland), die von ARD-aktuell in Hamburg produziert und mehrmals täglich ausgestrahlt wird. ARD-aktuell ist seit 1977 die zentrale Fernsehnachrichtenredaktion der ARD, bei welcher es sich wiederum um einen Rundfunkverbund handelt, der aus den Landesrundfunkanstalten und der Deutschen Welle besteht. 

Über die hier dokumentierte API stehen auf [www.tagesschau.de](https://www.tagesschau.de) aktuelle Nachrichten und Medienbeiträge im JSON-Format zur Verfügung.

**ACHTUNG:** Die Nutzung der Inhalte für den privaten, nicht-kommerziellen Gebrauch ist gestattet, die Veröffentlichung hingegen nicht - mit Ausnahme von Angeboten, die explizit unter der CC-Lizenz stehen (https://tagesschau.de/creativecommons). Es ist unzulässig, mehr als 60 Abrufe pro Stunde zu tätigen.


## Homepage

**URL:** https://www.tagesschau.de/api2u/homepage/

Ausgewählte Nachrichten und Eilmeldungen, die auf der Startseite der Tagesschau-App zu sehen sind.


## News

**URL:** https://www.tagesschau.de/api2u/news/

Aktuelle Nachrichten, die über GET-Parameter gefiltert werden können:

**Parameter:** *regions* 
- 1
- 2
- 3
- 4
- 5
- 6
- 7
- 8
- 9
- 10
- 11
- 12
- 13
- 14
- 15
- 16

Bundesland: 1=Baden-Württemberg, 2=Bayern, 3=Berlin, 4=Brandenburg, 5=Bremen, 6=Hamburg, 7=Hessen, 8=Mecklenburg-Vorpommern, 9=Niedersachsen, 10=Nordrhein-Westfalen, 11=Rheinland-Pfalz, 12=Saarland, 13=Sachsen, 14=Sachsen-Anhalt, 15=Schleswig-Holstein, 16=Thüringen. Mehrere Komma-getrennte Angaben möglich (z.B. regions=1,2).


**Parameters:** *ressort*

- inland
- ausland
- wirtschaft
- sport	
- video
- investigativ
- wissen

Ressort/Themengebiet


## Channels

**URL:** https://www.tagesschau.de/api2u/channels/

Aktuelle Kanäle (im Livestream: tagesschau24, tagesschau in 100 Sekunden, tagesschau, tagesschau 20 Uhr, tagesthemen, nachtmagazin, Bericht aus Berlin, tagesschau vor 20 Jahren, tagesschau mit Gebärdensprache)


## Search

**URL:** https://www.tagesschau.de/api2u/search/


**Parameter:** *searchText* 

Suchtext


**Parameter:** *resultPage* 

Seite


**Parameter:** *pageSize* 

Suchergebnisse pro Seite (1-30)


## Beispiel

```bash
tagesschau=$(curl -m 60 https://www.tagesschau.de/api2/homepage/)
```
