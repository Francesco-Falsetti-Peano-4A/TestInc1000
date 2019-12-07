# TestInc1000
Prima parte dell'esercizio:
Abbiamo creato una classe che estendeva un thread contenente come attributo una variabile intera statica.
Dopo aver creato il costruttore abbiamo aggiunto la funzione run, al cui interno vi era un ciclo che iterava per mille volte.
Dentro al ciclo implementavamo di uno il contatore e successivamente davamo un tempo di sospensione (sleep) di un secondo.
Nel main abbiamo istanziato due oggetti dello stesso tipo (Inc1000); dopo di che abbiamo aggiunto per ognuno dei due il metodo start().
L'output ricevuto è stato zero.
Questo perchè avendo una variabile comune (statica), i due oggetti sovrascrivevano il valore della variabile statica senza mai incrementare il contatore.

Seconda parte dell'esercizio:
Uguale al primo esercizio ma con l'aggiunta del metodo join() nel main.
Come risultato abbiamo ricevuto un numero più alto compreso tra 1000 e 2000, questo perchè tramite il metodo join() i thread cercavano di non sovrapporre il valore del contatore ma con un discreto risultato.

Terza parte dell'esercizio:
Come ultimo cambiamento in modo tale da far funzionare correttamente il programma, oltre ad aver messo prima il metodo start() e poi il metodo join(), abbiamo cambiato il codice all'interno del ciclio della funzione run():
Abbiamo chiamato una fuzione di nome inc1 che incrementava il contatore.
Tutto questo per far lavorare i due thread in modo parallelo ma senza sovrascrivere il valore del contatore.
Il risultato è stato di 2000.
