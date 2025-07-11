---
title: "Testei o novo Code Agent do Google (grátis) — Gemini CLI na prática"
date: 2025-07-10
layout: post
---

# 🎯 Novo Code Agent do Google 100% Grátis

O Google lançou recentemente uma CLI chamada `gemini`, que funciona como um agente de codificação com acesso direto ao modelo **Gemini 2.5 Pro**.

E sim: **é gratuito**, com direito a uma janela de contexto gigante (1 milhão de tokens), **60 requisições por minuto** e até **1.000 por dia**.

Instalei aqui e testei com alguns projetos meus — e já deu pra ver que ela pode ser útil, principalmente pra tarefas repetitivas.

---

## ✅ O que dá pra fazer?

- **Refatorar código**: pedi pra melhorar uma função que estava duplicada — ele reorganizou bem, com explicações no diff.
- **Achar bugs**: testei com um trecho em que faltava um `await`, e ele apontou na hora.
- **Começar do zero**: pedi um app básico com FastAPI + SQLite e ele deu uma base OK — não perfeita, mas já útil pra começar algo rápido.

Ainda estou explorando, mas já vale o teste.

---

## 🛠️ Como instalar e usar?

### O que você precisa

Como requisito obrigatório, você deve ter o **Node.js** instalado em sua máquina (versão 18 ou superior).  
Você pode baixar diretamente do site oficial: [https://nodejs.org/pt](https://nodejs.org/pt)  
Ou executar o código abaixo usando o `nvm`:

```bash
# Download e instale o NVM:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash

# (em vez de reiniciar o shell)
\. "$HOME/.nvm/nvm.sh"

# Instale o Node.js:
nvm install 22

# Verifique a versão do Node.js:
node -v       # Deve exibir "v22.17.0"
nvm current   # Deve exibir "v22.17.0"

# Verifique a versão do npm:
npm -v        # Deve exibir "10.9.2"
```

Isso garante que você consiga executar o Gemini CLI corretamente.

---

### 1º Passo: Configurar o Gemini

Depois que o Node.js e o npm estiverem instalados e verificados, instale o Gemini CLI com o comando:

```bash
npx https://github.com/google-gemini/gemini-cli
```

Ou, se preferir, use o npm para instalação global:

```bash
npm install -g @google/gemini-cli
gemini
```

Quando o `gemini-cli` estiver instalado, basta digitar `gemini` no terminal para acessá-lo.

---

### Passo 1.2 — Autenticação

Você pode usar sua conta pessoal do Google para se autenticar quando solicitado.  
Isso concederá a você até **60 solicitações por minuto** e **1.000 por dia** usando o Gemini.

Ao autenticar, uma janela será aberta no seu navegador para você fazer login com sua conta Google.

---

### Passo 1.3 — Finalmente! Iniciar um novo Projeto

Para iniciar um projeto do zero, execute os seguintes comandos:

```bash
cd new-project/
gemini
```

---

## Vale a pena?

Se você curte testar ferramentas novas e já usa IA no seu fluxo de trabalho, vale muito a pena dar uma chance pro `gemini`.

Ele ainda tem limitações, principalmente em projetos maiores ou com dependências específicas, mas pra tarefas pontuais e automações simples ele entrega bem.

Eu vou continuar testando com outras linguagens, frameworks e setups mais pesados. Se encontrar algo fora da curva (bom ou ruim), atualizo esse artigo aqui mesmo.

Se você já testou ou quer trocar ideia sobre, me chama no GitHub ou LinkedIn — tô sempre aberto a trocar experiências reais com outras pessoas dev.

---

✍️ *Escrito por Pedro Neves, estudante de Ciência da Computação.*
