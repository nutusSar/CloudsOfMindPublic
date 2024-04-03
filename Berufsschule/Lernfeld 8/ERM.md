---
tags: 
excalidraw-plugin:
---
## Aufgabe 1
![[Pasted image 20240129122859.png]]

Bestellung (<u>BestellungsID</u>, Attribute, *KundeID*)

Artikel (<u>ArtikelID</u>, Attribute)

Menge (<u>BestellungsID, ArtikelID</u>)

Kunde (<u>KundeID</u>, Attribute, *GirokontoID*)

Girokonto (<u>GiroKontoID</u>, Attribute)

## Aufgabe 2
![[Pasted image 20240129123841.png]]

Hilfsosterhase (<u>HONr</u>, Name, Telefon)

beauftragen (<u>ONr, HONr</u>)

Osterhaste (<u>ONr</u>, Name)

entnehmen (<u>HONr, LNr</u>)

Lagerort (<u>LNr</u>, Ort, *ONr*)

Wunsch (<u>WNr</u>, Wunsch, *KNr*, *ONr*)

Kind (<u>KNr</u>, Alter, Name, Adresse)

## Aufgabe 3
![[Pasted image 20240131120636.png]]

### Teil 1
### Teil 2
Krankenhaus (<u>Krankenhausnummer</u>, Namen, Anschrift, AnzahlBetten)

Arzt (<u>PersonalnummerAZ</u>, Namen, Adresse, Fachgebiet, *Krankenhausnummer*)

Patient (<u>Patientennummer</u>, Namen, Geschlecht, Adresse, Geburtsdatum, Station, *PersonalnummerAZ*, *Zimmernummer*)

Labor (<u>Labornummer</u>, Namen, Anschrift, Telefonnummer)

LaborKrankenhaus (<u>Labornummer, Krankenhausnummer</u>)

Test (<u>Testcode</u>, Typenstatus, Datum, *Labornummer*, *Patientennummer*)

Pflegepersonal (<u>PersonalnummerPF</u>, Name, Adresse, Geschlecht, Station, Alter)

Zimmer (<u>Zimmernummer</u>, Bettenanzahl, *Krankenhausnummer*, *PersonalnummerPF*)

Krankheit (<u>NameKR</u>, Symptome, Status)

PatientKrankheit (<u>Patientennummer, NameKR</u>)

Medikament (<u>NamenMD</u>, Preis, Bestand, Lieferanten)

PatientMedikament (<u>Patientennummer, NamenMD</u>)



