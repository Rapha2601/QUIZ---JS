# Relatório de Tecnologias: React & NestJS

# Raphael Ferreira e Pedro Sachetto
---

## 1. React

### 1.1 O que é?

React é uma **biblioteca JavaScript de código aberto** criada pelo Facebook (Meta) em 2013, voltada para a construção de interfaces de usuário (UI). Sua principal proposta é permitir que desenvolvedores criem componentes reutilizáveis que reagem automaticamente a mudanças de estado, atualizando apenas as partes necessárias da tela.

### 1.2 Conceitos Fundamentais

| Conceito | Descrição |
|---|---|
| **Componentes** | Blocos de construção reutilizáveis da UI (funcionais ou de classe) |
| **JSX** | Sintaxe que combina JavaScript e HTML para descrever a interface |
| **Props** | Dados passados de um componente pai para um filho (somente leitura) |
| **State** | Estado interno do componente; quando alterado, dispara nova renderização |
| **Virtual DOM** | Representação virtual do DOM real; o React calcula o mínimo de mudanças necessárias para atualizar a tela |
| **Hooks** | Funções como `useState`, `useEffect`, `useContext` que permitem usar recursos do React em componentes funcionais |

### 1.3 Ecossistema

- **Roteamento:** React Router
- **Gerenciamento de estado:** Redux, Zustand, Context API
- **Estilização:** Tailwind CSS, Styled Components, CSS Modules
- **Requisições HTTP:** Axios, React Query
- **Frameworks baseados em React:** Next.js (SSR/SSG), Remix

### 1.4 Vantagens e Desvantagens

| ✅ Vantagens | ❌ Desvantagens |
|---|---|
| Alta reutilização de componentes | É uma biblioteca, não um framework completo |
| Grande comunidade e ecossistema | Curva de aprendizado do ecossistema |
| Virtual DOM melhora a performance | Muitas opções geram decisões arquiteturais extras |
| Suportado pela Meta | JSX pode confundir iniciantes |

---

## 2. NestJS

### 2.1 O que é?

NestJS é um **framework Node.js progressivo** de código aberto, construído sobre o TypeScript e inspirado na arquitetura do Angular. Lançado em 2017 por Kamil Myśliwiec, é utilizado para construir aplicações de back-end eficientes, escaláveis e bem estruturadas, com suporte nativo a REST, GraphQL, WebSockets e microsserviços.

### 2.2 Conceitos Fundamentais

| Conceito | Descrição |
|---|---|
| **Módulos** | Organizam a aplicação em unidades coesas (`@Module`) |
| **Controllers** | Recebem requisições HTTP e retornam respostas (`@Controller`, `@Get`, `@Post`…) |
| **Services** | Contêm a lógica de negócio, injetados via IoC (`@Injectable`) |
| **Injeção de Dependência** | Padrão de design central; o NestJS gerencia o ciclo de vida dos objetos |
| **Guards** | Controlam o acesso a rotas (ex.: autenticação JWT) |
| **Pipes** | Transformam e validam dados de entrada (`ValidationPipe`) |
| **Interceptors** | Interceptam a execução para adicionar lógica transversal (logs, cache) |
| **DTOs** | Objetos que definem a forma dos dados trafegados entre camadas |

### 2.3 Ecossistema

- **ORM/Banco de dados:** TypeORM, Prisma, Mongoose (MongoDB)
- **Autenticação:** Passport.js + JWT
- **Documentação:** Swagger (OpenAPI) integrado
- **Testes:** Jest (embutido), Supertest
- **Microsserviços:** suporte nativo a RabbitMQ, Kafka, Redis, gRPC

### 2.4 Vantagens e Desvantagens

| ✅ Vantagens | ❌ Desvantagens |
|---|---|
| Arquitetura opinada e escalável | Mais verboso para projetos pequenos |
| TypeScript nativo (tipagem forte) | Curva de aprendizado maior (decorators, IoC) |
| Suporte a múltiplos protocolos | Overhead para APIs simples |
| Documentação oficial excelente | Requer conhecimento sólido de POO |

---

## 3. React + NestJS: Uso Combinado (Full-Stack)

A combinação **React (front-end) + NestJS (back-end)** é uma das stacks mais adotadas no mercado para aplicações modernas:

```
[ Usuário ] ──► [ React SPA ] ──► [ NestJS API REST/GraphQL ] ──► [ Banco de Dados ]
```

- O React consome endpoints REST ou GraphQL expostos pelo NestJS via `fetch` ou Axios.
- O NestJS valida, processa e persiste os dados, retornando respostas tipadas.
- Ambos utilizam **TypeScript**, facilitando o compartilhamento de tipos entre front e back (monorepo com Nx ou Turborepo).

---

## 4. Comparativo Rápido

| Critério | React | NestJS |
|---|---|---|
| **Tipo** | Biblioteca front-end | Framework back-end |
| **Linguagem** | JavaScript / TypeScript | TypeScript |
| **Paradigma** | Componentes / Funcional | OOP + Funcional + Reativo |
| **Renderização** | Client-side (+ SSR via Next.js) | Servidor (Node.js) |
| **Curva de aprendizado** | Baixa a moderada | Moderada a alta |
| **Uso ideal** | Interfaces dinâmicas e SPAs | APIs REST, microsserviços, BFF |

---

## 5. Referências

- React Docs: <https://react.dev>
- NestJS Docs: <https://docs.nestjs.com>
- Node.js: <https://nodejs.org>
- TypeScript: <https://www.typescriptlang.org>
