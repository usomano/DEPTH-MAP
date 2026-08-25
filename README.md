# Depth map

Strumento per generare mappe di profondità da un'immagine. Gira interamente nel
browser: le immagini non vengono caricate su nessun server.

## Come si usa

Apri l'indirizzo del sito, trascina un'immagine, premi **Genera depth map**.

Al primo utilizzo il browser scarica il modello, circa 50 MB. Dopo resta in
memoria e le volte successive parte subito.

## I controlli

**Dettaglio** — Lascia "Intera, una passata" per fotografie e paesaggi. I tile
servono solo su soggetti ravvicinati e molto dettagliati.

**Lato lungo in uscita** — La misura del file finale, in pixel o in millimetri.
Se scegli i millimetri imposta anche i dpi: il valore viene scritto dentro il
JPG, quindi InDesign e Photoshop lo piazzano alla misura fisica giusta.

**Modello** — Quattro modelli provati. Il primo va bene quasi sempre.

**Il grafico** — L'istogramma della mappa con la curva sopra. Clicca per
aggiungere un punto, trascina per spostarlo, doppio clic per toglierlo. I due
triangoli sotto tagliano il nero e il bianco.

**Espandi lontananza** — Apre le zone dove la profondità è compressa. Utile sui
paesaggi, dove le montagne occupano molti pixel ma pochi livelli di grigio.

**Contorni** — Aggancia i bordi della profondità a quelli della foto. Alzalo sui
ritratti e sui soggetti stagliati, tienilo a zero sui paesaggi e sulla grafica.

**Sfocatura, Grana, Qualità JPG** — Rifiniture sull'immagine finale.

**Preset** — Salva un'impostazione che usi spesso e la ritrovi la volta dopo.

## Limiti da conoscere

Su grafica piatta, loghi e tipografia il risultato non ha significato: il
modello cerca indizi di profondità che in un'immagine vettoriale non esistono.
Per quel tipo di materiale la mappa va costruita dalla geometria, non stimata.

L'uscita è JPG a 8 bit, quindi 256 livelli. Su gradienti molto lenti si possono
vedere delle fasce.

## Cosa esce dal browser

Tre sole richieste di rete: la libreria da jsdelivr, i pesi del modello da
huggingface.co, e un controllo sul repository del modello prima di scaricarlo.
Le tue immagini non escono mai dal computer.
