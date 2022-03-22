# 2 - Unità di calcolo
## 2.1. - Generalità
Tutti i sistemi hanno bisogno di unità di calcolo, ovvero unità capaci di svolgere calcoli per compiere operazioni di varia natura, tra cui: operazioni *aritmetiche*, operazioni *logiche*, spostamenti tra *zone di memoria*, *comunicazione* con altri dispositivi.
In generale, la capacità di calcolo delle varie unità (insieme ad altre grandezze come la dimensione della memoria e le relative velocità) rappresenta un limite stretto a ciò che il sistema può fare. Infatti, una macchina con poca memoria non potrà contenere più dati di quelli consentiti, per cui non potrà svolgere operazioni che coinvolgono dati di grandi dimensioni. Allo stesso modo, una macchina con unità di calcolo lente impiegherà *molto* tempo per effettuare alcune operazioni complesse.
Il limite sulla potenza di calcolo dei sistemi è stato affrontato andando a migliorare le strutture ed il funzionamento delle unità di calcolo, infatti sono presenti, ad oggi, diversi tipi di unità di calcolo, ognuna con i suoi pregi e difetti e settori di interesse.
Di seguito si esaminano tre tipi di unità di calcolo diverse.

## 2.2. - Central Processing Unit (CPU)
La CPU è un'unità di calcolo alla base del funzionamento delle macchine, in quanto essa è ciò che ne governa il funzionamento, eseguendo delle **istruzioni**, ovvero delle direttive che codificano le operazioni eseguibili, espresse in sequenza per realizzare quello che è chiamato **programma**. 
In generale le CPU recenti sono realizzate attraverso processori, che ne integrano tutte le funzionalità in un unico circuito integrato, e sono strutturate secondo due tipi di architetture che differiscono tra loro nella divisione dei tipi di memoria: 
- **Architettura di Von Neumann**: la memoria è omogenea, in quanto contiene sia istruzioni che dati;
- **Architettura Harvard**: la memoria è eterogenea, in quanto le istruzioni sono separate dai dati (tipicamente attraverso due memorie separate che possono lavorare in parallelo, rendendo possibile un incremento delle prestazioni);

Per quanto riguarda i microprocessori, invece, si hanno in generale due tipologie di architettura, spesso ibridate in un'architettura che presenti caratteristiche da entrambe in modo da colmarne alcuni difetti:
- Architettura Reduced Instruction Set Computer (**RISC**), caratterizzata da poche istruzioni semplici di lunghezza fissa, di solito con un alto numero di **registri** (zone di memoria ad alta velocità riservate e contenute nel processore) e che mira, quindi, all'elevata parallelizzazione;
- Architettura Complex Instruction Set Computer (**CISC**), caratterizzata da molte istruzioni di varia natura (possono avere lunghezze diverse tra loro e svolgere operazioni più complesse), con un minor numero di registri e che mira ad un'elevata velocità di esecuzione delle singole istruzioni ed alla semplificazione del lavoro dei compilatori (in quanto molte più operazioni sono codificate direttamente da istruzioni);

La CPU è un unità di calcolo in generale predisposta ad un approccio sequenziale alle istruzioni (anche considerando il parallelismo dato dalla presenza di più processori), in quanto cerca di ottimizzarne l'esecuzione sequenziale attraverso alcune tecniche (tra cui **pipelining** e  **branch prediction**).
Altri tipi di unità di calcolo sono stati sviluppati per l'esecuzione parallela delle istruzioni, come le GPU e le TPU.

## 2.3 - Graphics Processing Unit (GPU)
La GPU è un unità di calcolo creata (all'inizio) per svolgere elaborazione grafica, ma in generale ora è usata per molte altre applicazioni in cui è richiesto un elevato grado di parallelismo, vista la sua struttura ed i suoi punti di forza.

L'elaborazione grafica (come le altre applicazioni), infatti, necessita di tante "piccole" (rispetto ad un programma *"classico"*) operazioni, da eseguire in parallelo per ottenere un'uscita in tempi ottimi, come la gestione del colore dei singoli pixel che andranno a comporre un'immagine da mostrare su schermo (**frame**) o la trasformazione di coordinate di vertici da spazi tridimensionali (o quadridimensionali) in uno spazio bidimensionale (**proiezione**, che corrisponde anche all'operazione naturalmente svolta dai nostri occhi sulle informazioni provenienti dal mondo esterno), o molto altro (corrispondono ai passaggi di quella che è una pipeline grafica, ovvero diversi stadi attraverso il quale passano i dati che andranno poi a generare il frame finale).

Altre applicazioni delle GPU sono rappresentate dal calcolo per il ML, in cui occorre processare in parallelo grandi quantità di dati per ottenere una rete capace di apprendere informazioni da essi o il mining di criptovalute, in cui occorre mettere a disposizione la potenza di calcolo dei propri dispositivi per effettuare calcoli di natura crittografica (in generale molto pesanti).

La GPU è trattata più in dettaglio in [GPU](link).

## 2.4. - Tensor Processing Unit (TPU):
La TPU è un nuovo tipo di unità di calcolo derivata dalle necessità di operazioni più performanti in quanto a complessità, al livello delle istruzioni, rispetto a quel che è richiesto nel campo del ML.
Essa è un [ASIC](https://it.wikipedia.org/wiki/Application_specific_integrated_circuit) (Application Specific Integrated Circuit), ovvero un circuito creato appositamente per svolgere alcune operazioni, il che la rende più performante rispetto ad altre unità di calcolo *general purpose* (ovvero per calcolo generico). La necessità della sua introduzione è data dalla complessità intrinseca delle operazioni di apprendimento degli algoritmi di ML (prevalentemente prodotti matriciali, che rimangono operazioni di complessità superiore per via della loro particolarità).

Le TPU sono state sviluppate da Google per funzionare esclusivamente con la libreria Tensorflow, per cui altre soluzioni sono necessarie in caso si desideri utilizzare librerie diverse.

Una descrizione di alcune caratteristiche hardware della TPU è disponibile in [TPU](link)

