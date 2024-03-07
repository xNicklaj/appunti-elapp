# Lezione B1
## Moduli digitali
I moduli digitali possono essere modellizzati da un blocco che ha n ingresssi, m uscite, un pin di alimentazione ed uno di ground. 

Per rappresentare gli stati logici si utilizzano tensione **alta** per l'1 logico e tensione **bassa** per lo 0 logico. Dunque $V_L$ ha una tensione di circa 0 Volt, mentre $V_H$ ha una tensione vicina alla tensione di alimentazione.

Si usa un range di valori che determinano valore iniziale e finale degli stati per ridurre il rumore.

![Soglie](../img/img01.png)

Si può considerare come due soglie ed uno stato "cuscinetto" tra queste due soglie in cui il valore non è ben determinato.
Perché le porte funzionino correttamente è necessario che la tensione fornita in ingresso sia più grande della tensione di uscita.

![Soglie insieme](../img/img02.png)

Ovvero le ocndizioni di compatibilità sono:

- $V_{OL}$ < $V_{IL}$
- $V_{OH}$ > $V_{IH}$

La differenza $V_O - V_I$ definisce il margine di rumore:

- $NM_H = V_{OH} - V_{IH}$
- $NM_L = V_{OL} - V_{IL}$

## Struttura logica
Si può modellizare un modulo digitale in tre circuiti diversi:

- Circuito di ingresso, che verfifica lo stato logico dell'entrata
- Operatore logico, [...]
- Circuito d'uscita che generatensioni V esterne a $V_{OH}$ e $V_{OL}$.

## Moduli noti
### Inverter

Funzione logica: OUT = NOT IN