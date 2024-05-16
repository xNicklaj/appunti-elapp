# Multiplexer e Sample Hold
Multiplexer e Sample-Hold sono l'ultimo passo a valle del circuito di conversione, prima dell'effettivo ADC.

![alt text](../img/lezione_11.md/image-1.png)

## Multiplexer
Il multiplexer è un banco di interruttori realizzati tramite dei transistori MOS che permettono di selezionare un singolo ingresso tra N, e collegarlo all'uscita.

![alt text](../img/lezione_11.md/image.png)

In un multiplexer ideale, l'unico canale in cui passa segnale è quello selezionato, tuttavia un multiplexer reale soffre di diversi errori di non linearità.

![alt text](../img/lezione_11.md/image-2.png)

L'interruttore chiuso ha una resistenza equivalente $R_{ON}$, che forma quindi un partitore con $R_S$, $R_{ON}$ e la resistenza del carico $R_L$, dunque vi è dell'attenuazione del segnale.

![alt text](../img/lezione_11.md/image-3.png)

Inoltre le uscite aperte hanno comunque delle correnti di perdita $I_{OFF}$ che percorrono $R_L // (R_{ON} + R_S$, generando una $V_{OFF}$ in uscita.

![alt text](../img/lezione_11.md/image-4.png)

Infine, le capacità parassite del carico e del multiplexer limitano la banda che può passare attraverso il multiplexer e generano un errore di offset.
## Sample Hold