# Pomodoro Local

Este é um aplicativo local para gerenciamento de tempo utilizando a técnica Pomodoro, desenvolvido com React, TypeScript e Vite.

## Funcionalidades

- Inicie, pause e reinicie ciclos Pomodoro
- Personalize o tempo de foco e descanso
- Histórico de sessões
- Interface simples e intuitiva

## Como usar

1. Clone o repositório:
   ```bash
   git clone https://github.com/bernardo-kra/Pomodoro-Local.git
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Execute o aplicativo:
   ```bash
   npm run dev
   ```

## Sobre a Técnica Pomodoro

A técnica Pomodoro é um método de gerenciamento de tempo que utiliza blocos de foco (geralmente 25 minutos) seguidos de breves intervalos.

---

## Stack do Projeto

- **React** + **TypeScript** + **Vite**

Este template fornece uma configuração mínima para rodar React no Vite com HMR e algumas regras de ESLint.

Atualmente, dois plugins oficiais estão disponíveis:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) usa [Babel](https://babeljs.io/) para Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) usa [SWC](https://swc.rs/) para Fast Refresh

### Expansão da configuração do ESLint

Se você está desenvolvendo uma aplicação para produção, recomendamos atualizar a configuração para habilitar regras de lint com verificação de tipos:

```js
export default tseslint.config({
  extends: [
    // Remove ...tseslint.configs.recommended and replace with this
    ...tseslint.configs.recommendedTypeChecked,
    // Alternatively, use this for stricter rules
    ...tseslint.configs.strictTypeChecked,
    // Optionally, add this for stylistic rules
    ...tseslint.configs.stylisticTypeChecked,
  ],
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

Você também pode instalar [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) e [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) para regras específicas do React:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config({
  plugins: {
    // Add the react-x and react-dom plugins
    'react-x': reactX,
    'react-dom': reactDom,
  },
  rules: {
    // other rules...
    // Enable its recommended typescript rules
    ...reactX.configs['recommended-typescript'].rules,
    ...reactDom.configs.recommended.rules,
  },
})
```

## 🚀 Padrão de Branches e Commits

### 📂 Criação de Branches

As branches devem seguir o padrão:

```
PO-[número-da-tarefa]/[descricao-curta]
```

#### Exemplo:
```bash
git checkout -b PO-1/login
```
- **PO-1** → número da tarefa
- **login** → descrição curta e objetiva da feature ou correção

⚠️ Sempre crie a branch a partir da branch `dev`:

```bash
git checkout dev
git pull origin dev
git checkout -b PO-1/login
```

### 📝 Commits

Os commits devem seguir o padrão:

```
PO-[número-da-tarefa] [tipo]: descrição breve
```

**Tipos aceitos:**
- `[feat]` → Nova funcionalidade
- `[fix]` → Correção simples
- `[bugfix]` → Correção de bug mais complexo
- `[refactor]` → Refatoração de código sem alterar comportamento
- `[chore]` → Tarefas técnicas (build, scripts, configs, etc.)
- `[docs]` → Atualizações na documentação

#### Exemplos:
```bash
git commit -m "PO-1 [feat]: adiciona tela de login"
git commit -m "PO-2 [fix]: corrige validação do campo de e-mail"
git commit -m "PO-3 [bugfix]: corrige redirecionamento após login"
```

## Licença

Este projeto está licenciado sob a licença MIT.
