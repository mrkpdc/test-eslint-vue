# Vue.js + ESLint + Prettier test app

App di test basata su Vue con plugin ESLint e Prettier per la formattazione (vedi il componente TestLint.vue)

- Il linter può essere configurato tramite il file eslint.config.js
- Prettier può essere configurato tramite la chiave "prettier" all'interno di package.json

## Setup

- [Vue - Official](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (previously Volar) and disable Vetur
- [Install eslint-plugin-vue](https://eslint.vuejs.org/)
- [Install Prettier](https://prettier.io/docs/en/install)
- [Install eslint-config-prettier](https://github.com/prettier/eslint-config-prettier#installation)
- Aggiungere ai settings di VSCode (anche solo per il workspace corrente)
  
  {
    "eslint.validate": [
        "javascript",
        "vue"
    ],
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
