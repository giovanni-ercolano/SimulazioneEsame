Ecco un esempio di README per un progetto Java che utilizza il protocollo Telnet per connettersi a un server e inviare comandi:

# Progetto Telnet per l'elenco auto

Questo progetto Java implementa un server Telnet che consente agli utenti di ottenere informazioni sull'elenco di auto. Gli utenti possono connettersi al server Telnet utilizzando l'indirizzo IP e la porta specificati.

## Come compilare e avviare il progetto

Per compilare il progetto, è necessario avere installato il JDK di Java. Dopo aver scaricato il progetto, eseguire i seguenti comandi dalla cartella principale del progetto:

```
$ javac -cp "lib/*" -d bin src/*.java
```

Questo comando compila il codice sorgente e crea una cartella "bin" contenente le classi Java.

Per avviare il server, eseguire il comando seguente dalla cartella principale del progetto:

```
$ java -cp "bin:lib/*" Server
```

Il server sarà in ascolto sulla porta 1234.

## Come connettersi al server Telnet

Per connettersi al server Telnet, utilizzare un client Telnet e specificare l'indirizzo IP della macchina in cui il server è in esecuzione e la porta 1234. Ad esempio, se il server è in esecuzione sulla macchina con l'indirizzo IP 192.168.1.100, eseguire il seguente comando da un terminale:

```
$ telnet 127.0.0.1 1234
```

## Comandi supportati

Il server Telnet supporta i seguenti comandi:

### more_expensive

Il comando `more_expensive` restituisce l'auto più costosa presente nell'elenco di auto.

Esempio di utilizzo:

```
{"command":"more_expensive"}
```

### all

Il comando `all` restituisce l'elenco completo di auto presente nell'elenco.

Esempio di utilizzo:

```
{"command":"all"}
```

### all_sorted

Il comando `all_sorted` restituisce l'elenco completo di auto ordinato per prezzo, modello, id e quantità.

Esempio di utilizzo:

```
{"command":"all_sorted"}
```

## Come interrompere il server

Per interrompere il server, premere `CTRL + C` dalla finestra del terminale in cui il server è in esecuzione.
