# Pretest Panel

Die Idee des Pretest Panel ist es, im Voraus Menschen für die Bewertung der Velorouten zu rekrutieren. Gleichzeitig sehen wir so auch, wie "biased" unsere Auswahl von Bewerter:innen sind bzw. sein werden. So können wir aktiv gegensteuern.

Siehe: https://index.velobserver.ch


## Variante 1

### Pretest Panel für die Bewertung der Velorouten
Um den VelObserver-Index von möglichst vielen verschiedenen Menschen testen lassen zu können, richten wir ein Pretest Panel ein, damit wir ein möglichst gutes Bild haben, wer unsere zukünftigen Tester:innen sind.        
        
Wir stellen Fragen zur:     
- Verkehrsmittelnutzung        
- Alter, Geschlecht, Ort         
       
Und wir schliessen mit der Kontoeröffnung für die zukünftige Bewertung der Velorouten ab. Dazu benötigen wir E-Mail und Passwort.    
     

### Wie bist du unterwegs?
- [ ] Zu Fuss %
- [ ] Velo %
- [ ] **ÖV**: Tram, Bus, Bahn %
- [ ] **MIV**: Auto, Motorrad %

### Dein Velo?
- [ ] Citybike
- [ ] Rennvelo
- [ ] E-Bike, 25km/h
- [ ] Schnelles E-Bike, 45km/h
- [ ] Mountainbike
- [ ] E-Mountainbike
- [ ] Bikesharing (Publibike usw.)

### Wann fährst Du?
- [ ] Arbeit
- [ ] Ausbildung (Schule, Universität)
- [ ] Alltag
- [ ] Freizeit
- [ ] Sport
- [ ] Touren

### Wie oft?
- Täglich
- Mehrmals pro Woche
- Einmal pro Woche, mehrmals pro Monat
- Einmal pro Monat, mehrmals pro Jahr
- Nie

### Alter, Geschlecht, Ort

### Konto Erstellen


PS: 
BFS 2021
- Arbeit
- Ausbildung
- Einkauf
- Freizeit
- Übriges


## Variante 2

### Teilnahme am Pretest Panel
Bewertung der Zürcher Velorouten      
       
Wir möchten VelObserver möglichst vielen Menschen zugänglich machen.          
Dazu laden wir dich ein, uns als Tester:in zu unterstützen.           
               
Wir stellen Fragen zur:
- Verkehrsmittelwahl
- Verkehrsmittelnutzung
- Alter, Geschlecht, Ort
         
Und schliessen mit der Kontoeröffnung für die zukünftige Bewertung der Velorouten ab.        
Dazu benötigen wir E-Mail und Passwort.      


### Wie bist Du unterwegs?
- [ ] Zu Fuss
- [ ] ÖV: Tram, Bus, Bahn  
-------
- [ ] Citybike
- [ ] Rennvelo
- [ ] E-Bike, 25km/h
- [ ] Schnelles E-Bike
- [ ] 45km/h, Mountainbike
- [ ] E-Mountainbike
- [ ] Bikesharing (Publibike usw.)
-------
- [ ] Eigenes Auto
- [ ] Carsharing
- [ ] Motorrad 
--------
- [ ] Skateboard, Scooter

### Wie häufig?
(Auswahl von oben wird in Reihenfolge gebracht)

### Warum fährst Du Velo?
Arbeit, Schule, Universität
- Täglich (mehrmals pro Woche)
- Regelmässig (einmal pro Woche, mehrmals pro Monat)
- Selten (einmal pro Monat, mehrmals pro Jahr)
- Nie

- [x] Auch im Winter

### Alter, Geschlecht, Ort
Ich pendle nach       
PLZ, Ort         

### Konto Erstellen
Damit du später die Velorouten bewerten kannst, benötigst du ein Konto. Die bisher gemachten Aussagen sind wichtig, um die Bewertungen zu gewichten und ihre Repräsentativität zu gewährleisten. 
- E-Mail
- Passwort 


## Other Possibilities
When presenting the first variant to Prototype Fund, David from Businessresponsibility meant, he would like to give a certain time by transport mode. E.g. 30min by Tram. We could then take the average speed to come to km.           
This works less good with broad categories (Velo), so a further differentiation would be needed (e.g. Citybike, E-Bike 25km/h, E-Bike 45km/h etc.).


### Variante 3 (nur "Wie bist du unterwegs?")

#### Unter der Woche 
Pro Tag

| Verkehrsmittel  | Zeit (min) | km/h  | km | 
|---|---|---|---|
| [x] Zu Fuss | [ 15 ] | [ 4 ] | 1 |
| [x] Velo v | [ 20 ] | [ 15 ] | 5 | 
| [x] ÖV v | [ 20 ] | [ 15 ] | 5 |
| [ ] MIV v | [    ] | [  ] |  |
| [ ] Weitere v | [  ] | [  ] |  |
| Total | 55  | ? | 11 |

#### Wochenende, Feiertage, Ferien
Pro Tag

| Verkehrsmittel  | Zeit (min) | km/h  | km | 
|---|---|---|---|
| [x] Zu Fuss | [ 15 ] | [ 4 ] | 1 |
| [x] Velo v | [ 20 ] | [ 15 ] | 5 | 
| [x] ÖV v | [ 20 ] | [ 15 ] | 5 |
| [ ] MIV v | [    ] | [  ] |  |
| [ ] Weitere v | [  ] | [  ] |  |
| Total | 55  | ? | 11 |


Nur das Verkehrsmittel und Zeit müssen angegeben werden.         
Kilometer pro Stunde (default: Durchschnittswert) können justiert werden.  

Evtl. Für jede Überkategorie, kann spezifisch via Dropdown (Velo > Citybike, Rennvelo usw.) ausgewählt werden. 
Wenn ja, dann sollte man aber Mehrfachnennungen pro Kategorie zulassen.

Sind die km/h anpassbar, dann müsste entweder die DB erweitert werden (value2), oder es werden 2 Einträge pro Verkehrsmittel in der Datenbank abgelegt. 

## Design 1
Siehe Video. Einige Inputs von Peter, siehe Design 2, wurden in Version 1 übernommen.

## Design 2
Von Peter Gassner
<table align="top" border="0">
<tr>
<td >
<img src="https://raw.githubusercontent.com/posmocoop/bike-index/main/pretest_panel/media/pg_1.png" width="160"/>
<img src="https://raw.githubusercontent.com/posmocoop/bike-index/main/pretest_panel/media/pg_2.png" width="160"/>
<img src="https://raw.githubusercontent.com/posmocoop/bike-index/main/pretest_panel/media/pg_3.png" width="160"/>
<img src="https://raw.githubusercontent.com/posmocoop/bike-index/main/pretest_panel/media/pg_4.png" width="160"/>
<img src="https://raw.githubusercontent.com/posmocoop/bike-index/main/pretest_panel/media/pg_5.png" width="160"/>
<img src="https://raw.githubusercontent.com/posmocoop/bike-index/main/pretest_panel/media/pg_6.png" width="160"/>  
</td>
</tr> 
</table>     

## Version 2
In einer Version 2, könnten wir neben Design 2 und Variante 3 auch weitere Fragen stellen. 
Siehe z.B. Gfk- und Bosch-Umfrage.
 
          
## Database Structure: VelObserver Personas
### Personas
**user_id, topic, key, value, created_at, updated_at**      
For created_at, updated_at, we probably use UNIX timestamps.


| user_id  | topic  | key  | value  | created_at | updated_at |
|---|---|---|---|---|---|
| XXX  | transport_mode | fussgaenger_pct | 0.40  | 2021-09-20  | |
| XXX  | transport_mode | velo_pct | 0.25  | 2021-09-20  | |
| XXX  | transport_mode | oev_pct | 0.35  | 2021-09-20 | |
| XXX  | transport_mode | miv_pct | 0.00  | 2021-09-20  | |  
| XXX  | bike_type | citybike | 1 | 2021-09-20 | |
| XXX  | bike_type | rennvelo | 0 | 2021-09-20 | |
| XXX  | bike_type | e-bike25km | 0 | 2021-09-20 | |
| XXX  | bike_type | e-bike45km | 0 | 2021-09-20  | |
| XXX  | bike_type | mountainbike | 0 | 2021-09-20 | |
| XXX  | bike_type | e-mountainbike | 0 | 2021-09-20  | |
| XXX  | bike_type | bikesharing | 1 | 2021-09-20 | |
| XXX  | bike_usage | arbeit | 0 | 2021-09-20 | |  
| XXX  | bike_usage | ausbildung | 0 | 2021-09-20 | |  
| XXX  | bike_usage | alltag | 1 | 2021-09-20 | |  
| XXX  | bike_usage | freizeit | 1 | 2021-09-20 | |  
| XXX  | bike_usage | sport | 0 | 2021-09-20  | | 
| XXX  | bike_usage | touren | 0 | 2021-09-20 | | 
| XXX  | bike_frequency | selten | 1 | 2021-09-20 | |  
| XXX  | transport_mode | fussgaenger_pct | 0.40  | 2021-09-20  | 2022-10-09|
| XXX  | transport_mode | velo_pct | 0.55  | 2021-09-20  | 2022-10-09 |
| XXX  | transport_mode | oev_pct | 0.05  | 2021-09-20 | 2022-10-09 |
| XXX  | transport_mode | miv_pct | 0.00  | 2021-09-20  | 2022-10-09 | 
| XXX  | bike_type | citybike | 0 | 2021-09-20 | 2022-10-09 |
| XXX  | bike_type | rennvelo | 0 | 2021-09-20 | 2022-10-09 |
| XXX  | bike_type | e-bike25km | 0 | 2021-09-20 | 2022-10-09 |
| XXX  | bike_type | e-bike45km | 1 | 2021-09-20  | 2022-10-09 |
| XXX  | bike_type | mountainbike | 0 | 2021-09-20 | 2022-10-09 |
| XXX  | bike_type | e-mountainbike | 0 | 2021-09-20 | 2022-10-09 |
| XXX  | bike_type | bikesharing | 1 | 2021-09-20 | 2022-10-09 |
| XXX  | bike_usage | arbeit | 1 | 2021-09-20 | 2022-10-09|  
| XXX  | bike_usage | ausbildung | 0 | 2021-09-20 | 2022-10-09 |  
| XXX  | bike_usage | alltag | 1 | 2021-09-20 | 2022-10-09 |  
| XXX  | bike_usage | freizeit | 1 | 2021-09-20 | 2022-10-09 |  
| XXX  | bike_usage | sport | 0 | 2021-09-20  | 2022-10-09 | 
| XXX  | bike_usage | touren | 0 | 2021-09-20 | 2022-10-09 | 
| XXX  | bike_frequency | taeglich | 1 | 2021-09-20  | 2022-10-09 |  

Last rows are examples after an update, values and keys can switch from 0 to 1 and vice versa. That is why it is meaninful to store zero values as well for the topics with multiple options. Only bike_frequency wouldn't need an additional value, as the selected one will be unique and always be 1. 
We might also modify or extend the DB in the future, so it is good to use all options. 



### Topics          
1. user_id, transport_mode [options: fussgaenger|velo|oev|miv], 0.00-1.00     
(more than one, max. 4 options)     
     
2. user_id, bike_type [options: citybike|rennvelo|e-bike25km|e-bike45km|mountainbike|e-mountainbike|bikesharing], 1 or 0    
(more than one option)      
      
3. user_id, bike_usage [options: arbeit|ausbildung|alltag|freizeit|sport|touren], 1 or 0    
(more than one option)    
      
4. user_id, bike_frequency [options: taeglich|regelmaessig|selten|nie], 1 or 0    
(only one option)    
    




