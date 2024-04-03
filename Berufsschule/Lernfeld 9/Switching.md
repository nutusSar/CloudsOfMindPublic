## [Switch](Switch.md)
+ [Switches](Switch.md) arbeiten auf Layer 2
+ Speichern Ziel MAC-Adressen mit dem Port in einer MAC-Address-Table 
+ Eingangsport (Ingress) eines Frames kann nie gleichzeitig Ausgangsport (Egress) sein
+ Anzeigen der MAC-Address-Table:
```console
show mac address-table
```
+ Ein Eintrag in dieser Tabelle hat in der Regel eine TTL von 5 min (300s). 

## Logik
![[switch_logik.png]]

## Unterschied zum Hub:
+ [Frame](Ethernet%20Frame.md) gehen nur zum Ziel Port raus, Ziel wird anhand der MAC-Adresstabelle (CAM Content-addressable Memory) ermittelt.

## Verfahren 1: Store and Forward 
[Frame](Ethernet%20Frame.md) wirst erst nach der Prüfung der Frame Check Sequenz Weitergeleitet. Dazu wird der gesamte Frame gespeichert. Dies hat den Nachteil, dass es zu einer höheren Latenz kommt. Jedoch ergibt sich daraus auch der Vorteil, dass es weniger fehleranfällig ist.

## Verfahren 2: Cut-Through
[Frame](Ethernet%20Frame.md) wird nach Empfangen von Preamble (010101...) und Ziel-Mac direkt weitergeleitet. Keine FCS-Prüfung möglich.
**Vorteil:** Schneller (weniger Latenz)
**Nachteil:** Keine Fehlererkennung

### 2 Arten von Cut-Through:
+ **Fast forward:** nach Ziel-MAC
+ **Fragment Free:** nach 64 Byte (Mindestgröße) -> Kompromiss zwischen Fehlerkontrolle und Geschwindigkeit 

## Übersicht der Methoden
> [!ascii] Schaubild
>Bytes:
>ㅤㅤ   7      1   6      6      2      max 1500    4
>ㅤ╔════════╤═══╤═════╤══════╤═══════╤════════════╤═══╗
>ㅤ║Preamble│SFD│Dest.│Source│Length/│    Data    │FCS║
>ㅤ║        │   │Addr │Addr. │ Type  │            │   ║
>ㅤ╚════════╧═══╧═════╧══════╧═══════╧════════════╧═══╝
>ㅤ             ⇑                      ⇑            ⇑
>ㅤ        Fast Forward          Fragment Free  Store and
>ㅤ               ⇖                   ⇗          Forward
>ㅤ                     Cut-Trough


## Kollisionsdomäne / Collision Domain (CD)
Bereich, in dem max. 1 Gerät pro Richtung reden kann 
**Beispiel IRL:**
	Ein Raum:
	Wenn mehrere Personen sprechen, gibt es eine Kollision 
Mit modernen Switches ist jeder Link (Switch zu Gerät) eine eigene CD

## Broadcast-Domain
Bereich, in dem Broadcasts weitergeleitet werden
+ Entspricht dem Lan (Layer 2)
+ Layer 2 Geräte gehören zu einer Broadcastdomain 
+ Layer 3 Geräte (Router) teilen sich eine Broadcastdomain
+ Endet am Router

## 
Switches bilden mathematisch gesehen einen Graphen, d.h. ein Gebilde aus Knoten (Switches) und Kanten (Leitungen).
Das es auf Layer 2 keine TTL o.ä. gibt muss ein Zyklus (eine Schleife) unbedingt verhindert werden.
-> sonst kompletter Stillstand durch im Kreis gesendeter Frames

**Lösung:** Abschaffen von redundanten Verbindungen um einen schleifenfreien Graph (-> einen Baum) zu bekommen. -> Spanning Tree Protocol (STP) 

