#Layer2
## Frame 
Die normale Größe eines Frames beträgt 1500 Bytes
Die minimale Größe eines Frames beträgt 64 Bytes. Frames die kleiner als die minimale Größe sind, heißen Runt-Frames.
Die Maximale Größe eines Frames beträgt 1518 Bytes, wovon 1500 für die Nutzlast zugänglich sind .

## Aufbau 
> [!ascii] Ethernet Frame
> ╔════════╤═════════╤═══════════╤══════╤════╗
> ║ Frame  │ Network │ Transport │ Data │    ║
> ║ Header │ Header  │ Header    │      │    ║
> ╚════════╧═════════╧═══════════╧══════╧════╝
>ㅤㅤㅤ⇓                                       ⇘
> ╔════════╤═══════════╤═══════════╤══════╗   ╔════════════╗
> ║Preamble│Destination│  Source   │ Type ║   ║FCS Checksum║
> ║        │MAC Address│MAC Address│      ║...║   (CRC)    ║
> ╚════════╧═══════════╧═══════════╧══════╝   ╚════════════╝
>Bytes:
>ㅤㅤㅤ8ㅤㅤㅤㅤㅤㅤ6ㅤㅤㅤㅤ ㅤ6ㅤㅤㅤㅤㅤ 2ㅤㅤㅤㅤㅤㅤㅤㅤ4

