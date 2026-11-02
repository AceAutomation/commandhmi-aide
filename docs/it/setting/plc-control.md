# Controllo da PLC

Il controllo da PLC consente di cambiare pagina, livello utente, ricetta e di scrivere ricette tramite il PLC. Fare doppio clic su "Controllo PLC" nel "Gestore di progetto" per aprire la finestra mostrata nella Figura 7-8:

Figura 7-8      Finestra Controllo PLC

• Cambia ricetta: l'HMI cambia ricetta in base al valore di questo indirizzo.

• Scrivi ricetta: l'HMI scrive la ricetta in base al valore di questo indirizzo.

• Livello utente corrente: l'HMI imposta il livello utente corrente in base al valore di questo indirizzo.

• Cambio pagina tramite indirizzo word: l'HMI cambia pagina in base al valore di questo indirizzo word; se il valore è n, passa alla pagina n.

• Cambio pagina tramite indirizzo bit: fare doppio clic sulla riga "Nuovo"; compare la finestra mostrata nella Figura 7-9:

Nuovo controllo tramite bit:

<img src="../../setting/plc-control.files/image004.jpg" width="458" />

Nuovo controllo pagina tramite word

<img src="../../setting/plc-control.files/image006.jpg" width="497" />

Pagina: il controllo word del PLC passa solo tra pagine

Finestre: il controllo word del PLC passa solo tra finestre

Pagina/finestra: il controllo word del PLC passa tra pagine e finestre

<img src="../../setting/plc-control.files/image005.jpg" width="130" />

Nota: quando si cambia pagina tramite PLC, il valore letto la prima volta non provoca il cambio. Il cambio avviene solo quando il valore del registro PLC è diverso dal primo valore letto.
