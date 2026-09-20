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
* **Asset modificabili**: Vuoi cambiare le forme o i colori delle pietre? Ti basta modificare il file `assets/stones.json` senza ricompilare il codice[cite: 8].
* **No Console in Release**: Quando compili in `Release`, la finestra nera del terminale sparisce automaticamente grazie a una macro (`#ifdef NDEBUG`).

## Cosa ho usato (Tech Stack)
* **Linguaggio**: C++17
* **Grafica**: [Raylib](https://www.raylib.com/)
* **Networking**: [ENet](https://github.com/lsalzman/enet) (UDP)
* **JSON**: [nlohmann/json](https://github.com/nlohmann/json)

---

## Come compilarlo (con Visual Studio)

Il progetto usa **CMake** (versione 3.16 o superiore), quindi aprirlo in Visual Studio è semplicissimo:

1. Apri **Visual Studio** e fai *Apri una cartella locale*, selezionando la cartella del progetto.
2. CMake scaricherà in automatico tutte le dipendenze necessarie (Raylib, ENet, nlohmann-json) tramite `FetchContent`[cite: 1].
3. Seleziona il target **`OrapaMine.exe`** dal menu in alto[cite: 1].
4. Scegli se compilarlo in **Debug** (con la console attiva per i log) o in **Release** (gioco pulito a schermo intero/finestra).
5. Premi **F5** per compilare e partire! La cartella `assets/` viene copiata in automatico accanto all'eseguibile[cite: 1].

---

## Crediti & Copyright
* **Gioco originale**: Junghee Choi e Wanjin Gill (Gameology).
* **Adattamento e sviluppo software**: Copyright (c) LordCambion. Tutti i diritti riservati.
