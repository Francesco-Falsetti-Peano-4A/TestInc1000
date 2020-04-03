# TestInc1000
Prima parte dell'esercizio:
Abbiamo creato una classe che estendeva un thread contenente come attributo una variabile intera statica.
Dopo aver creato il costruttore abbiamo aggiunto la funzione run, al cui interno vi era un ciclo che iterava per mille volte.
Dentro al ciclo implementavamo di uno il contatore e successivamente davamo un tempo di sospensione (sleep) di un secondo.
Nel main abbiamo istanziato due oggetti dello stesso tipo (Inc1000); dopo di che abbiamo aggiunto per ognuno dei due il metodo start().
L'output ricevuto è stato zero.
Questo perchè il main terminava prima rispetto al tempo di incrementazione della variabile statica.

Seconda parte dell'esercizio:
Uguale al primo esercizio ma con l'aggiunta del metodo join() nel main.
Come risultato abbiamo ricevuto un numero più alto compreso tra 1000 e 2000, questo perchè tramite il metodo join() i thread cercavano di non sovrapporre il valore del contatore ma con un discreto risultato.

Terza parte dell'esercizio:
A differenza della seconda parte, nella classe in cui sono presenti i due threads, l'incremento della variabile avviene in un metodo a parte, ovvero il metodo synchronized(), di tipo void e che viene chiamato all'interno del metodo run() in cui viene eseguito il codice dei due threads. synchronized ha il compito appunto di sincronizzare l'esecuzione dei due threads, la quale risorsa comune (ovvero la variabile), viene incrementata da entrambi velocemente, in modo tale da neutralizzare ogni probabilità di conflitto.
