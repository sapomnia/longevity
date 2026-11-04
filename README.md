# Longevity

Dati e grafici sulle RSA italiane: posti letto disponibili, persone in lista d'attesa e crescita della popolazione over 65 al 2050.

Progetto di <a href="https://www.linkedin.com/in/marta-abbà/">Marta Abbà</a> e <a href="https://www.linkedin.com/in/riccardo-saporiti-71812845/">Riccardo Saporiti</a>.

**Grafici e codici di embed:** <https://sapomnia.github.io/longevity/>

---

## Metodo di lavoro

Per raccogliere i dati utilizzati in questa inchiesta è stata inviata un’istanza di accesso generalizzato (FOIA) a tutte le aziende sanitarie locali italiane. Abbiamo chiesto loro di fornirci l’elenco delle RSA attive sul territorio di competenza, sia pubbliche che private, con il numero dei posti letto disponibili, il numero di persone in lista d’attesa alla data più recente disponibile e la tariffa media giornaliera per il ricovero nelle RSA. Solo il 78,2% delle aziende sanitarie ha risposto all’istanza e non tutte hanno fornito le informazioni richieste in maniera completa. I dati sono stati aperti, processati e visualizzati anche utilizzando Claude Opus 5.5 e Google Antigravity con Gemini 3.8 Flash.

---

## Grafici

| File | Titolo | Tipo | Dati usati |
|---|---|---|---|
| `posti-rsa-ogni-10mila-over-65.html` | I posti letto nelle RSA italiane | Barre orizzontali; un menu a tendina passa dalle regioni alle province di una regione | `Posti ogni 10mila over 65.csv` |
| `persone-lista-attesa-per-posto-letto.html` | RSA, i posti letto e le liste d'attesa | Barre orizzontali; un menu a tendina passa dalle regioni alle province di una regione | `Persone in lista d'attesa per posto letto.csv` |
| `rsa-posti-oggi-e-over-65-al-2050.html` | RSA: cosa succederà nel 2050? | Grafico a dispersione a bolle, con area proporzionale ai posti letto 2026 | `Posti letto e over 65 al 2050.csv` |

## Pagina indice ed embed

| File | Contenuto |
|---|---|
| `index.html` | Pagina principale del sito: mostra tutti i grafici, ciascuno con il proprio codice di embed da copiare. |
| `embed-longevity.md` | Gli stessi codici di embed in Markdown. Ogni codice è composto da un iframe e da uno script che ne regola l'altezza: vanno incollati insieme. |

## Contenuto cartella data

File originali, non modificati se non dove indicato.

#### `Posti disponibili RSA raw.csv`
Posti letto nelle RSA per singola struttura, come comunicati dalle aziende sanitarie.

#### `Persone in lista d'attesa raw.csv`
Persone in lista d'attesa per l'ingresso in RSA, come comunicati dalle aziende sanitarie.

#### `Residenti over 65.csv`
Residenti con 65 anni e più per provincia al 1 gennaio 2026. Fonte: Istat.

#### `Previsione popolazione over 65 al 2050.csv`
Previsioni Istat della popolazione over 65 nel 2050, per regione e per le province autonome di Bolzano e Trento.

### Dati elaborati

#### `Posti ogni 10mila over 65.csv`
Posti letto in RSA ogni 10mila residenti over 65, per provincia. 89 province.

- Province senza dati sui posti: Belluno, Benevento, Catania, Chieti, Cosenza, Enna, Frosinone, L'Aquila, Novara, Palermo, Pordenone, Ragusa, Reggio Calabria, Siracusa, Taranto, Teramo, Treviso, Vibo Valentia. Non compaiono nel file e i loro residenti sono esclusi dai valori regionali e dalla media nazionale del grafico.
- Il file dei posti usa la vecchia suddivisione provinciale della Sardegna. Ogliastra è attribuita a Nuoro e Sulcis Iglesiente a Sud Sardegna. Per questo il grafico mostra solo il dato regionale della Sardegna.

#### `Persone in lista d'attesa per posto letto.csv`
Persone in lista d'attesa per ogni posto letto disponibile, per provincia. 78 province.

- Liste e posti sono abbinati per azienda sanitaria. Al denominatore ci sono solo i posti delle aziende che hanno comunicato le liste: a Roma mancano le Asl Roma 1 e Roma 2, a Vicenza la Ulss 8 Berica.
- Province senza dati sulle liste: Avellino, Bolzano, Cagliari, Caserta, Genova, Latina, Pescara, Rovigo, Sassari, Sud Sardegna (ex Sulcis Iglesiente), Udine. L'Abruzzo è assente perché Pescara è la sua unica provincia con dati sui posti.
- In Lombardia (tranne la provincia di Bergamo), in Friuli Venezia Giulia e nelle province di Roma, Rieti e Lecce le liste sono quelle delle singole strutture. Una persona iscritta in più strutture può essere contata più volte, quindi il numero effettivo di persone in attesa potrebbe essere sovrastimato.

#### `Posti letto e over 65 al 2050.csv`
Confronto tra i posti letto di oggi e la crescita della popolazione over 65 tra il 2026 e il 2050. 10 righe.

- Comprende solo le aree in cui tutte le aziende sanitarie hanno fornito i dati sui posti letto: Valle d'Aosta, Lombardia, Provincia autonoma di Bolzano, Provincia autonoma di Trento, Emilia Romagna, Toscana, Marche, Umbria, Molise e Basilicata. Il calcolo è su base regionale perché le previsioni Istat sono regionali.
- Per la provincia autonoma di Bolzano il dato sui posti comprende una sola struttura (116 posti).

## Contenuto cartella raw data

I dati ottenuti dalle singole aziende sanitarie locali in risposta alle istanze di accesso generalizzato, suddivisi per regione.

## Altri file

| File | Contenuto |
|---|---|
| `.gitignore` | Esclude dal repository i file di sistema e le cartelle di lavoro locali (script di generazione e anteprime). |

## Licenza

Creative Commons Attribution 4.0 International
