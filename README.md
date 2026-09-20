# La Miniera di Orapa

Un porting digitale del gioco da tavolo di deduzione e logica **La Miniera di Orapa** (ideato da Junghee Choi e Wanjin Gill / Gameology). 

L'ho sviluppato interamente in **C++17**, usando **Raylib** per la parte grafica e **ENet** per gestire il multiplayer P2P.

---

## Come funziona il gioco
È un gioco per 2 giocatori, completamente simmetrico:
* Ognuno posiziona e nasconde segretamente le proprie pietre sulla propria plancia.
* A turno, si fa da ricercatore sulla plancia dell'avversario.
* Sparando onde dalle porte perimetrali (o sondando singole celle), bisogna capire dove sono nascoste le pietre avversarie basandosi sui rimbalzi, i colori e gli assorbimenti.

## Caratteristiche
* **P2P Reale**: Non ci sono server di mezzo. Uno fa da host e l'altro si collega inserendo l'IP.
* **Motore solido**: Gestisce raytracing delle onde, riflessi diagonali, pareti e pietre speciali (come il diamante o la pietra nera).

## Cosa ho usato (Tech Stack)
* **Linguaggio**: C++17
* **Grafica**: [Raylib](https://www.raylib.com/)
* **Networking**: [ENet](https://github.com/lsalzman/enet) (UDP)
* **JSON**: [nlohmann/json](https://github.com/nlohmann/json)

---

## Crediti & Copyright
* **Gioco originale**: Junghee Choi e Wanjin Gill (Gameology).
* **Adattamento e sviluppo software**: Copyright (c) LordCambion. Tutti i diritti riservati.
