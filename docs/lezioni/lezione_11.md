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
Il circuito di Sample-Hold è il circuito più a valle possibile. Si occupa di campionare un ingresso che varia costantemente nel tempo e mantenere l'uscita per un tempo $t \ge t_H$.

La prima parte del Sample-Hold è un circuito di amplificazione unitario, in quanto l'uscita dev'essere pari all'ingresso.

In un SH ideale, il campionamento istantaneo avviene in un tempo infinitesimo, tuttavia in un SH reale si ha :

- un **tempo di apertura**, ovvero il tempo che intercorre tra la ricezione del comando di sample e l'apertura dell'interruttore 
- un **tempo di assetto**, ovvero il tempo che impiega il segnale ad assestarsi su suo valore reale. Questo perché quando viene chiuso il circuito di ricezione del segnale, il passaggio da alta impedenza a circuito chiuso fa rialzare il segnale più del dovuto per un fenomeno detto **Jitter** di campionamento.

![alt text](../img/lezione_11.md/image-5.png)

Come in precedenza, essendo il Jitter un rumore si può valutare il **Signal-To-Noise-Ratio** come $SNR_J = \frac{\sigma_A^2}{\sigma_J^2}$.

Una volta catturato il segnale, questo è prono a fenomeni di **decadimento**, ovvero diminuzione del segnale nel tempo e **feedthrough**, se l'ingresso è schermato male e quindi una minima parte delle variazioni va ad influire sull'uscita.

![alt text](../img/lezione_11.md/image-6.png)