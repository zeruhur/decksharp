# VEIL

## Un astratto per 2 (o 4) giocatori su DECK#

**Sistema:** DECK# (Profilo Base)  
**Giocatori:** 2 · espandibile a 4 con un secondo mazzo  
**Durata:** 20–40 minuti  
**Componenti:** 1 mazzo DECK# · nessun componente aggiuntivo

---

## Il concetto

Due giocatori giocano le carte del proprio colore per costruire sequenze e formare coppie con le carte avversarie. Ogni carta ha un valore, un glifo primario e un modificatore: la combinazione di questi elementi determina se una coppia è valida, chi la vince, e quanto vale.

VEIL è un gioco di informazione parziale: le carte in mano sono nascoste, quelle giocate sono visibili. La tensione è tra ciò che sai e ciò che supponi.

---

## Mappatura degli assi DECK#

| Asse | Valore in VEIL |
|---|---|
| **Colore** | Appartenenza: ogni giocatore gioca solo le proprie carte (rosso o nero) |
| **Valore (A–K)** | Forza della carta: A = 1 (minimo) · K = 13 (massimo) |
| **Seme** | Famiglia: ♥/♣ = famiglia alta · ♦/♠ = famiglia bassa |
| **Primario** | Tipo della carta: determina come si forma una coppia valida |
| **Modificatore** | Condizione: modifica il valore della coppia a posteriori |

---

## Setup

Mescola il mazzo. Distribuisci **7 carte** a ciascun giocatore. Il giocatore con carte rosse gioca per primo. Le carte non distribuite formano il **pozzo** coperto al centro.

Con 4 giocatori (due mazzi): due giocatori per squadra (uno rosso, uno nero per squadra), 6 carte a testa. I compagni di squadra non possono mostrarsi le carte.

---

## Struttura del turno

Ogni turno si compone di due fasi obbligatorie:

### Fase 1 — Gioco

Il giocatore attivo **gioca 1 carta** dalla propria mano, scoperta, davanti a sé. Questa carta è la sua **offerta**.

### Fase 2 — Risposta

L'avversario guarda la carta giocata e sceglie una delle tre opzioni:

**a) Accoppia** — gioca dalla propria mano una carta che forma una **coppia valida** con l'offerta (vedi Coppie valide). Entrambe le carte vengono rimosse dal tavolo e assegnate al giocatore che ha vinto la coppia (vedi Risoluzione).

**b) Passa** — non gioca nessuna carta. L'offerta rimane sul tavolo come **carta esposta**. Il giocatore che ha passato pesca 1 carta dal pozzo.

**c) Sfida** — gioca una carta che non forma coppia valida, dichiarando esplicitamente "sfida". Le due carte rimangono sul tavolo come **campo aperto**. Entrambi i giocatori pescano 1 carta dal pozzo. Al proprio prossimo turno, il giocatore sfidato deve rispondere al campo aperto prima di poter giocare una nuova offerta.

Dopo la risposta, il turno passa all'avversario.

---

## Coppie valide

Una coppia è valida se le due carte soddisfano **almeno una** delle seguenti condizioni:

| Condizione | Regola |
|---|---|
| **Risonanza di glifo** | Le due carte hanno lo stesso glifo primario |
| **Risonanza di famiglia** | Le due carte appartengono alla stessa famiglia (♥/♣ oppure ♦/♠) |
| **Sequenza** | I valori delle due carte sono consecutivi (es. 7 e 8, o Q e K) · A e K sono consecutivi |
| **Simmetria** | Una carta è rossa e l'altra è nera, e il valore della carta rossa + il valore della carta nera = 14 (es. 3♥ + J♠, oppure A♦ + K♣) |

Più condizioni soddisfatte = coppia più forte (vedi Risoluzione).

---

## Risoluzione della coppia

Quando si forma una coppia valida, si determina chi la vince:

1. **Conta le condizioni soddisfatte** (1–4). Chi ha giocato la carta che soddisfa più condizioni vince la coppia. In caso di parità, vince chi ha il valore più alto.

2. **Applica il modificatore** della carta vincente:

| Modificatore | Effetto |
|---|---|
| • (punto) | La coppia vale 1 punto bonus aggiuntivo |
| — (linea) | Nessun modificatore |
| + (croce) | Il vincitore della coppia pesca 1 carta dal pozzo |
| × (diagonale) | Il perdente della coppia scarta 1 carta a scelta dalla propria mano (scoperta, va al pozzo) |
| △ (triangolo) | La coppia vale doppio nel conteggio finale |
| ○ (cerchio) | Il vincitore può giocare immediatamente un'altra offerta senza passare il turno |
| □ (quadrato) | Il vincitore mette la coppia coperta (non visibile al conteggio parziale degli avversari) |

3. **Chi vince la coppia** la mette davanti a sé, scoperta (o coperta se □). Le coppie accumulate sono visibili a tutti, eccetto quelle con modificatore □.

---

## Le figure: carte Velo

J, Q e K sono **carte Velo**. Hanno proprietà speciali:

- **Non possono essere giocate come offerta** al primo turno di ciascun giocatore.
- **Formano coppia valida con qualsiasi carta** (ignorano le condizioni normali), ma con un vincolo: la carta Velo vince la coppia **solo se** il suo valore è strettamente maggiore dell'avversaria. Altrimenti vince l'avversario.
- **Il modificatore della carta Velo si applica sempre**, indipendentemente da chi vince la coppia.

Le figure tendono verso • e △ nella distribuzione DECK# — presenza e direzione. Nel gioco questo si traduce in carte che valgono punti bonus o coppie doppie, ma che rischiano di perdere se l'avversario ha un valore alto.

---

## I Jolly: carte Nebbia

I 2 Jolly non entrano nel mazzo distribuito. Vengono posizionati scoperti ai lati del pozzo prima del gioco, come **riserva condivisa**.

Una volta per partita, invece di giocare un'offerta o rispondere, un giocatore può prendere un Jolly dalla riserva e usarlo come **carta jolly** — vale come qualsiasi glifo primario e qualsiasi famiglia, con valore 0. Può formare coppia con qualsiasi carta, ma vince la coppia **solo se** l'avversario ha valore A (1).

Il Jolly è uno strumento difensivo: non per vincere, ma per non perdere in un momento critico.

---

## Fine della partita

La partita termina quando:
- Un giocatore esaurisce la mano **e** il pozzo è vuoto, oppure
- Un giocatore ha accumulato **7 coppie**.

### Conteggio

Ogni coppia vale **1 punto base**, più:
- +1 per ogni condizione soddisfatta oltre la prima
- Modificatori applicati (△ raddoppia, • aggiunge 1)
- Le coppie □ vengono rivelate e conteggiate solo ora

Il giocatore (o la squadra) con più punti vince.

**Patta:** se i punti sono uguali, vince chi ha più coppie. Se ancora pari, vince chi ha la coppia singola di valore più alto.

---

## Variante a 4 giocatori

Si usano **due mazzi DECK#** mescolati insieme. I giocatori si dispongono alternati (rosso–nero–rosso–nero). Ogni squadra ha un giocatore con carte rosse e uno con carte nere.

Variazioni:
- Le coppie valide ora possono formarsi **anche tra compagni di squadra** (stessa condizione di risonanza), ma il punto va alla squadra, non al singolo giocatore.
- Le carte Velo giocate da un compagno di squadra non possono essere sfidate dal compagno — solo dagli avversari.
- Il conteggio è per squadra: si sommano i punti di entrambi i giocatori.

La durata si allunga a 40–60 minuti.

---

## Note di design

**Perché il colore mappa all'appartenenza?**  
Il colore è l'asse più visibile. In un gioco senza componenti aggiuntivi, la distinzione "mia carta / tua carta" deve essere immediata a colpo d'occhio. Il rosso/nero del mazzo standard assolve questo ruolo senza nessun marcatore aggiuntivo.

**Perché la simmetria (rosso + nero = 14) è una condizione di coppia?**  
Perché sfrutta la struttura del mazzo in modo non ovvio: A♦ e K♣ sono "complementari" nel senso letterale. Introduce una tensione produttiva — le carte di valore medio (7, 7) non si completano a vicenda, mentre gli estremi (A/K, 2/Q, 3/J) sì. Il giocatore deve tenere a mente sia le proprie carte sia quelle esposte per calcolare le complementarità.

**Perché le figure non possono essere offerta al primo turno?**  
Evita l'apertura dominante. Una carta Velo in apertura forzarebbe l'avversario in una risposta obbligata prima di avere informazioni sul campo. Ritardarne l'uso di un turno apre spazio strategico.