# Setup e validazione di una infrastruttura LoRaWAN privata 🎓📡

[![LaTeX](https://img.shields.io/badge/LaTeX-47A141?style=flat-square&logo=LaTeX&logoColor=white)](https://www.latex-project.org/)
[![UniPd](https://img.shields.io/badge/UniPd-B71234?style=flat-square)](https://www.unipd.it/)
[![LoRaWAN](https://img.shields.io/badge/LoRaWAN-000000?style=flat-square)](https://lora-alliance.org/)
[![M31](https://img.shields.io/badge/M31-Corporate-blue?style=flat-square)](https://www.m31.com/)

Questa repository contiene il codice sorgente in LaTeX della mia tesi di Laurea in **Informatica** presso l'**Università degli Studi di Padova (UniPd)**.

Il progetto è stato sviluppato durante un periodo di stage presso l'azienda **M31 Srl**.


## 📝 Abstract

L'obiettivo di questo lavoro è stato progettare, realizzare e validare sperimentalmente una infrastruttura LoRaWAN privata orientata a contesti agricoli. Il sistema si basa su un gateway LoRaWAN implementato su Raspberry Pi con concentratore SX1303, un server locale basato su ChirpStack e nodi sensore dotati di firmware custom. Il progetto ha previsto un'estesa campagna di test per caratterizzare il sistema dal punto di vista prestazionale, individuandone i limiti operativi sul campo e definendo le linee guida per una sua possibile industrializzazione.


## 🏗️ Architettura del Sistema

Il progetto sviluppato si struttura su tre livelli principali:

* **Livello di campo:** Composto dal gateway LoRaWAN e dai nodi sensore distribuiti.
* **Livello server:** Infrastruttura completamente locale basata su ChirpStack, comprensiva di network server, broker MQTT e database.
* **Livello applicativo:** Livello dedicato alla decodifica dei dati e alla loro integrazione con servizi esterni tramite MQTT o API.


## 🏢 Contesto Accademico e Aziendale

* **Università:** Università degli Studi di Padova (Dipartimento di Matematica "Tullio Levi-Civita")
* **Corso di Laurea:** Laurea in Informatica
* **Azienda Partner:** M31 Srl (Padova)
* **Anno Accademico:** 2025/2026
* **Relatore:** Prof. Marco Zanella
* **Correlatore Aziendale:** David Eccher


## 📂 Struttura della Repository

Il codice sorgente è organizzato secondo la struttura del template di Dipartimento:

* `config/`: Variabili globali, metadati del PDF e pacchetti LaTeX.
* `preface/`: Pagine iniziali (sommario, ringraziamenti, dediche, frontespizio).
* `chapters/`: Il cuore della tesi (dall'analisi dei requisiti fino ai test funzionali e prestazionali).
* `appendix/`: Bibliografia (`.bib`), glossario e appendici.
* `images/`: Asset grafici e diagrammi.
* `thesis.tex`: Il file root per generare il PDF digitale.
* `printable-thesis.tex`: Il file root per generare la versione da stampa.


## 🛠️ Requisiti e Compilazione

Per compilare correttamente il documento, inclusi glossario, bibliografia e immagini vettoriali, è necessaria una configurazione LaTeX completa (es. **TeX Live**).

### Dipendenze Aggiuntive

Il template supporta nativamente l'inclusione di immagini SVG. Assicurati di avere installato:

* `cairosvg`
* Un ambiente POSIX (per i diagrammi draw.io)

### Compilazione tramite Terminale

Il metodo consigliato per generare il PDF completo è utilizzare `latexmk`:

```bash
latexmk thesis.tex
```

### Compilazione tramite Editor

Se utilizzi VS Code con l'estensione LaTeX Workshop, la repository include già il file .vscode/settings.json. Il progetto è preconfigurato per usare latexmk come comando di build predefinito, quindi la compilazione funzionerà out-of-the-box ad ogni salvataggio.


## 📄 Licenza e Riservatezza

Il presente documento fa riferimento a tecnologie e infrastrutture sviluppate per M31 Srl. Alcuni dettagli implementativi e il codice sorgente dell'applicativo potrebbero costituire informazioni confidenziali e, come tali, non sono divulgabili senza previo consenso scritto dell'azienda. Questa repository contiene esclusivamente l'elaborato testuale della tesi di laurea.