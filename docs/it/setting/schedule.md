# Tabella di pianificazione

L'utente può programmare eventi tramite la tabella di pianificazione. Per esempio, una fabbrica avvia le macchine alle 8:00 e le ferma alle 18:00 nei giorni feriali.

Fare clic su "Tabella di pianificazione" (Schedule Table) in "Elenco standard": compare la finestra della tabella di pianificazione, come mostrato di seguito.

<img src="../../setting/schedule.files/schedule706.png" width="728" />

 Figura 7-49 Finestra Tabella di pianificazione

Fare clic sul pulsante "Nuovo" per aprire una nuova finestra, come mostrato di seguito. Viene mostrata per prima la scheda Generale.

<img src="../../setting/schedule.files/schedule984.png" width="694" />

  Figura 7-50 Finestra Nuova pianificazione

• Descrizione:

Inserire un testo che aiuti a capire la funzione di questa pianificazione.

• Esegui l'azione di inizio/fine all'accensione:

Se l'HMI viene acceso dopo l'ora di inizio, esegue l'azione di inizio/fine.

• Indirizzo di destinazione:

Inserire tipo e indirizzo di destinazione; il valore viene scritto in questo indirizzo all'ora di inizio/fine.

• Operazione di scrittura:

I tipi sono "Costante" e "Indirizzo". Con "Costante" si indica il valore da scrivere nell'indirizzo di destinazione. Con "Indirizzo" si indica un indirizzo il cui valore viene scritto nell'indirizzo di destinazione all'ora di inizio/fine.

• Usa l'operazione di fine:

Se selezionata, all'ora di fine il valore dell'operazione di scrittura viene scritto nell'indirizzo di destinazione.

 Impostata la scheda Generale, fare clic sulla scheda "Limite di tempo", come mostrato di seguito.

<img src="../../setting/schedule.files/schedule2016.png" width="694" />

  Figura 7-51 Scheda Limite di tempo

• Costante: selezionare l'ora di inizio/fine; a quell'ora viene eseguita la scrittura corrispondente.

• Indirizzo: un blocco di indirizzi controlla l'ora di inizio e di fine della pianificazione, come mostrato di seguito.

 <img src="../../setting/schedule.files/schedule2396.png" width="693" />

 Figura 7-52 Impostazione del controllo tramite indirizzo

Per esempio, con indirizzo LW0, gli indirizzi LW0~LW10 sono usati per la pianificazione.

LW0: indirizzo di controllo; quando LW0 == 1 gli orari della pianificazione vengono caricati nell'HMI e l'elemento di pianificazione entra in funzione. Dopo il caricamento LW0 viene riportato a 0;

LW1: stato della pianificazione; quando gli orari sono stati caricati (LW0==0), LW1 viene impostato a 1.

LW2: modalità di azione; se LW2 vale 1 e l'ora corrente è successiva all'ora di inizio, esegue la scrittura. Se LW2 vale 0, esegue l'operazione di inizio/fine quando l'ora corrente coincide con l'ora di inizio/fine.

LW3: indica i giorni dell'ora di inizio; il valore è 2^(numero del giorno della settimana), LW3 = (0,1,4,8,16,32,64)

LW4~LW6: ore, minuti e secondi dell'ora di inizio.

LW7: indica i giorni dell'ora di fine; il valore è 2^(numero del giorno della settimana), LW3 = (0,1,4,8,16,32,64)

LW8~LW10: ore, minuti e secondi dell'ora di fine.

Analogamente, se LWn è l'indirizzo di controllo, LWn~LWn+10 sono usati per la pianificazione, come sopra.

**Suggerimento:** se si sceglie Indirizzo, dopo aver impostato gli orari di inizio/fine non dimenticare di mettere a 1 l'indirizzo di controllo per caricare la pianificazione; altrimenti non funzionerà.

Scheda Divieto, come mostrato di seguito:

<img src="../../setting/schedule.files/schedule3691.png" width="694" />

 Figura 7-53 Scheda Divieto

Se si seleziona "Usa divieto", la pianificazione funziona solo quando l'indirizzo bit soddisfa la condizione (0 o 1).

Impostati i parametri della nuova finestra, fare clic su "OK" per creare un elemento della tabella di pianificazione, come mostrato di seguito.

<img src="../../setting/schedule.files/schedule4054.png" width="732" />

  Figura 7-50 Pianificazione creata
