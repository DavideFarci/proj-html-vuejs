DESCRIZIONE DEL PROGETTO:

L'App è divisa in 3 componenti principali: Header, main e footer.

HEADER: questo componente è formato da 3 sezioni, il pre-header contiene la whishlist e l'assistenza. La sezione della navigazione invece contiene il logo e i pulsanti per la ricerca, l'account personale e il carrello. Al centro invece si trova la nav che è stata resa un componente a se stante e viene elaborata tramite i dati di un array. L'ultima sezione è il jambotron, una semplice immagine con del testo sopra che mostra gli ultimi giochi arrivati nello store.

MAIN: è il componente più sostanzioso che contiene tutte le sezioni, alcune molto simili tra loro, per questo ho cercato di riciclare la struttura la dove possibile. La prima e l'ultima sezione ('mini-sec') sono identiche tranne il loro contenuto. Anche le sezioni 'double' hanno struttura identica ma differiscono per contenuto. Esse mostrano informazini prodotti "speciali" come quelli in offerta o gli ultimi arrivati. Le altre due sezioni 'carousel' invece mostrano rispettivamente i tutti i prodotti e i prodotti in offerta. Gli ho realizzari con un carosello dinamico generato tramite i dati.

FOOTER: diviso in footer alto e footer basso, il secondo, più semplice contiene il copyright e le informazioni sui pagamenti accettati. Il footer alto è stato inceve in parte generato tramite dati

Per il progetto sono stati utilizzati Vue.js, botstrap 5, sass e le icone sono invece di font awesome
