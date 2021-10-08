# Pretest Panel

## Variante 1

### Pretest Panel für die Bewertung der Velorouten
Um den VelObserver-Index von möglichst vielen verschiedenen Menschen testen lassen zu können, richten wir ein Pretest Panel ein, damit wir ein möglichst gutes Bild haben, wer unsere zukünftigen Tester:innen sind.        
        
Wir stellen Fragen zur:     
- Verkehrsmittelnutzung        
- Alter, Geschlecht, Ort         
       
Und wir schliessen mit der Kontoeröffnung für die zukünftige Bewertung der Velorouten ab. Dazu benötigen wir E-Mail und Passwort.    
     

### Wie bist Du unterwegs?
- Zu Fuss %
- Velo %
- ÖV: Tram, Bus, Bahn %
- MIV: Auto, Motorrad %

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
When presenting the first variant to Prototype Fund, David meant, he would like to give time by transport mode. E.g. 30min by Tram. We could then take the average speed to come to km. 


## Design 1

## Design 2



## Database Structure
user_id, key, value             
          
1. user_id, transport_mode [options: fussgaenger|velo|oev|miv], 0.00-1.00     
(more than one, max. 4 options)   
2. user_id, bike_type [options: citybike|rennvelo|e-bike25|e-bike45|mountainbike|e-mountainbike|bikesharing], 1 or 0    
(more than one option)     
3. user_id, bike_usage [options: arbeit|ausbildung|alltag|freizeit|sport|touren], 1 or 0    
(more than one option)   
4. user_id, bike_frequency [options: taeglich|regelmaessig|selten|nie], 1 or 0    
(only one option)   





