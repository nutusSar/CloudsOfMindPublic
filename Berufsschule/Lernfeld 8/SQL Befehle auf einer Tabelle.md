
## Aufgabe 1
+ Eine Liste aller Schüler:
```SQL
SELECT name, vorname
FROM schueler
ORDER BY name
```

+ Eine Liste der Räume
```SQL
SELECT nummer, plaetze
FROM raum
ORDER BY plaetze DESC
```

+ Eine Liste der Etagen
```SQL
SELECT DISTINCT etage
FROM raum
```

## Aufgabe 2
+ Wie viele Schüler gibt es insgesamt?
```SQL
SELECT COUNT(*)
FROM schueler
```

+ Wie viele Stunden Unterricht werden insgesamt erteilt?
```SQL
SELECT SUM(stunden)
FROM unterricht
```

+ Wie viele Stunden Sport werden erteilt?
```SQL
SELECT SUM(STUNDEN) 
FROM UNTERRICHT 
WHERE FACH = 'Sport';
```

+ Wie viele Plätze hat der Größte Raum?
```SQL
SELECT MAX(PLAETZE) 
FROM RAUM;
```

+ Wie viele Plätze haben die Räume in der oberen Etage?
```SQL
SELECT AVG(PLAETZE) 
FROM RAUM 
WHERE ETAGE = 'oben';
```

## Aufgabe 3
+ Eine Liste der Etagen, in der vermerkt ist, wie viele Räume es jeweils in der Etage gibt
```SQL
SELECT ETAGE, COUNT(*) 
FROM RAUM 
GROUP BY ETAGE;
```

+ Eine Liste der Etagen, in der vermerkt ist, wie viele Plätze es jeweils in der Etage gibt
```SQL
SELECT ETAGE, SUM(PLAETZE) 
FROM RAUM 
GROUP BY ETAGE;
```

+ Eine Liste aller Unterrichtsfächer, in der steht, wie viele Stunden sie jeweils unterrichtet werden; die Unterrichtsfächer mit vielen Stunden sollen oben stehen
```SQL
SELECT FACH, SUM(STUNDEN) AS ANZSTUNDEN 
FROM UNTERRICHT 
GROUP BY FACH 
ORDER BY ANZSTUNDEN DESC;
```
