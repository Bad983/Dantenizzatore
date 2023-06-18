# DANTENIZZATORE

## Modello di traduzione linguistica su architettura Transformer: riuscire a tradurre in Dantesco 

L’idea era quella di portare al PyCon un argomento che coinvolgesse tutta la città di Firenze e da qui è nata l’idea di pensare ad un modello di Intelligenza Artificiale che effettuasse traduzioni dall’Italiano alla lingua Dantesca (il volgare fiorentino del 1300). E' stata intrapresa una sfida importante e sono state utilizzate tecnologie avanzate per creare un sistema di traduzione automatica che possa (speriamo!) aiutare gli studiosi e gli appassionati della letteratura a comprendere meglio le opere di Dante, oppure, perché no, a tradurre parole dei giorni nostri nella lingua del 1300.

Il progetto ha rivelato grosse sfide fin dall’inizio, per questo abbiamo suddiviso le attività in due macro-fasi:
  - <b>Data Preparation</b>
  - <b>Modello Transformer</b>

### DATA PREPARATION

La data preparation è una disciplina che consente di acquisire, combinare e organizzare i dati per renderli fruibili per la loro analisi. Risulta assolutamente cruciale per garantire una qualità dei dati che consenta di estrarre un adeguato valore informativo dai dati. Di seguito tutte le fasi percorse:
1.	<b>Data Discovery:</b>
Trovare le opere di Dante è stato semplice, questo invece non si può dire per le relative parafrasi. È iniziata una ricerca per reperire in rete queste informazioni che potessero aiutare nella creazione di un modello linguistico basato su tecnologia Transformer. Una volta identificati i siti internet abbiamo utilizzato una combinazione di tecniche di scraping e di elaborazione del linguaggio naturale per raccogliere i dati necessari ad addestrare i nostri modelli. Abbiamo riscontrato parecchie difficoltà nell'acquisizione dei dati a causa di problemi di formattazione.
2.	<b>Data Cleaning:</b>
Il problema successivo è stato la qualità delle informazioni scaricate. Analizzando i dati si è riscontrata spesso una bassa qualità nella traduzione in quanto spesso le informazioni trovate erano più vicine ad una parafrasi commentata rispetto ad una traduzione della frase o del versetto. Da qui la necessità di migliorare la qualità dei dati per ottenere dei risultati. In prima battuta sono state adottate tecniche di pulizia del dataset in modo da renderlo il più utilizzabile possibile, successivamente abbiamo controllato manualmente i dati riga per riga per garantire che fossero adatti ai nostri modelli.
3.	<b>Data Transformation:</b>
Questa fase ha avuto l’obiettivo di rendere il dataset perfettamente compatibile con le tecnologie delle applicazioni utilizzate per la loro elaborazione. Ha quindi previsto una modellazione, strutturazione e organizzazione del dataset che ci potesse garantire una qualità superiore in base anche a determinate scelte effettuate per il modello Transformer. Abbiamo quindi deciso di organizzare le frasi, sia delle opere che delle traduzioni, secondo una determinata struttura che ci consentisse una possibile traduzione senza aumentare la complessità del modello.
4.	<b>Data Augmentation:</b>
In questa fase il focus è stato sulla quantità dei dati, i dati a disposizione erano troppo pochi. Con l’ausilio di modelli di Intelligenza Artificiale a disposizione di tutti, come ChatGPT, oppure attraverso la creazione di script che facessero uso dei modelli Transformer di Hugging-Face abbiamo tradotto i dati a nostra disposizione in lingue diverse come inglese, francese, spagnolo, tedesco.
5.	<b>Data Validation:</b>
Infine l’ultima fase dove è stato validato il dataset a disposizione consentendo la predisposizione di un primo modello di traduzione linguistica.

### <b>MODELLO TRANSFORMER</b>

Per questo task specifico abbiamo scelto di adottare un modello di Intelligenza artificiale che facesse uso della tecnologia Transformer. Un Transformer è una particolare struttura di rete neurale artificiale particolarmente utile nel Natural Language Processing, in quanto pone la giusta attenzione (Attention Is All You Need) identificando le parti importanti delle sequenze di frasi a nostra disposizione. 
Sapevamo che l’obiettivo da raggiungere era alto e la potenza computazionale necessaria per addestrare un’architettura del genere è davvero importante. Abbiamo quindi deciso di provare ad innestare nel modello, al posto del blocco di Encoder, il modello pre-addestrato di <b>BERT</b> in modo che potesse consentire di dare una corretta e profonda visione di tutti dati di input. 
