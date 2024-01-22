# VITE BOOLFOLIO


# Milestone 1
Iniziamo ad occuparci della parte front-office della nostra applicazione: <br>

creiamo un nuovo progetto Vue 3 con Vite e installiamo axios. <br>

Installiamo vue router e creiamo il file router.js con le rotte (almeno  home, projects, singolo progetto e fallback route) <br>

# Milestone 2
Nel componente relativo alla lista dei progetti della nostra Vue App facciamo una chiamata API all’endpoint costruito nel progetto Laravel  e recuperiamo tutti i progetti dal nostro back-end. <br>
Stampiamo in console i risultati e verifichiamo di ricevere i dati correttamente. Poi stampiamoli in pagina. <br>
# Milestone 3
Creiamo un nuovo componente ProjectCard, che corrisponde ad una card per visualizzare un progetto. <br>
Utilizziamo questo componente per visualizzare tutti i progetti ricevuti tramite API. <br>
# Milestone 4
Creiamo un nuovo componente es. ProjectDetail che corrisponde alla rotta per visualizzare il singolo progetto completo di technologies e Type. <br>
Utilizziamo questo componente per visualizzare i dati ricevuti tramite API che recupera il singolo progetto. <br>
Creiamo anche un componente NotFound per la rotta di fallback. <br>

# Bonus:
Gestire la paginazione dei risultati nella pagina dei progetti <br>
Creare una barra di navigazione in un componente header e un componente per il footer <br>s