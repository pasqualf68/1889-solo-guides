# Guida allo Sviluppo Tecnico 18xx

Usa questi standard per tradurre la tua idea in un prototipo giocabile.

---

## 1. Il Blueprint (JSON per 18xx-maker)
Crea un file chiamato `mygame.json` con questa struttura base:

```json
{
  "info": {
    "title": "18XX: Il Mio Gioco",
    "designer": "Tuo Nome"
  },
  "trains": [
    { "name": "2", "quantity": 6, "price": 80, "rusts": "4" },
    { "name": "3", "quantity": 5, "price": 180, "rusts": "6" }
  ],
  "companies": [
    {
      "id": "FS",
      "name": "Ferrovie dello Stato",
      "color": "blue",
      "tokens": [0, 40, 100]
    }
  ],
  "map": {
    "hexes": {
      "A1": { "color": "white", "cities": [{ "name": "Città", "revenue": 20 }] }
    }
  }
}
```

---

## 2. Il Motore Economico (Formule Excel)
Crea un foglio di calcolo con queste colonne per testare la "Train Rush":

*   **Colonna A:** Nome Treno
*   **Colonna B:** Prezzo
*   **Colonna C:** Rendita Media Stimata (per compagnia)
*   **Colonna D:** Turni necessari per ripagarsi il treno (`Prezzo / Rendita`)

*Regola empirica:* Un treno dovrebbe ripagarsi in 2-3 round operativi. Se ci mette di più, il gioco sarà lento e frustrante.

---

## 3. Risorse per il Coding
Se vuoi implementare il gioco su **18xx.games**:
1. Clona il repository `tobymao/18xx`.
2. Guarda la cartella `lib/engine/game/` per vedere come sono definiti i giochi esistenti.
3. Ogni gioco è una classe Ruby che eredita da `Base`.
