# DANTENIZZATORE

## Modello di traduzione linguistica su architettura Transformer: riuscire a tradurre in Dantesco 

L’idea era quella di portare al PyCon un argomento che coinvolgesse tutta la città di Firenze e da qui è nata l’idea di pensare ad un modello di Intelligenza Artificiale che effettuasse traduzioni dall’ Italiano alla lingua di Dante (il volgare fiorentino del 1300). Abbiamo intrapreso una sfida importante e utilizzato queste tecnologie avanzate per creare un sistema di traduzione automatica che possa (speriamo!) aiutare gli studiosi e gli appassionati della letteratura a comprendere meglio le opere di Dante, oppure, perché no, a tradurre parole dei giorni nostri nella lingua del 1300.
Il progetto ha rivelato grosse sfide fin dall’inizio, per questo abbiamo suddiviso le attività in due macro-fasi:
●	Data Preparation
●	Modello Transformer

### DATA PREPARATION
La data preparation è una disciplina che consente di acquisire, combinare e organizzare i dati per renderli fruibili per la loro analisi. La data preparation risulta assolutamente cruciale per garantire una qualità dei dati che consenta di estrarre un adeguato valore informativo dai dati. Abbiamo quindi ripercorso tutte le fasi della data preparation:
1.	Data Discovery
Trovare le opere di Dante è stato semplice, questo invece non si può dire per le relative parafrasi. È iniziata una ricerca per reperire in rete queste informazioni che potessero aiutarci nella creazione di un modello linguistico basato su tecnologia Transformer. Una volta identificati i siti internet abbiamo utilizzato una combinazione di tecniche di scraping e di elaborazione del linguaggio naturale per raccogliere i dati necessari ad addestrare i nostri modelli. Abbiamo riscontrato parecchie difficoltà nell'acquisizione dei dati a causa di problemi di formattazione.
2.	Data Cleaning
Il problema successivo è stato la qualità delle informazioni scaricate. Analizzando i dati abbiamo riscontrato spesso una bassa qualità nella traduzione in quanto spesso le informazioni trovate erano più vicine ad una parafrasi commentata rispetto ad una traduzione della frase o del versetto. Questo ci ha fatto capire che dovevamo necessariamente migliorare la qualità dei dati per provare ad ottenere dei risultati. In prima battuta sono state adottate tecniche di pulizia del dataset in modo da renderlo il più utilizzabile possibile, successivamente abbiamo controllato manualmente i dati riga per riga per garantire che fossero adatti ai nostri modelli.
3.	Data Transformation
Questa fase ha l’obiettivo di rendere il dataset perfettamente compatibile con le tecnologie delle applicazioni utilizzate per la loro elaborazione. Ha quindi previsto una modellazione, strutturazione e organizzazione del dataset che ci potesse garantire una qualità superiore in base anche a determinate scelte effettuate per il modello Transformer. Abbiamo quindi deciso di organizzare le frasi, sia delle opere che delle traduzioni, secondo una determinata struttura che ci consentisse una possibile traduzione senza aumentare la complessità del modello.
4.	Data Augmentation
In questa fase ci siamo concentrati sulla quantità dei dati, in quanto ci siamo resi conto che i dati a nostra disposizione fossero troppo pochi; ed è qui che ci siamo concentrati per questa fase. Siamo partiti avvalendoci di tecniche di data augmentation per la generazione di dati che potessero in un qualche modo aumentare le traduzioni a nostra disposizione generando ad esempio sinonimi dei vocaboli utilizzati. Successivamente con l’aiuto di modelli di Intelligenza Artificiale a disposizione di tutti come ChatGPT oppure attraverso la creazione di script che facessero uso dei modelli Transformer di Hugging-Face abbiamo tradotto i dati a nostra disposizione in lingue diverse come inglese, francese, spagnolo, tedesco.
5.	Data Validation
Siamo poi passati all’ultima fase dove abbiamo validato il dataset a nostra disposizione e questo ci ha consentito di incominciare a predisporre un primo modello di traduzione linguistica.

### MODELLO TRANSFORMER
Per questo task specifico abbiamo scelto di adottare un modello di Intelligenza artificiale che facesse uso della tecnologia Transformer. Un Transformer è una particolare struttura di rete neurale artificiale particolarmente utile nel Natural Language Processing, in quanto pone la giusta attenzione (Attention Is All You Need) identificando le parti importanti delle sequenze di frasi a nostra disposizione. 
Sapevamo che l’obiettivo da raggiungere era alto e la potenza computazionale necessaria per addestrare un’architettura del genere è davvero importante. Abbiamo quindi deciso di provare ad innestare nel nostro Transformer, al posto del layer di Encoder, il modello pre-addestrato di BERT in modo che ci potesse consentire di dare una corretta e profonda visione di tutti dati di input. 
