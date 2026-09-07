<h1 align="center">Manoel Barros</h1>

<p align="center">
  <b>Full-Stack Developer</b> · <b>Backend Developer & Researcher at NUTES / UEPB</b><br>
  Cross-platform desktop apps · Production web SaaS on the edge · High-performance REST APIs · Healthcare VR & AI
</p>

<p align="center">
  <i>Desenvolvedor Full-Stack · Pesquisador no NUTES / UEPB — apps desktop multiplataforma, SaaS web em produção sobre infraestrutura serverless, APIs REST de alta performance e VR/IA para a saúde.</i>
</p>

<p align="center">
  Campina Grande, PB — Brazil
</p>

<p align="center">
  <a href="mailto:manoelneto400@gmail.com"><img src="https://img.shields.io/badge/Gmail-c14438?style=flat-square&logo=Gmail&logoColor=white" alt="Gmail"/></a>
  <a href="https://www.linkedin.com/in/manoelbcruz/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=Linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://painel-fatia-de-ouro.com.br/demo"><img src="https://img.shields.io/badge/Live_demo-Painel_Fatia_de_Ouro-D4A017?style=flat-square&logo=pwa&logoColor=white" alt="Live demo"/></a>
  <img src="https://komarev.com/ghpvc/?username=manoelbcruz&style=flat-square&color=blueviolet&label=profile+views" alt="profile views"/>
</p>

---

## About me

Computer Science undergraduate at **UEPB** (Campus I) — since 2022.
**Backend Developer** and undergraduate researcher (**PIBIC / FAPESQ-PB**) at **NUTES — Center for Strategic Health Technologies**, working across the **Usability & Human Factors Lab** and the **Biomedical Computing Lab**.

I build **cross-platform desktop applications** (C# / .NET / Avalonia), **high-performance REST APIs** (ASP.NET Core and FastAPI), **web apps on serverless infrastructure** (React/TypeScript PWAs on Cloudflare Workers + Supabase) and **Virtual Reality experiences** for healthcare. I focus on clean code, well-separated architecture (**MVVM**, **Clean Architecture**), agile delivery (**Scrum**), security by design (**Row-Level Security**, least privilege, threat modeling) and disciplined review before every delivery.

### Featured — Fatia de Ouro *(freelance · in production)*

**A complete retail platform for a bakery**, designed, built and shipped end to end by me, and **running the client's business today**: a desktop POS on the store counter, a mobile dashboard in the owner's pocket, and my own licensing/billing backend behind both.

#### POS + ERP — desktop

Shipped as a **self-contained single Windows executable** (Inno Setup installer): the owner installs and runs it with no extra runtime.

- **Full POS** with keyboard shortcuts and barcode scanner, designed for a non-technical operator.
- **Products, Inventory, Expenses, Production (PCP) and Reports** modules, with a daily production ledger that has to balance to the unit.
- **Optimized for low-end hardware** (4 GB RAM, 1024×768 display) — list virtualization, DB-side paging, short-lived `DbContext`.
- **BCrypt authentication** and owner approval of sensitive actions via **email token** (MailKit).
- **MVVM** architecture with dependency injection; persistence on **SQLite + EF Core 9** (WAL mode); `decimal` everywhere money or stock is involved.

`C#` · `.NET` · `Avalonia UI` · `MVVM` · `EF Core 9` · `SQLite` · `MailKit` · `BCrypt` · `Inno Setup`

#### Painel do Dono — the owner's dashboard *(new · live)*

[**painel-fatia-de-ouro.com.br**](https://painel-fatia-de-ouro.com.br)

A **mobile-first PWA** where the owner sees the day from the phone: sales, expenses, balance, production and the product's signature metric, *production yield*.

- **Read-only by design** — the POS computes every number and pushes ready daily aggregates through a Postgres RPC; the dashboard only presents them, so a business rule can never be born in SQL or in the front-end.
- **Row-Level Security per store** — tenant isolation verified in production against three real stores; the service key exists in one place only, the jobs service.
- **Analytics the owner actually asks for**: production yield, ABC curve, hourly heatmap, records, goals and *where the margin leaks* (discounts and cancellations per product).
- **Unattended jobs** (daily summary, stale-sync alert, monthly report, capacity monitor) in **FastAPI on Render**, woken by two redundant crons — GitHub Actions and a Cloudflare Worker — with idempotent transactional email through **Resend**.
- Deployed as a **Cloudflare Worker with static assets** on its own domain, with a CSP that allows no third parties and no business data left on the device.
- A **self-feeding public demo**: a deterministic generator writes a fresh day every night, so anyone can walk the real product without an account.

`React 19` · `TypeScript` · `Vite` · `Tailwind v4` · `Recharts` · `Vitest` · `Supabase (PostgreSQL · RLS · RPC)` · `Cloudflare Workers` · `FastAPI` · `Render` · `GitHub Actions`

#### Licensing & recurring billing

Cloud licensing with **automated recurring billing** (Supabase + Cloudflare Worker + payment-gateway webhooks), **signed license attestation** and **offline-first resilience**: three synchronized sources of truth (cloud primary, edge backup, local SQLite) reconciled by last-write-wins, so the store keeps selling with the internet down.

`Supabase` · `Cloudflare Workers` · `D1` · `SQLite` · `Webhooks` · `Cryptographic signing`

### Other projects & experience

| Project | Core stack |
|---|---|
| **Usability measurement (UX)** — client-server system to run usability performance tests, with a directed graph of the whole user path | `ASP.NET Core` · `JWT` · `EF Core` · `PostgreSQL` · `Docker` · `Avalonia UI` |
| **Virtual plenary** — multi-tenant voting-session system with per-session rules, public live panel and a hash-chained audit trail | `FastAPI` · `PostgreSQL (RLS)` · `React` · `TypeScript` · `Docker` · `TOTP 2FA` |
| **VR palliative-care trainer** — real-time voice conversation with an AI-driven patient NPC, one psychological persona per session | `Unity` · `Meta Quest (XR)` · `Python` · `Gemini Live API` · `WebSocket` |
| **Mixed-reality clinical software** — AI-assisted reading/storage of multiparametric monitor data, with audio/video streaming | `Python` · `FastAPI` · `Pydantic` · `JWT` · `Docker` |
| **VR cognitive/motor rehab** — application for elderly patients, with sessions operated remotely by the therapist | `Unity` · `Meta Quest (XR)` · `REST` · `WebSocket` |

> All projects have **private source code** (client and research work).

### Currently learning
- **Security by design** — Postgres RLS, least privilege, threat modeling and adversarial code review
- **Edge & serverless** architecture (Cloudflare Workers, Supabase, scheduled jobs that run unattended)
- System design & **Clean Architecture**
- Robust **REST APIs** (ASP.NET Core & FastAPI)
- **DevOps**: Docker, GitHub Actions and observability of what nobody is watching

<br>

<details>
<summary><b>Ler em Português</b></summary>

<br>

Graduando em **Ciência da Computação** na **UEPB** (Campus I) — desde 2022.
**Desenvolvedor Backend** e pesquisador de iniciação científica (**PIBIC / FAPESQ-PB**) no **NUTES — Núcleo de Tecnologias Estratégicas em Saúde**, atuando entre o **Laboratório de Usabilidade e Fatores Humanos** e o **Laboratório de Computação Biomédica**.

Construo **aplicações desktop multiplataforma** (C# / .NET / Avalonia), **APIs REST** de alta performance (ASP.NET Core e FastAPI), **aplicações web sobre infraestrutura serverless** (PWA em React/TypeScript na Cloudflare Workers + Supabase) e **experiências em Realidade Virtual** para a área da saúde. Trabalho com foco em código limpo, arquitetura bem dividida (**MVVM**, **Clean Architecture**), entrega ágil (**Scrum**), segurança desde o desenho (**Row-Level Security**, menor privilégio, modelagem de ameaças) e revisão disciplinada antes de cada entrega.

#### Destaque — Fatia de Ouro *(freelance · em produção)*

**Uma plataforma completa de varejo para uma loja de bolos**, do desenho à entrega, feita inteira por mim e **rodando o negócio do cliente hoje**: o PDV desktop no balcão, o painel no celular do dono e, atrás dos dois, o meu próprio backend de licenciamento e cobrança.

##### PDV + ERP — desktop

Distribuído como um **executável único autocontido para Windows** (instalador Inno Setup): o lojista instala e usa, sem runtime à parte.

- **PDV completo** com atalhos de teclado e leitor de código de barras, desenhado para um operador não-técnico.
- Módulos de **Produtos, Estoque, Despesas, Produção (PCP) e Relatórios**, com um controle diário de produção que precisa fechar na unidade.
- **Otimizado para hardware modesto** (4 GB de RAM, tela 1024×768) — virtualização de listas, paginação no banco e `DbContext` de vida curta.
- **Autenticação com BCrypt** e aprovações sensíveis do dono via **token enviado por e-mail** (MailKit).
- Arquitetura **MVVM** com injeção de dependência; persistência em **SQLite + EF Core 9** (modo WAL); `decimal` em tudo que é dinheiro ou estoque.

`C#` · `.NET` · `Avalonia UI` · `MVVM` · `EF Core 9` · `SQLite` · `MailKit` · `BCrypt` · `Inno Setup`

##### Painel do Dono — o painel do lojista *(novo · no ar)*

[**painel-fatia-de-ouro.com.br**](https://painel-fatia-de-ouro.com.br)

Um **PWA mobile-first** onde o dono vê o dia pelo celular: vendas, despesas, saldo, produção e a métrica que dá identidade ao produto, o *aproveitamento da produção*.

- **Read-only por desenho** — o PDV calcula todos os números e empurra agregados diários prontos por uma RPC no Postgres; o painel só apresenta, então regra de negócio nunca nasce no SQL nem no front.
- **Row-Level Security por loja** — isolamento entre lojas verificado em produção com três lojas reais; a chave de serviço existe num lugar só, o serviço de jobs.
- **As análises que o dono realmente pede**: aproveitamento da produção, curva ABC, mapa de calor por horário, recordes, metas e *onde a margem escapa* (desconto e cancelamento por produto).
- **Rotinas automáticas** (resumo diário, alerta de loja sem sincronizar, relatório mensal, monitor de capacidade) em **FastAPI no Render**, acordadas por dois crons redundantes — GitHub Actions e um Worker da Cloudflare — com e-mail transacional idempotente via **Resend**.
- Publicado como **Worker da Cloudflare com assets estáticos** em domínio próprio, com CSP que não libera terceiros e nenhum dado do negócio guardado no aparelho.
- Uma **demonstração pública que se alimenta sozinha**: um gerador determinístico escreve um dia novo toda madrugada, então qualquer pessoa percorre o produto real sem criar conta.

`React 19` · `TypeScript` · `Vite` · `Tailwind v4` · `Recharts` · `Vitest` · `Supabase (PostgreSQL · RLS · RPC)` · `Cloudflare Workers` · `FastAPI` · `Render` · `GitHub Actions`

##### Licenciamento e cobrança recorrente

Licenciamento em nuvem com **cobrança recorrente automatizada** (Supabase + Worker da Cloudflare + webhooks do gateway de pagamento), **atestado de licença assinado** e **resiliência offline-first**: três fontes de verdade sincronizadas (nuvem primária, backup na borda, SQLite local) reconciliadas por *last-write-wins*, para a loja continuar vendendo com a internet fora.

`Supabase` · `Cloudflare Workers` · `D1` · `SQLite` · `Webhooks` · `Assinatura criptográfica`

#### Outros projetos & experiência

| Projeto | Stack principal |
|---|---|
| **Mensuração de usabilidade (UX)** — sistema cliente-servidor para conduzir testes de desempenho, com grafo direcionado de todo o percurso do voluntário | `ASP.NET Core` · `JWT` · `EF Core` · `PostgreSQL` · `Docker` · `Avalonia UI` |
| **Plenário virtual** — sistema multi-tenant de sessões de votação com regras configuráveis por sessão, painel público em tempo real e trilha de auditoria encadeada por hash | `FastAPI` · `PostgreSQL (RLS)` · `React` · `TypeScript` · `Docker` · `2FA TOTP` |
| **Treinamento VR em cuidados paliativos** — conversa por voz, em tempo real, com um paciente NPC conduzido por IA, uma persona psicológica por sessão | `Unity` · `Meta Quest (XR)` · `Python` · `Gemini Live API` · `WebSocket` |
| **Software clínico de realidade mista** — leitura/armazenamento de dados de monitores multiparamétricos com apoio de IA e transmissão de áudio/vídeo | `Python` · `FastAPI` · `Pydantic` · `JWT` · `Docker` |
| **Reabilitação cognitiva/motora em VR** — aplicação para idosos, com sessões operadas remotamente pelo terapeuta | `Unity` · `Meta Quest (XR)` · `REST` · `WebSocket` |

> Todos os projetos têm **código-fonte privado** (clientes e pesquisa).

#### Atualmente aprofundando
- **Segurança desde o desenho** — RLS no Postgres, menor privilégio, modelagem de ameaças e revisão adversarial
- Arquitetura **serverless e de borda** (Cloudflare Workers, Supabase, rotinas que rodam sem ninguém olhando)
- Arquitetura de sistemas e **Clean Architecture**
- **APIs REST** robustas (ASP.NET Core & FastAPI)
- **DevOps**: Docker, GitHub Actions e observabilidade do que roda desacompanhado

</details>

---

## Tech Stack

**Desktop & .NET**
<br>
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=c-sharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-5C2D91?style=flat-square&logo=dotnet&logoColor=white)
![.NET MAUI](https://img.shields.io/badge/.NET%20MAUI-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Avalonia UI](https://img.shields.io/badge/Avalonia_UI-111111?style=flat-square&logo=avalonia&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity%20Framework-442B6E?style=flat-square)

**Python & Backend**
<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat-square&logo=fastapi)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white)
![Poetry](https://img.shields.io/badge/Poetry-%233B82F6.svg?style=flat-square&logo=poetry&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-6BA81E?style=flat-square)
![REST API](https://img.shields.io/badge/REST_API-02569B?style=flat-square&logo=json&logoColor=white)
![Beanie](https://img.shields.io/badge/Beanie-ODM-black?style=flat-square)
![Motor](https://img.shields.io/badge/Motor-Driver-green?style=flat-square)

**Web & JavaScript**
<br>
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat-square&logo=pwa&logoColor=white)

**VR, AI & Game Engine**
<br>
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)
![Meta Quest](https://img.shields.io/badge/Meta%20Quest%20(XR)-1C1E20?style=flat-square&logo=meta&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini%20Live-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)

**Databases**
<br>
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=flat-square&logo=microsoft-sql-server&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=flat-square&logo=sqlite&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

**DevOps & Cloud**
<br>
![Docker](https://img.shields.io/badge/Docker-%230db7ed.svg?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-%23F05033.svg?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare%20Workers-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Render](https://img.shields.io/badge/Render-000000?style=flat-square&logo=render&logoColor=white)

**Other languages**
<br>
![Java](https://img.shields.io/badge/Java-red?style=flat-square&logo=java)
![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)

---

## 📊 GitHub Stats

<div align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=manoelbcruz&show_icons=true&theme=radical&hide_border=true&count_private=true" alt="GitHub Stats"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=manoelbcruz&layout=compact&theme=radical&hide_border=true" alt="Top Languages"/>
</div>
