🧩 React Frontend – Dev Container

Questo progetto utilizza un Dev Container basato su Alpine Linux con Node.js 20 LTS per garantire un ambiente di sviluppo riproducibile, leggero e coerente per tutto il team.

Il dev server React viene avviato automaticamente all’apertura del container.

📦 Stack

OS: Alpine Linux 3.20

Runtime: Node.js 20 LTS

Package Manager: npm

Framework Frontend: React (Vite consigliato)

Editor: VS Code + Dev Containers

🚀 Avvio rapido
Prerequisiti

Docker

Visual Studio Code

Estensione Dev Containers

Avvio ambiente

Clona il repository

Apri il progetto in VS Code

Seleziona “Reopen in Container”

Il container verrà costruito automaticamente e:

verranno installate le dipendenze (npm install)

il dev server React partirà in automatico

il browser si aprirà su http://localhost:5173

🌐 Dev Server

Porta: 5173

Binding: 0.0.0.0

Auto-open browser: sì

Per Vite, assicurati che vite.config.js contenga:

export default {
  server: {
    host: true,
    port: 5173,
    strictPort: true
  }
}

🛠️ Lifecycle del Dev Container
Fase	Comando
Creazione container	npm install
Avvio container	npm run dev -- --host

postCreateCommand: installa le dipendenze una sola volta

postStartCommand: avvia il dev server a ogni start

🧠 Best Practices adottate
✅ Sicurezza

Container non root (vscode)

Nessun servizio superfluo

⚡ Performance

Cache npm persistente (~/.npm)

Alpine minimal

🧑‍💻 Developer Experience

Dev server auto-start

Browser auto-open

Estensioni VS Code preinstallate

🧩 Estensioni VS Code incluse

ESLint

Prettier

React / Redux Snippets

Tailwind CSS IntelliSense

Auto Rename Tag

npm Intellisense

Tutte le estensioni vengono installate automaticamente nel container.

📁 Struttura progetto consigliata
.
├─ src/
├─ public/
├─ package.json
├─ vite.config.js
└─ .devcontainer/
   └─ devcontainer.json