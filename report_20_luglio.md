# Voice Math - Riunione 20 Luglio 2021

## Riassunto
La riunione di oggi riguarda principalmente l'interfaccia del programma VoiceMath.

Viene illustrata l'interfaccia grafica: in linea di principio, deve essere possibile caricare un video;
di tale video viene fatta una trascrizione automatica ( con il modello basato su motore di trascrizione Nuance Transcription Engine, NTE).
Tale trascrizione sarà sottoposta a classificazione e scritta in una textbox in maniera che:
1. L'utente possa modificare la trascrizione.
2. Sia possibile distinguere nel testo le porzioni automaticamente classificate come formule dal testo discorsivo.
3. Sia possibile fare click su Export per ottenere il testo corretto, modificato e integrato di formule in un file.

È anche possibile l'inserimento di immagini, che subiscono un diverso processamento:
ignorando il parlato, le immagini vengono processate da MathPix che ne estrae le formule e le traduce in formato LaTeX.
Stesso processamento MathPix: è possibile effettuarlo su immagine estratta dal video; in linea di principio èidentico, essendo processamento di immagine;
in pratica, si richiede che l'utente indichi l'intervallo di tempo, identificato da  (timestamp inizio, timestamp fine) in cui è possibile identificare la formula.

L'interazione tra le varie componenti è abbastanza complessa: a sinistra viene mostrato un testo, che è risultato delle fasi di riconoscimento vocale e di classificazione del discorso in "formula"/"testo senza formula";
a destra c'è la parte di formule provenienti dal video e/o dalle immagini; quindi ci si aspetta che sia possibile prendere le "formule video" e inserirle nel "testo della voce".

L'interazione che ci si aspetta, repetita iuvant, è complessa.
La diapositiva però contiene una schematizzazione abbastanza scarna di come sarà il programma:
il mockup presentato contiene dei rettangoli pressocché vuoti o con all'interno un lorem ipsum e nessuna formula.

## Interventi
Riporto in basso in maniera sintetica alcuni interventi che abbiamo fatto:

**Compatibilità con Axessibility**: Anna e Sandro indicano il formato Latex e l'uso del package Axessibility integrato nella trascrizione del testo.

**Davide**: È possibile fare il mockup con degli esempi veri? Un testo vero - anche molto semplice - ma con formule vere, relativa trasformazione in Latex, immagini e acquisizione immagini? Sarebbe utile anche come manuale operativo per l'utente.

**Tiziana**: Sarebbe utile riascoltare pezzi di video dall'interno dell'interfaccia per individuare gli intervalli di tempo in cui compaiono formule:
aiuterebbe l'umano che fa da correttore.

**Carola**: come inserire i timestamp? Carola propone un meccanismo simile ai video di YouTube, in cui c'è un file di sottotitoli che contiene la trascrizione e l'intervallo di tempo in cui vale la trascrizione.

**Adriano**: Si potrebbe fare in modo che allo scorrere del video, il cursore del testo voce si sposti in base a ciò che viene detto nel video. 

**Francesco** risponde che: i timestamp ci sono a livello di parola(quindi per ogni parola sappiamo quando la voce inizia e finisce di pronunciarla); bisogna decidere come presentarli. Si può provare a inserire il timestamp nei commenti latex.

**Adriano propone MathJax** come formato di esportazione.

**Francesco: Utente**: che tipo di utente è ? Professore, studente, altro?

**Maria Luisa**: chiede specifiche su MathJax; inoltre chiede indicazioni su come rendere accessibile il sito.
Si sollevano un po' di perplessità sulla parola **"sito"**; le diapositive precedenti non lo dicono, ma l'elaborazione è fornita come "web application" e non come programma client-desktop.

**Da inviare a CELI**: specifiche per l'esportazione in formato HTML/MathJax.

**Prossimo incontro**:  Mercoledì 28 ore 15, (Settimana prossima) per parlare dei modelli
