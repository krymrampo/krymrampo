# Francesco Rampini — Progetti selezionati

Data & AI Engineer. Progetti selezionati su assistenti AI, automazione di processi e sviluppo di applicazioni web, dalla logica applicativa alle interfacce e alla persistenza dei dati.

[GitHub](https://github.com/krymrampo) · [Krymtech](https://krymtech.com)

## Salone AI / tAIuto

**Obiettivo:** permettere ai clienti di gestire le prenotazioni di un salone tramite WhatsApp, affiancando una dashboard per gli operatori.

**Implementazione:**

- Assistente con OpenAI Responses API e tool per disponibilità, proposte alternative, creazione, cancellazione e spostamento degli appuntamenti.
- Regole applicative per durata dei servizi, disponibilità dello staff e sovrapposizioni; ricontrollo dello slot prima del salvataggio, con lock sulle operazioni di prenotazione.
- Webhook WhatsApp con gestione dei messaggi duplicati, elaborazione asincrona e instradamento verso il salone configurato.
- Persistenza SQLite per salone e dashboard per appuntamenti, clienti, servizi e staff.

**Tecnologie:** Python, Flask, OpenAI API, WhatsApp Cloud API, SQLite.

**Focus tecnico:** collegare la conversazione naturale a operazioni concrete, mantenendo i controlli di disponibilità nella logica applicativa.

## Piattaforma HR con supporto AI

**Obiettivo:** riunire gestione dei candidati, preparazione dei colloqui e supporto AI al lavoro del recruiter.

**Implementazione:**

- Caricamento dei CV, estrazione dei dati con anteprima nell'interfaccia e gestione di ruoli e competenze.
- Preparazione delle domande, follow-up e trascrizione delle risposte audio tramite un componente di registrazione nel browser.
- Supporto AI alla valutazione delle singole risposte e alla sintesi del colloquio, con comandi dedicati nell'interfaccia.
- Backend organizzato in API, servizi e modelli; dati associati all'azienda, autenticazione, migrazioni Alembic e registrazione degli input/output AI con identificativo della versione dei prompt.

**Tecnologie:** Python, FastAPI, PostgreSQL, SQLAlchemy, Alembic, React, TypeScript, OpenAI API.

**Focus tecnico:** integrare più funzioni AI nello stesso flusso applicativo, collegando frontend, API e dati persistenti, con output tracciati e azioni avviate dal recruiter.

## Workspace della band

**Obiettivo:** aiutare una band a scegliere il repertorio e organizzare scaletta e appunti in uno spazio condiviso.

**Implementazione:**

- Votazioni sui brani, consultazione delle preferenze per membro e ordinamento del repertorio.
- Scaletta riordinabile con controllo della revisione al salvataggio e richiesta di ricaricamento quando un altro membro l'ha modificata.
- Note collegate ai brani, conservate anche quando il brano associato viene eliminato.
- Dati condivisi tramite Supabase; modalità locale nel browser quando il database non è configurato.
- Test presenti per migrazioni ripetibili, revisioni e conservazione delle note; scenari Playwright per navigazione, persistenza, conflitti e layout mobile/desktop.

**Tecnologie:** Next.js, React, TypeScript, Supabase/PostgreSQL, Tailwind CSS, Playwright.

**Focus tecnico:** coerenza dei dati e gestione esplicita dei conflitti in un'applicazione per un gruppo fidato, con selezione del membro senza account individuali.

[Repository del progetto](https://github.com/krymrampo/votazione_band)
