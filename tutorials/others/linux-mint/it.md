---
name: Linux Mint

description: Configurare un computer per le transazioni Bitcoin
---

![image](assets/cover.jpeg)

## Cosa succede se si utilizza un computer normale?

Quando si effettuano transazioni Bitcoin, è ideale che il computer non abbia malware. Ovviamente.

Se si tiene la frase di recupero del Bitcoin (di solito composta da 12 o 24 parole) lontana dal computer con un dispositivo di firma (ad esempio un portafoglio hardware - il suo scopo principale), potresti pensare che non sia così importante avere un computer "pulito" - ma non è vero.

Un computer infestato da malware potrebbe leggere i tuoi indirizzi Bitcoin, esponendo il tuo saldo a un attaccante: non possono rubare bitcoin solo conoscendo l'indirizzo, ma possono vedere quanto possiedi e calcolare se sei un obiettivo degno di interesse. Potrebbero anche scoprire dove vivi, ad esempio, ed estorcere denaro o minacciare i tuoi cari per farti pagare un riscatto.

## Qual è la soluzione?

Incoraggio la maggior parte dei Bitcoiner a utilizzare un computer dedicato privo di malware (con accesso a Internet) per effettuare transazioni Bitcoin. Suggerisco alle persone di utilizzare un sistema operativo open-source come Linux Mint, ma se è necessario, è meglio utilizzare Windows o Mac rispetto a un computer normale e molto utilizzato che inevitabilmente contiene malware nascosto.

Un ostacolo che le persone incontrano è l'installazione di un nuovo sistema operativo su tali computer. Questa guida è stata creata per aiutare in tal senso.

Esistono molte varianti di Linux e ne ho provate diverse. La mia raccomandazione per i Bitcoiner è Linux Mint, perché è facile da installare, molto veloce (soprattutto all'avvio e allo spegnimento), non è appesantito (ogni software aggiuntivo rappresenta un rischio) e raramente si è bloccato o ha avuto comportamenti strani (rispetto ad altre versioni come Ubuntu e Debian).

Alcuni possono essere molto restii a un nuovo sistema operativo, preferendo Windows o Mac OS. Capisco, ma i sistemi operativi Windows e Apple sono closed source, quindi dobbiamo fidarci di ciò che fanno; non penso che sia una buona politica, ma non è tutto o niente. Preferirei molto di più che le persone utilizzino un computer Windows o Mac OS appena installato e dedicato piuttosto che un computer molto utilizzato (con chissà quali malware accumulati). Un passo avanti è utilizzare un computer Linux appena installato, che è ciò che dimostrerò.

Se sei nervoso nell'utilizzare Linux a causa dell'ignoto, è naturale, ma lo è anche dedicare del tempo per imparare. Sono disponibili molte informazioni online. Ecco un eccellente breve video che introduce le basi della riga di comando che consiglio vivamente.
Scegli un computer

Inizierò con ciò che penso sia la migliore opzione. Poi darò la mia opinione sulle alternative.

Opzione ideale:

La mia raccomandazione, se te lo puoi permettere e se le dimensioni del tuo stack di bitcoin lo giustificano, è acquistare un nuovo laptop di fascia entry-level. Il modello più semplice costruito in questi giorni è abbastanza buono per gestire ciò per cui verrà utilizzato. Le specifiche del processore e della RAM non sono rilevanti, perché saranno tutte sufficienti.

Da evitare:

- Qualsiasi combinazione di tablet, inclusi Surface Pro
- Chromebook - spesso la capacità di archiviazione è troppo bassa
- Qualsiasi computer con un'unità eMMC; se ha un'unità SSD, è perfetto
- Mac - sono costosi e l'hardware non si adatta bene ai sistemi operativi Linux secondo la mia esperienza
- Qualsiasi cosa ricondizionata o di seconda mano (anche se non è un fattore decisivo assoluto)
  Invece, cerca un laptop con Windows 11 (Attualmente Windows 11 è l'ultima versione. Ci libereremo di quel software, non preoccuparti.). Ho cercato su amazon.com "Windows 11 Laptop" e ho trovato questo buon esempio:
  ![image](assets/1.webp)

Il prezzo di questo sopra è buono. Le specifiche sono abbastanza buone. Ha una fotocamera integrata che possiamo usare per le transazioni QR code PSBT (altrimenti dovresti comprare una fotocamera USB per farlo). Non preoccuparti del fatto che non sia un marchio ben riconosciuto (è economico). Se vuoi un marchio migliore, ti costerà, ad esempio:

![image](assets/2.webp)

Alcuni dei più economici hanno solo 64Gb di spazio di archiviazione; non ho testato laptop con unità così piccole - probabilmente va bene avere 64Gb, ma potrebbe essere un po' al limite.

## Altre opzioni - Tails

Tails è un sistema operativo che si avvia da una chiavetta USB e temporaneamente prende il controllo dell'hardware di qualsiasi computer. Utilizza solo connessioni Tor, quindi è necessario essere a proprio agio nell'usare Tor. Nessuno dei dati che scrivi nella memoria durante la sessione viene salvato sull'unità (parte sempre da zero ogni volta) a meno che tu non modifichi le impostazioni e crei un'opzione di archiviazione permanente (sulla chiavetta USB) - che blocchi con una password.

Non è una cattiva opzione ed è gratuita, ma è un po' scomoda per il nostro scopo. Installare nuovi software su di essa non è semplice. Una buona caratteristica è che viene fornito con Electrum, ma il lato negativo è che non l'hai installato tu stesso. Assicurati che la chiavetta USB che utilizzi abbia almeno 8Gb.

La tua flessibilità è ridotta se usi Tails. Potresti non essere in grado di seguire varie guide per configurare ciò di cui hai bisogno e farlo funzionare correttamente. Ad esempio, se segui la mia guida per l'installazione di Bitcoin Core, sono necessarie modifiche per farlo funzionare. Non penso di fare una guida specifica per Tails, quindi dovrai sviluppare le tue competenze e farlo da solo.

Non sono nemmeno sicuro di come interagiranno i portafogli hardware con questo sistema operativo.

Detto tutto ciò, un computer con Tails per le transazioni Bitcoin è una bella opzione aggiuntiva e sicuramente aiuterà le tue competenze complessive di privacy imparando ad usare Tails.

## Altre opzioni - Avvio di un sistema operativo live

Questo è molto simile a Tails, tranne che il sistema operativo non è dedicato alla privacy. Il modo di base per utilizzarlo è quello di copiare un'unità USB con il sistema operativo Linux a tua scelta e far avviare il computer da quella invece che dall'unità interna. Come fare ciò verrà spiegato in seguito.

Il vantaggio è che sei meno vincolato e le cose funzioneranno senza modifiche avanzate.

Non sono sicuro di quanto bene un tale sistema isola il malware presente sul computer esistente dalla chiavetta USB di avvio che contiene il nuovo sistema operativo. Probabilmente fa un buon lavoro e probabilmente non è così buono come Tails. Poiché non lo so, la mia preferenza è il laptop dedicato.
Altre opzioni - Il tuo laptop o computer desktop usato

Utilizzare un computer usato non è l'ideale, principalmente perché non conosco il funzionamento interno del malware sofisticato, né se cancellare un'unità sia sufficiente per eliminarlo. Probabilmente lo è, ma non voglio sottovalutare quanto intelligenti possono essere gli hacker malintenzionati. Puoi decidere, non voglio impegnarmi.
Se scegli di utilizzare un vecchio desktop invece di un vecchio laptop, va bene, tranne che occuperà permanentemente spazio per le tue transazioni di bitcoin probabilmente rare; non dovresti usarlo per nient'altro. Mentre con un laptop, puoi semplicemente metterlo via e persino nasconderlo per una sicurezza extra.

## Installazione di Linux Mint su qualsiasi computer

Queste sono istruzioni per cancellare qualsiasi sistema operativo dal tuo nuovo laptop e installare Linux Mint, ma puoi adattarle per installare praticamente qualsiasi versione di Linux su qualsiasi computer.

Stiamo per utilizzare qualsiasi computer per trasferire il sistema operativo su una chiavetta di memoria di qualche tipo. Non importa quale chiavetta di memoria, purché sia compatibile con una porta USB, e suggerisco almeno 16 GB.

Prendi una di queste cose:

![image](assets/3.webp)

Oppure puoi usare qualcosa del genere:

![image](assets/4.webp)

Successivamente, vai su linuxmint.com

![image](assets/5.webp)

Posiziona il mouse sopra il menu Download in alto e poi clicca sul link "Linux Mint 20.3" o qualunque versione sia quella raccomandata più recente al momento in cui fai questo.

![image](assets/6.webp)

Ci saranno alcuni "flavors" tra cui scegliere. Scegli "Cinnamon" per seguire questa guida. Clicca sul pulsante Download.

![image](assets/7.webp)

Nella pagina successiva, puoi scorrere verso il basso per vedere i mirror (i mirror sono vari server che contengono una copia del file che vogliamo). Puoi verificare il download utilizzando SHA256 e gpg (raccomandato), ma salterò spiegazioni su questo in quanto ho già scritto delle guide a riguardo.

![image](assets/8.webp)

Scegli un mirror che sia più vicino a te e clicca sul suo link (il testo verde nella colonna mirror). Il file inizierà a scaricarsi - la versione che sto scaricando è di 2,1 gigabyte.

Una volta scaricato, puoi trasferire il file su un dispositivo di memoria portatile e renderlo avviabile. Per farlo, il modo più semplice è utilizzare Balena Etcher. Scaricalo e installalo se non lo hai.

Poi avvialo:

![image](assets/9.webp)

Clicca su "flash from file" e seleziona il file LinuxMint che hai scaricato.

Poi clicca su "Select target". Assicurati che il dispositivo di memoria sia collegato e assicurati di selezionare il drive corretto, altrimenti potresti distruggere i contenuti del drive sbagliato!

Dopo di che, seleziona "Flash!" Potrebbe essere necessario inserire la tua password. Quando è completato, il drive probabilmente non sarà leggibile dal tuo computer Windows o Mac perché è stato trasformato in un dispositivo Linux. Basta tirarlo fuori.
Preparazione del computer di destinazione

Accendi il nuovo laptop e, mentre si accende, tieni premuto il tasto del BIOS. Di solito è F2, ma potrebbe essere F1, F8, F10, F11, F12 o Delete. Prova ognuno finché non lo trovi, o cerca su internet il modello del tuo computer e fai la domanda giusta.

Ad esempio "tasto BIOS laptop Dell".

Ogni computer avrà un menu BIOS diverso. Esplora e trova quale menu ti consente di configurare l'ordine di avvio. Per i nostri scopi, vogliamo che il computer cerchi di avviarsi da un dispositivo USB collegato (se ne è collegato uno), prima di cercare di avviarsi dall'hard disk interno (altrimenti si avvierà Windows). Una volta impostato ciò, potresti dover salvare prima di uscire o potrebbe salvare automaticamente.

Riavvia il computer e dovrebbe caricarsi dal dispositivo di memoria USB. Non possiamo installare Linux sull'hard disk interno e Windows verrà rimosso definitivamente.
Quando arrivi alla schermata seguente, seleziona "Installazione OEM (per produttori)". Se invece scegli "Avvia Linux Mint", avvierai una sessione di Linux Mint caricata dal dispositivo di memoria, ma una volta spento il computer, nessuna delle tue informazioni verrà salvata: è praticamente una sessione temporanea per provarlo.
![image](assets/10.webp)

Verrai guidato attraverso una procedura guidata grafica che ti farà alcune domande che dovrebbero essere semplici. Una riguarderà le impostazioni della lingua, un'altra riguarderà la connessione di rete domestica e la password. Se ti viene chiesto di installare software aggiuntivo, rifiutalo. Quando arrivi alla domanda sul tipo di installazione, alcune persone potrebbero esitare: devi scegliere "Cancella disco e installa Linux Mint". Inoltre, non criptare il disco e non selezionare LVM.

Arriverai infine al desktop. A questo punto, non hai ancora finito. In realtà stai agendo come il produttore (cioè qualcuno che costruisce un computer e configura Linux per il cliente). Devi fare doppio clic sull'icona del desktop "Installazione di Linux Mint" per finalizzarla.

![image](assets/11.webp)

Ricorda di rimuovere la chiavetta di memoria e riavviare. Dopo il riavvio, utilizzerai il sistema operativo per la prima volta come nuovo utente. Congratulazioni.

Una delle prime cose da fare (e da fare regolarmente) è mantenere il sistema aggiornato.

Apri l'applicazione Terminale e digita quanto segue:

```
    sudo apt-get update
```

premi <invio>, conferma la tua scelta e poi questo comando:

```
    sudo apt-get upgrade
```

premi <invio> e conferma la tua scelta.

Lascia che faccia il suo lavoro, potrebbe richiedere diversi minuti.

Successivamente, mi piace installare Tor (sensibile alle maiuscole):

```
    sudo apt-get install tor
```

> _AGGIUNTA: Puoi anche eseguire l'avvio di Linux Mint da "Installazione OEM" (assicurati di essere connesso a Internet, altrimenti potresti ottenere degli errori). Se fai questo, successivamente devi fare clic sull'icona "spedisci all'utente finale" che dovrebbe essere sul desktop. Quindi riavvia e avvia il sistema operativo come se stessi aprendo il computer per la prima volta._

Questa guida ha spiegato perché potresti aver bisogno di un computer dedicato per le transazioni Bitcoin e come installare un nuovo sistema operativo Linux Mint su di esso.
