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

## Auflistung der Protokolle
+ [[OSPF]]
+ 