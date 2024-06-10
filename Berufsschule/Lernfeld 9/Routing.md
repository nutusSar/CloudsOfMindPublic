## Routingprotokolle
Routingprotokolle werden von Routern genutzt, um Informationen über erreichbare Netze (Routen) auszutauschen. Eine solche Route könnte wie folgt aussehen:
```cli
Router2# show ip route
```
![[Pasted image 20240513141038.png]]

Ohne Routingprotokolle müssten alle Routen statisch von Hand eingetragen werden -> hoher Aufwand, keine Flexibilität bei Defekten

Heute sind 2 Arten/Familien von Routingprotokollen im Einsatz. 
+ **Distanzvektorprotokolle**: einfacher, jeder Router baut sich seine eigene Tabelle auf z.B. RIP
+ **Link-State**: komplexer, es wird eine generische Tabelle gebildet
## Statisches vs. Dynamisches 
Beim **statischem** Routing werden die Einträge händisch in die Routingtabelle eingetragen. Hingegen beim **dynamischem** Routing werden diese Einträge über Protokolle automatisiert.
## Arten der Protokolle

### Link-State-Protokolle
#### Definition
Link-State- Protokolle tauschen Informationen über ihre direkten Verbindungen und deren Status mit allen anderen Routern aus. Dadurch wird eine komplexe Datenbank aufgebaut.

#### Protokolle
+ [[OSPF]]
+ IS-IS

### Distanz-Vektor-Routing
#### Definition
Jeder Router kennt nur die Distanz und Richtung. Dabei werden Informationen mit ihren Nachbarn ausgetauscht und über z.B. den **Bellman-Ford-Algorithmus** ihre Routingtabellen aktualisiert.
#### Protokolle
+ RIP (**R**outing **I**nformation **P**rotocoll)
+ RIPv
+ BGP (**B**order **G**ateway **P**rotocoll)
### Link-State vs. Distanz-Vektor
| **Link-State**                        | **Distanz-Vektor**    |
| ------------------------------------- | --------------------- |
| schnellere Konvergenz                 | geringere Komplexität |
| genaueres Routing                     | weniger Speicher      |
| bessere Skalierbarkeit                | geringere CPU Last    |
| reagieren schneller auf Veränderungen | geringere Bandbreite  |

## Codes
![[Pasted image 20240610081720.png]]

## Metrik
Bei der Metrik einer Route handelt es sich um die Summe der Kosten aller Router.
### OSPF
Bei OSPF handelt es sich um die Bandbreite -> Je größer die Bandbreite, desto geringer die Kosten.
$cost=\frac{costreference}{bandwith}$

### RIP
Bei RIP handelt es sich bei der Metrik um die Anzahl der Hops. Dabei entspricht ein Hop einem Router. -> Je kleiner der Hop-Count, desto geringer die Metrik. 
+ **1 Hop**: Direkt verbundenes Netzwerk
+ **2 Hops**: Über einen weiteren Router erreichbar
+ **...**
+ **15 Hops** Maximale Anzahl an Routern
+ **16 Hops** Nicht mehr erreichbar

## Troubleshooting
+ Der Ping Befehl ist eine einfache und schnelle Möglichkeit, die Erreichbarkeit eines Netzwerkes zu überprüfen.
```bash
ping <IP-Address>
```

+ Der folgende Befehl kann benutzt werden, um die Hops der Route nachzuvollziehen
```bash
(Linux): traceroute <IP-Address>
(Windows): tracert <IP-Address>
```
+ Auf einem Router können die Routen über folgenden Befehl angezeigt werden:
```CLI
Router> show ip route
```

```CLI
Router# show ip protocols 
Router# show ipv6 protocols 
Router# show ip route ospf 
Router# show ipv6 route ospf 
Router# show ip ospf Router# show ipv6 ospf 
Router# show ip ospf neighbor 
Router# show ipv6 ospf neighbor 
Router# show ip ospf interface 
Router# show ipv6 ospf interface Router# show ip ospf interface brief 
Router# show ipv6 ospf interface brief Router# clear ip ospf process 
Router# clear ipv6 ospf process 
```
