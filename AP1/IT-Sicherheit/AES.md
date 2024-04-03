---
tags:
  - "#AP1"
  - "#IT-Sicherheit"
---
## Bedeutung 
AES steht für Advanced Encryption Standard und wurde von Joan Daemen und Vincent Rijmen entwickelt. Es handelt sich um ein symmetrisches Verschlüsselungsverfahren, d.h. der Schlüssel zum Ver- und Entschlüsseln ist der Selbe. 

## Block- und Schlüssellänge
Die Blockgröße beträgt 128 Bit während die Schlüssellänge zwischen 128, 192 oder 256 Bit variieren kann. Man spricht dann auch von AES-128, AES-192 oder AES-256.

## Anwendung 
AES findet in den Verschiedensten Bereichen Anwendung, da es der heutige symmetrische Verschlüsselungsstandard ist. Dieses verfahren wird mittlerweile durch Prozessoren unterstützt. So haben Prozessoren erweiterte Befehlssätze für AES.
Zu diesen Bereichen zählen z.B.
+ WLan (IEEE 802.11i)
+ WPA2
+ SSH
+ IPSec
+ ...

## Ablauf

### Anzahl der Runden

| Schlüsselgröße: | 128 | 192 | 256 |
| -- | -- | -- | -- | 
| Anzahl Runden R: | 10 | 12 | 14 |

### PAP
1) Schlüsselexpansion 
2) AddRoundKey(Rundenschlüssel[0])
3) Verschlüsselungsrunden r = 1 bis R-1:
	1)  SubBytes()
	2) ShiftRows()
	3) MixColumns()
	4) AddRoundKey(Rundenschlüssel[r])
4) Schlussrunde:
	1) SubBytes()
	2) ShiftRows()
	3) AddRoundKey(Rundenschlüssel[R])

Bei der Verschlüsselung wird der PAP von oben nach unten abgearbeitet, bei der Entschlüsselung werden als erstes die Rundenschlüssel generiert und dann der PAP von unten nach oben, also rückwärts abgearbeitet. 