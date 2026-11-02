# Esempio di ricette

L'esempio seguente mostra le impostazioni e la modalità di visualizzazione delle ricette.

1\. **Creare una nuova ricetta**

In Gestione progetto, fare clic con il tasto destro su Recipe, come mostrato in Figura 1:

<img src="../../case/formula-case.files/formula-case168.png" width="284" />

Figura 11 Creazione di una nuova ricetta

Fare doppio clic per aprire la ricetta, come mostrato in Figura 2:

<img src="../../case/formula-case.files/formula-case254.png" width="514" />

Figura 12 Impostazioni generali della ricetta

Impostare la lunghezza della ricetta a 4, cioè ogni ricetta contiene 4 dati, e il numero totale a 10, cioè 10 ricette. Impostare a D50 l'indirizzo in cui scrivere la ricetta nel PLC e selezionare intero positivo a 16 bit: la ricetta viene scritta nei registri D50, D51, D52 e D53. Le impostazioni sono le stesse dell'indirizzo di scrittura.

2\. **Impostazione degli elementi dati della ricetta:**

<img src="../../case/formula-case.files/formula-case637.png" width="511" />

Figura 13 Impostazione degli elementi dati della ricetta

Dopo aver impostato il nome della ricetta, selezionare "OK" per completare. Per visualizzare i dati della ricetta sul touch screen si usano gli oggetti di inserimento e visualizzazione numerica. Per l'oggetto di inserimento e visualizzazione numerica che indica il numero della ricetta selezionare l'indirizzo di memoria interna RWI0: il valore di RWI0 è il numero della ricetta (il valore 2 indica la ricetta numero 2, e così via). Usare gli oggetti di inserimento e visualizzazione numerica per mostrare i dati da D50 a D53. Con le funzioni del "Function Button" è possibile salvare o leggere una ricetta. Per i dettagli, vedere "Pulsante funzione".

<img src="../../case/formula-case.files/formula-case1276.png" width="663" />

Figura 14 Oggetto "inserimento e visualizzazione numerica" per il dato di ricetta D50

Configurare gli oggetti di inserimento e visualizzazione numerica e posizionarli nella pagina:

<img src="../../case/formula-case.files/formula-case1422.png" width="746" />

Figura 15 Vista della pagina di visualizzazione delle ricette

I parametri della ricetta possono essere modificati tramite gli oggetti di inserimento e visualizzazione numerica; i pulsanti funzione permettono di consultare, leggere e scrivere le ricette.
