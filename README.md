# Big Bang Theory Claude Agents 🧪

Una collezione di agenti Claude riutilizzabili ispirati ai personaggi di **The Big Bang Theory**, progettati per essere utilizzati con [Claude Code](https://github.com/anthropics/claude-code) tramite Git submodule.

Ogni agente ha personalità, competenze e stile di comunicazione unici basati sul personaggio della serie, rendendo le interazioni più coinvolgenti e specializzate per diversi ambiti dello sviluppo software.

---

## 🎭 Gli Agenti

### 👨‍💻 **Sheldon Cooper** - DevOps Expert
**File:** `sheldon.md`
**Specializzazione:** Git, CI/CD, Bash scripting, Docker, deployment
**Personalità:** Metodico, preciso, ossessionato dalle best practices
**Usa quando:** Devi configurare pipeline CI/CD, automatizzare deployment, scrivere script bash robusti, gestire Git workflows

### 🍷 **Penny** - Wine Data Explorer & UX Specialist
**File:** `penny.md`
**Specializzazione:** UX/UI design, wine domain knowledge, Liv-Ex API, user testing
**Personalità:** Pratica, orientata all'utente finale, comunicazione chiara
**Usa quando:** Serve feedback UX, devi cercare dati vini su Liv-Ex, vuoi migliorare usabilità, scrivi copy user-friendly

### 🛠️ **Howard Wolowitz** - Full-Stack Developer
**File:** `howard.md`
**Specializzazione:** PHP, WordPress, API integration, frontend/backend development
**Personalità:** Pragmatico, orientato ai risultati, creativo nel problem-solving
**Usa quando:** Devi implementare features WordPress, integrare API esterne, sviluppare checkout, scrivere codice full-stack

### 🏗️ **Leonard Hofstadter** - Software Architect
**File:** `leonard.md`
**Specializzazione:** System design, architecture patterns, DDD, database modeling, API design
**Personalità:** Bilanciato tra teoria e pratica, collaborativo, flessibile
**Usa quando:** Devi progettare architettura di sistema, definire pattern, creare database schema, design RESTful APIs

### 🧪 **Rajesh Koothrappali** - QA Engineer
**File:** `raj.md`
**Specializzazione:** PHPUnit, Jest, Cypress, testing automation, bug tracking
**Personalità:** Metodico, attento ai dettagli, paziente
**Usa quando:** Scrivi unit test, esegui integration testing, fai performance testing, documenti bug

### 📚 **Amy Farrah Fowler** - Technical Writer
**File:** `amy.md`
**Specializzazione:** Documentation, API docs, technical writing, knowledge management
**Personalità:** Strutturata, chiara, educativa
**Usa quando:** Devi scrivere documentazione tecnica, creare API reference, README files, user guides

### 🎨 **Bernadette Rostenkowski** - Project Manager
**File:** `bernadette.md`
**Specializzazione:** Project planning, team coordination, stakeholder management, roadmap
**Personalità:** Efficiente, diretta, orientata ai risultati
**Usa quando:** Pianifichi progetti, gestisci priorità, coordini team, crei roadmap

### ⚡ **Barry Kripke** - Performance Engineer
**File:** `barry.md`
**Specializzazione:** Performance optimization, profiling, caching strategies, scalability
**Personalità:** Competitivo, diretto, focus su velocità
**Usa quando:** Ottimizzi performance, identifichi bottleneck, implementi caching, migliori scalabilità

### 🔬 **Leslie Winkle** - Research & Analysis
**File:** `leslie.md`
**Specializzazione:** Code analysis, research, technical investigation, competitive analysis
**Personalità:** Analitica, critica, basata sui dati
**Usa quando:** Analizzi codebase, ricerchi soluzioni, confronti tecnologie, fai technical audit

### 🍕 **Pasquale** - Italian Backend Specialist
**File:** `pasquale.md`
**Specializzazione:** Backend systems, API development, microservices, Italian market expertise
**Personalità:** Passionale, diretto, focus su soluzioni pratiche
**Usa quando:** Sviluppi backend robusti, progetti microservices, lavori su progetti per mercato italiano

---

## 📦 Installazione come Git Submodule

### 1️⃣ Aggiungi il submodule al tuo progetto

Nella root del tuo progetto, aggiungi questo repository come submodule nella directory `.claude/commands/`:

```bash
# Crea la directory .claude se non esiste
mkdir -p .claude

# Aggiungi il submodule
git submodule add https://github.com/tuousername/big-bang-theory-claude-agent.git .claude/commands

# Commit il submodule
git add .claude/commands .gitmodules
git commit -m "Add Big Bang Theory Claude agents as submodule"
```

### 2️⃣ Inizializza il submodule (per chi clona il tuo repo)

Se qualcun altro clona il tuo repository, dovrà inizializzare i submodule:

```bash
# Clone del repo principale
git clone https://github.com/tuo-progetto/repo.git
cd repo

# Inizializza e aggiorna i submodule
git submodule init
git submodule update
```

Oppure clona direttamente con i submodule:

```bash
git clone --recurse-submodules https://github.com/tuo-progetto/repo.git
```

### 3️⃣ Aggiorna gli agenti (pull delle ultime modifiche)

Per aggiornare gli agenti alla versione più recente:

```bash
# Entra nella directory del submodule
cd .claude/commands

# Pull delle ultime modifiche
git pull origin main

# Torna alla root e commit l'aggiornamento
cd ../..
git add .claude/commands
git commit -m "Update Claude agents to latest version"
```

---

## 🚀 Utilizzo

### Con Claude Code CLI

Una volta installato come submodule, gli agenti saranno automaticamente disponibili come comandi in Claude Code:

```bash
# Lista tutti i comandi disponibili
claude --help

# Usa un agente specifico
claude /sheldon "setup CI/CD pipeline for WordPress plugin"
claude /penny "review this checkout UX"
claude /howard "implement Liv-Ex API integration"
claude /leonard "design architecture for multi-tenant system"
claude /raj "write unit tests for CheckoutService"
```

### Da Web UI (claude.ai)

Se usi Claude via web, puoi caricare manualmente i file `.md` come context o copiare le istruzioni nella conversazione.

### Struttura Directory

Dopo l'installazione, la struttura sarà:

```
tuo-progetto/
├── .claude/
│   └── commands/              # Git submodule
│       ├── README.md          # Questo file
│       ├── sheldon.md
│       ├── penny.md
│       ├── howard.md
│       ├── leonard.md
│       ├── raj.md
│       ├── amy.md
│       ├── bernadette.md
│       ├── barry.md
│       ├── leslie.md
│       └── pasquale.md
├── src/
├── tests/
└── README.md
```

---

## 🎯 Esempi di Workflow

### Scenario 1: Sviluppo Feature Completa

```bash
# 1. Leonard progetta l'architettura
claude /leonard "design checkout system for wine marketplace"

# 2. Howard implementa il codice
claude /howard "implement checkout service following Leonard's design"

# 3. Raj scrive i test
claude /raj "write unit and integration tests for checkout"

# 4. Penny testa la UX
claude /penny "review checkout user experience"

# 5. Amy scrive la documentazione
claude /amy "document checkout API endpoints"

# 6. Sheldon configura il deployment
claude /sheldon "setup CI/CD for automated deployment"
```

### Scenario 2: Ottimizzazione Performance

```bash
# 1. Barry identifica i bottleneck
claude /barry "profile application and identify performance bottlenecks"

# 2. Howard implementa le ottimizzazioni
claude /howard "implement caching layer for Liv-Ex API calls"

# 3. Raj verifica le performance
claude /raj "write performance tests and benchmarks"
```

### Scenario 3: Wine Data Research

```bash
# Usa Penny per cercare vini su Liv-Ex
claude /penny "find best value Bordeaux 2015 under €500"
claude /penny "compare Château Latour vs Margaux 2015"
claude /penny "search Pomerol wines with investment potential"
```

---

## 🔧 Personalizzazione

Puoi personalizzare gli agenti per il tuo progetto:

### Opzione 1: Fork il Repository

1. Fai fork di questo repository
2. Modifica i file `.md` con context specifico del tuo progetto
3. Usa il tuo fork come submodule:

```bash
git submodule add https://github.com/tuo-username/big-bang-theory-claude-agent.git .claude/commands
```

### Opzione 2: Estendi gli Agenti

Crea agenti personalizzati nella directory `.claude/commands/custom/`:

```bash
mkdir -p .claude/commands/custom
```

Mantieni gli agenti base come submodule e aggiungi i tuoi custom commands separatamente.

---

## 🤝 Contribuire

Contributi benvenuti! Per aggiungere miglioramenti:

1. Fork il repository
2. Crea un branch per la tua feature: `git checkout -b feature/miglioramento-sheldon`
3. Commit le modifiche: `git commit -m "Aggiungi supporto Kubernetes a Sheldon"`
4. Push al branch: `git push origin feature/miglioramento-sheldon`
5. Apri una Pull Request

### Linee Guida

- Mantieni la personalità del personaggio coerente
- Aggiungi esempi pratici e codice funzionante
- Testa le istruzioni prima di committare
- Aggiorna questo README se aggiungi nuovi agenti

---

## 📋 Vantaggi dell'Approccio Submodule

✅ **Riutilizzabilità:** Usa gli stessi agenti in progetti diversi
✅ **Aggiornamenti centralizati:** Fix e miglioramenti disponibili per tutti i progetti
✅ **Versionamento:** Ogni progetto può usare una versione specifica degli agenti
✅ **Separazione:** Gli agenti sono separati dal codice del progetto
✅ **Condivisione team:** Tutto il team usa gli stessi agenti standardizzati

---

## 🎬 Origine del Progetto

Questi agenti sono stati sviluppati originariamente per il progetto **liv-ex-helper**, un sistema di integrazione tra Liv-Ex (wine trading platform) e WordPress/WooCommerce.

La specializzazione sul dominio wine trading (particolarmente evidente in Penny) è parte del contesto originale, ma gli agenti sono progettati per essere riutilizzabili in qualsiasi progetto software.

---

## 📄 Licenza

MIT License - Vedi [LICENSE](LICENSE) per dettagli

---

## 🙏 Credits

- Inspired by **The Big Bang Theory** TV series
- Powered by [Claude Code](https://github.com/anthropics/claude-code) by Anthropic
- Created for the liv-ex-helper project

---

## 📞 Supporto

Per domande, problemi o suggerimenti:
- Apri una [Issue](https://github.com/tuousername/big-bang-theory-claude-agent/issues)
- Contribuisci con una Pull Request

---

**Bazinga!** 🖖 Buon coding con la gang di Big Bang Theory!
