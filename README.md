# template-tesi
Template LaTeX estremamente minimale e altamente personalizzabile, che ho usato per scrivere la mia Tesi di Laurea Magistrale presso l'Università Politecnica delle Marche.

Siccome non riuscivo a trovare un template online che mi soddisfacesse abbastanza a livello estetico senza doverlo stravolgere, mi sono detto che tanto valeva farmelo da me. Basato sulla classe standard `book`: niente classi aggiuntive con documentazioni da imparare, e le uniche dipendenze sono i pacchetti che ho usato per modificarla a mio gusto personale. È disponibile un [PDF di esempio](https://github.com/fp555/template-tesi/raw/master/esempio.pdf) come anteprima del template.

## Utilizzo
Il template consiste nel file [tesi.tex](https://github.com/fp555/template-tesi/blob/master/tesi.tex), al cui interno vengono inclusi i file delle singole parti/capitoli contenuti nella cartella `content/`, semplificando la stesura e la gestione della tesi. La cartella `figure/` dovrebbe invece contenere tutte le immagini da inserire nel documento. La struttura della tesi è quindi la seguente:
- *Front matter* con frontespizio, indice (generato automaticamente), sommario e ringraziamenti. Se necessario si possono aggiungere (facendole generare automaticamente da LaTeX) anche le liste delle figure/tabelle/equazioni;
- *Main matter*, ovvero la serie dei capitoli e appendici numerate;
- *Back matter* con la bibliografia (generata automaticamente) ed eventualmente un glossario.

Ovviamente non siete obbligati a seguire questo schema, e potete cambiarlo come vi pare (la tesi è la vostra).

### Nota: frontespizio
La mia università non impone restrizioni particolari sul layout del frontespizio: ho potuto quindi decidere posizione, grandezza e carattere di tutti gli elementi sostanzialmente a mio gusto. Assicuratevi che la vostra università non imponga un formato specifico prima di usare il mio (o di modificarvelo per conto vostro).

### Nota: bibliografia
Il file [tesi.bib](https://github.com/fp555/template-tesi/blob/master/tesi.bib) è il "database" delle fonti bibliografiche del documento (con relativa chiave di citazione per LaTeX), da riempire secondo la [sintassi di `biber`](http://ctan.org/tex-archive/macros/latex/exptl/biblatex/doc/biblatex.pdf). Se non usate un IDE per LaTeX dovrete inoltre ridefinire opportunamente il comando per compilare il sorgente e generare il PDF.

## Personalizzazioni
Un rapido elenco delle personalizzazioni da me implementate:
- la tesi è impaginata per la stampa *fronte-retro*; per impostare solo fronte occorre dare l'opzione `oneside` [qui](https://github.com/fp555/template-tesi/blob/master/tesi.tex#L1);
- il font è *Latin Modern* a dimensione 12;
- il documento è impostato come multilingua italiano-inglese. Per mandare correttamente a capo le parole in inglese occorre racchiuderle all'interno della macro `\eng{}` (o `\eeng{}` per dare il corsivo); per le citazioni in bibliografia basta [specificare la lingua della fonte](https://github.com/fp555/template-tesi/blob/master/tesi.bib#L9);
- i riferimenti bibliografici nel testo appaiono tra parentesi quadre come numeri, secondo l'ordine alfabetico degli autori;
- i numeri di pagina sono in basso al centro; il *front matter* ha anche le testatine in alto e le *marche* personalizzate, ad eccezione della prima pagina di ciascun capitolo e delle pagine vuote;
- i capitoli iniziano sempre in una pagina dispari, aggiungendo dove serve una pagina vuota;
- i titoli dei capitoli hanno uno stile simile a quello della classe `article`;
- i paragrafi sono spaziati, senza indentazione sulla prima riga;
- gli elenchi puntati e numerati occupano molto meno spazio nella pagina;
- l'indice non ha i punti tra i titoli dei capitoli/sezioni e il numero di pagina;
- le figure hanno la didascalia centrata rispetto alla pagina.

A quanto pare, scrivere un template è il modo migliore di diventare pratici di LaTeX :wink:
