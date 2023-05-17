# Autori

Simone Di Luna, [Gloria Segurini](https://github.com/GloriaSegurini), [Giusy Nittoli](https://github.com/Giusynit)

# Tool utilizzati

<a href="https://www.visual-paradigm.com/">
  <img src="https://cdn-images.visual-paradigm.com/media/vplogo_300.png" width="200"/>
</a>

# Introduzione al problema

Si vuole realizzare EasyRegatta, Sistema nel seguito, un sistema software di supporto agli organizzatori e ai partecipanti alle regate veliche, in particolare di regate di flotta in cui barche di dimensioni diverse gareggiano insieme, usando poi un meccanismo di compenso, basato sui ratings delle barche, per redigere la classifica.

L’Autorità Organizzatrice deve pubblicare un bando di regata che indica dove e quando l'evento si svolgerà, quali classi sono ammesse e le condizioni per partecipare. Il Sistema memorizza il bando che diventa accessibile a tutti consultando un catalogo di bandi. Il bando di regata può essere modificato, in questo caso il Sistema aggiorna il catalogo e invia una notifica a tutte le barche che si erano iscritte prima della modifica.

L’Autorità Organizzatrice deve inoltre nominare un Comitato di Regata. Il Comitato di Regata deve pubblicare le istruzioni di regata, che comprendono la definizione del sistema di compenso, e poi deve condurre la gara. Infine, il Comitato di Regata deve calcolare la classifica della regata e ha la responsabilità di esaminare e decidere le proteste (mancate precedenze, boe toccate, motori accesi…). Le decisioni comprendono “protesta invalida” oppure penalità in termini di posizione in classifica o la squalifica.

Il Sistema deve permettere l’iscrizione a barche ed equipaggio, memorizzando per ogni barca: nome, rating e numeri velici, per ogni membro dell’equipaggio: nome, numero tessera FIV, certificato medico.

Il Sistema deve gestire le comunicazioni pre-partenza in modo che le comunicazioni arrivino agli equipaggi (senza dover più usare le bandiere e i segnali acustici della Barca Comitato). Verranno mandati i seguenti segnali: Avviso, 5 minuti prima della partenza, Ultimo minuto: 1 minuto prima della partenza, Partenza.

Il Sistema deve permettere anche le comunicazioni dalle imbarcazioni verso il Comitato di Regata e verso le altre imbarcazioni per segnalare le proteste.

Il Sistema deve memorizzare i tempi di passaggio alle boe (al solo fine informativo per valutare le prestazioni delle barche) e all’arrivo (per stilare la classifica finale) e supportare il Comitato di Regata per calcolare la classifica tenendo conto dei rating delle imbarcazioni.

I passaggi in boa vengono comunicati dagli equipaggi, assieme ai numeri velici della barca che precede e della barca che segue, ove possibile. Il tempo all’arrivo è preso invece dall’equipaggio della Barca Comitato.

Ogni regata ha un tempo limite deciso dal Comitato di Regata. Le imbarcazioni che non arriveranno entro il tempo limite saranno considerate “non arrivate”. E’ possibile (decisione del Comitato di Regata) tenere conto del tempo di passaggio a una data boa per la classifica delle barche che arrivano oltre tempo limite. Le imbarcazioni che sono passate dalla boa indicata e che non hanno tagliato la linea di arrivo entro il tempo limite, saranno comunque poste in classifica in coda all'ultimo arrivato, in base all’ordine (compensato) di passaggio alla boa. In tal caso ci sarà una Barca Comitato anche in pressi della boa per prendere i tempi.

Le proteste dovranno essere inserite entro 60 minuti dall’arrivo dell’imbarcazione protestante.

Una barca che si ritira dovrà darne comunicazione al più presto, tranne che in una situazione di emergenza.

Una barca che non parta entro 30 minuti dal proprio segnale di partenza sarà classificata “Non Partita” senza possibilità di protesta.

# Scopo del progetto

Si integrano i requisiti già specificati con le seguenti ulteriori informazioni:
* La base di dati deve tenere traccia di tutte le persone (nominativi, recapiti,...), equipaggi e comitati;
* Si faccia particolare attenzione alla gestione del Comitato e del processo di comunicazioni/proteste.

Questa descrizione è volutamente incompleta e aperta a diversa interpretazione.

# Requisiti progetto

1. Descrizione precisa del dominio del discorso.
2. Produzione di uno schema concettuale a oggetti in formato grafico dettagliato.
3. Produzione di uno schema logico relazionale sia in formato grafico che testuale.
4. Generare almeno sei query SQL che abbiano, rispettivamente, le seguenti caratteristiche:
    - uso di proiezione, join e restrizione;
    - uso di group by con having, where e sort;
    - uso di join, group by con having e where;
    - uso di select annidata con quantificazione esistenziale;
    - uso di select annidata con quantificazione universale;
    - uso di subquery di confronto quantificato usando una subquery.
5. Definire i piani di accesso delle query al punto precedente:
    - Scrivere un piano di accesso logico delle prime tre query del punto precedente
    - Scrivere un piano di accesso fisico efficiente per i suddetti tre piani di accesso logico che non fanno uso di indici, e (opzionale) verificare se la sort prima della Group By può essere evitata.
    - Scrivere un piano di accesso fisico efficiente per i tre suddeti piani di accesso logico che fanno uso di due indici (o comunque del numero massimo di indici possibili), e (opzionale) verificare se la sort prima della Group By può essere evitata.


