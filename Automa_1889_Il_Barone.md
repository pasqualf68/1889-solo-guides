# Automa per 1889: "Il Barone di Shikoku" (v1.0)

Questo sistema permette di giocare a **1889** in solitario contro uno o più avversari virtuali (Automi). L'Automa agisce come un investitore razionale ma aggressivo.

---

## 1. Setup dell'Automa
*   **Giocatori:** Tu (Umano) vs 1 o 2 Automi.
*   **Capitale:** L'Automa riceve il capitale standard per il numero di giocatori.
*   **Priorità:** L'Automa ha sempre la precedenza nelle scelte se il regolamento non specifica diversamente.

---

## 2. Round Azionario (Stock Round)
L'Automa segue questa gerarchia di azioni (esegue la prima possibile):

1.  **Protezione Presidenza:** Se una compagnia dell'Automa è senza treno e ha bisogno di fondi, l'Automa non compra nulla e risparmia.
2.  **Acquisto Azioni (Se ha soldi):**
    *   **Priorità A:** Compra un'azione della compagnia che ha pagato il dividendo più alto nell'ultimo turno.
    *   **Priorità B:** Se nessuna ha pagato, apre una nuova compagnia (compra il certificato della Presidenza) partendo da quella con il valore di mercato più alto ancora disponibile.
    *   **Priorità C:** Compra un'azione della compagnia del giocatore Umano (per parassitare i dividendi).
3.  **Vendita Azioni:** L'Automa vende solo se deve coprire l'acquisto obbligatorio di un treno. Vende prima le azioni delle compagnie dell'Umano, poi le proprie (partendo dalla meno redditizia).

---

## 3. Round Operativo (Operating Round)
Quando l'Automa presiede una compagnia, segui queste regole "algoritmiche":

### A. Costruzione Binari (Tile Laying)
L'Automa piazza tasselli seguendo questa priorità:
1.  **Connessione:** Verso la città a valore più alto non ancora raggiunta.
2.  **Potenziamento (Upgrade):** Potenzia una città già raggiunta se questo aumenta il valore della rotta attuale.
3.  **Ostruzione:** Se non può aumentare il proprio valore, piazza un tassello che blocca o complica la strada verso la città più vicina alla compagnia dell'Umano.

### B. Stazioni (Tokens)
L'Automa piazza una stazione se:
*   Può bloccare l'accesso dell'Umano a una città da 30+ o a una città "rossa" (off-board).
*   È necessario per garantire la propria rotta verso **Takamatsu** o **Kochi**.

### C. Dividendi
*   L'Automa **Paga sempre** i dividendi (Pay Out), a meno che la compagnia non sia senza treni o il treno attuale stia per "arrugginire" (rust) nel turno successivo. In quel caso, **Trattiene tutto** (Withhold).

### D. Acquisto Treni
*   L'Automa compra sempre il miglior treno disponibile se ha i fondi.
*   Se una compagnia dell'Automa è senza treno, l'Automa userà i fondi della compagnia. Se non bastano, l'Automa (come giocatore) contribuirà con i propri soldi (come da regole standard).

---

## 4. Gestione delle Compagnie Private
Durante l'asta iniziale, l'Automa:
*   Compra sempre la privata meno costosa disponibile finché ha soldi.
*   Se l'Umano punta su una privata costosa, l'Automa "passa" per risparmiare capitale per le compagnie pubbliche.

---

## 5. Livelli di Difficoltà
*   **Facile (Il Novellino):** L'Automa non piazza mai stazioni per bloccare l'Umano.
*   **Medio (L'Imprenditore):** Segue le regole sopra descritte.
*   **Difficile (Il Barone):** L'Automa riceve 100¥ extra di capitale iniziale e non vende mai azioni delle proprie compagnie a meno che non sia l'ultima risorsa per evitare il fallimento.

---

## Consigli per l'Umano
L'Automa è prevedibile ma efficiente. La tua unica speranza è superarlo in astuzia nella **gestione del timing dei treni**. L'Automa comprerà treni appena possibile, accelerando la partita: assicurati di non restare a secco quando i treni "2" spariranno!
