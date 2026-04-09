<div align="center">

<br/>

```
███╗   ███╗ ██████╗ ███████╗ █████╗ ██╗   ██╗ ██████╗ █████╗
████╗ ████║██╔═══██╗╚══███╔╝██╔══██╗╚██╗ ██╔╝██╔════╝██╔══██╗
██╔████╔██║██║   ██║  ███╔╝ ███████║ ╚████╔╝ ██║     ███████║
██║╚██╔╝██║██║   ██║ ███╔╝  ██╔══██║  ╚██╔╝  ██║     ██╔══██║
██║ ╚═╝ ██║╚██████╔╝███████╗██║  ██║   ██║   ╚██████╗██║  ██║
╚═╝     ╚═╝ ╚═════╝ ╚══════╝╚═╝  ╚═╝   ╚═╝    ╚═════╝╚═╝  ╚═╝
```

**Plataforma digital multidisciplinar para artistas independentes**

[![Status](https://img.shields.io/badge/status-MVP%20em%20desenvolvimento-C8A96E?style=flat-square)](.)
[![React](https://img.shields.io/badge/React-18.x-61DAFB?style=flat-square&logo=react)](https://react.dev)
[![Next.js](https://img.shields.io/badge/Next.js-14.x-white?style=flat-square&logo=nextdotjs&logoColor=white)](https://nextjs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=flat-square&logo=typescript)](https://www.typescriptlang.org)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15.x-336791?style=flat-square&logo=postgresql)](https://www.postgresql.org)
[![License](https://img.shields.io/badge/licença-MIT-green?style=flat-square)](LICENSE)

<br/>

[🎨 Ver Demo](#) · [📄 Documentação](#documentação) · [🐛 Reportar Bug](../../issues) · [✨ Sugerir Feature](../../issues)

<br/>

</div>

---

## ✦ Sobre o Projeto

**Mozayca** é uma plataforma de arte digital que reúne criadores de múltiplas linguagens artísticas em um único ecossistema. O nome remete ao mosaico — fragmentos distintos que, juntos, formam algo belo e coeso.

Artistas podem publicar suas obras, ganhar visibilidade, interagir com a comunidade, realizar lives, compartilhar materiais (presets, plugins, partituras) e acompanhar rankings atualizados por IA — tudo em um ambiente seguro, dinâmico e focado exclusivamente na arte.

```
Artes Visuais · Cinema · Música · Dança · Teatro · Fotografia
```

<br/>

## 🗂️ Estrutura do Repositório

```
mozayca/
├── apps/
│   ├── web/                  # Frontend Next.js 14 (App Router)
│   └── mobile/               # App React Native + Expo
├── packages/
│   ├── ui/                   # Design system compartilhado
│   └── types/                # Tipos TypeScript compartilhados
├── services/
│   ├── auth-service/         # Autenticação, JWT, OAuth2
│   ├── user-service/         # Perfis, seguidores
│   ├── content-service/      # Posts, uploads, coleções
│   ├── feed-service/         # Feed personalizado
│   ├── ranking-service/      # Rankings periódicos por categoria
│   ├── chat-service/         # Mensagens em tempo real
│   ├── live-service/         # Transmissões ao vivo
│   ├── notification-service/ # Push, e-mail, in-app
│   ├── search-service/       # Elasticsearch + busca semântica
│   ├── media-service/        # Transcodificação de mídia (FFmpeg)
│   └── ai-service/           # Moderação, recomendação, NLP
├── infra/
│   ├── terraform/            # IaC — provisionamento AWS
│   ├── k8s/                  # Manifestos Kubernetes
│   └── docker/               # Dockerfiles por serviço
├── docs/
│   └── Mozayca_Documentacao_Tecnica.docx
├── prototype/
│   └── mozayca-mvp.jsx       # Protótipo interativo React (MVP)
└── README.md
```

<br/>

## 🚀 Stack Tecnológica

### Frontend
| Tecnologia | Versão | Uso |
|---|---|---|
| Next.js | 14.x | App web com SSR e App Router |
| React | 18.x | Biblioteca UI principal |
| TypeScript | 5.x | Tipagem estática |
| TailwindCSS | 3.x | Estilização utilitária |
| Zustand | 4.x | Gerenciamento de estado |
| TanStack Query | 5.x | Cache e sync de dados |
| Socket.io-client | 4.x | WebSockets (chat, lives) |
| Framer Motion | 11.x | Animações |

### Mobile
| Tecnologia | Versão | Uso |
|---|---|---|
| React Native | 0.74.x | App iOS e Android |
| Expo | 51.x | Build e OTA updates |
| React Navigation | 6.x | Navegação nativa |

### Backend
| Tecnologia | Versão | Uso |
|---|---|---|
| Node.js | 20 LTS | Runtime principal |
| NestJS | 10.x | Framework modular de API |
| Python | 3.12 | Serviços de IA/ML |
| FastAPI | 0.111.x | API do ai-service |
| Prisma ORM | 5.x | Acesso ao banco de dados |
| PostgreSQL | 15.x | Banco de dados principal (SQL) |
| Redis | 7.x | Cache, filas, rankings |
| Elasticsearch | 8.x | Busca full-text e semântica |
| Socket.io | 4.x | WebSockets |
| BullMQ | 5.x | Filas assíncronas |

### Infraestrutura
| Tecnologia | Uso |
|---|---|
| AWS (EKS + S3 + CloudFront + IVS) | Hospedagem, mídia e streaming |
| Docker + Kubernetes | Containerização e orquestração |
| Terraform | Infraestrutura como código |
| GitHub Actions | CI/CD |
| Datadog + Sentry | Monitoramento e erros |
| Cloudflare | CDN e WAF |

<br/>

## 🤖 Inteligência Artificial

A Mozayca utiliza IA em quatro frentes principais:

| Módulo | Tecnologia | Função |
|---|---|---|
| **Moderação automática** | AWS Rekognition + NSFW.js | Filtra conteúdo impróprio antes da publicação |
| **Feed personalizado** | LightFM / Surprise (Python) | Recomenda obras com base no histórico do usuário |
| **Busca semântica** | Sentence-Transformers + ES KNN | Busca por descrição em linguagem natural |
| **Legendas automáticas** | OpenAI Whisper | Transcrição e acessibilidade em vídeos |
| **Rankings dinâmicos** | Modelo customizado de engajamento | Atualiza posições por categoria (diário/semanal/mensal) |

<br/>

## 🎯 Funcionalidades do MVP

O protótipo interativo (`prototype/mozayca-mvp.jsx`) cobre:

- [x] Feed com as 6 categorias artísticas
- [x] Stories horizontais por artista
- [x] Busca em tempo real por obra, artista ou tag
- [x] Curtir, comentar e salvar obras
- [x] Página de perfil do artista
- [x] Sistema de seguir/deixar de seguir
- [x] Rankings por categoria (diário/semanal/mensal)
- [x] Chat privado com histórico de mensagens
- [x] Notificações com badge e marcação de leitura
- [x] Modal de publicação com seleção de tipo e categoria
- [ ] Transmissões ao vivo *(próxima sprint)*
- [ ] Stories funcionais com expiração *(próxima sprint)*
- [ ] Autenticação real (JWT + OAuth2) *(fase 2)*
- [ ] Upload de mídia com processamento *(fase 2)*
- [ ] Recomendação por IA *(fase 3)*

<br/>

## ⚡ Como Executar o Protótipo

### Pré-requisitos

- Node.js 20+
- npm ou yarn

### Rodando localmente

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/mozayca.git
cd mozayca

# Entre na pasta do protótipo
cd prototype

# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm run dev
```

Acesse `http://localhost:3000` no navegador.

### Via CodeSandbox / StackBlitz

Importe o arquivo `prototype/mozayca-mvp.jsx` diretamente em qualquer sandbox React para rodar sem instalação.

<br/>

## 🗓️ Roadmap

```
Fase 1 — Descoberta e Design          Semanas  1–6   ████████░░░░░░░░  ✅
Fase 2 — Fundação Técnica             Semanas  7–14  ░░░░░░░░░░░░░░░░  🔜
Fase 3 — Core da Plataforma           Semanas 15–26  ░░░░░░░░░░░░░░░░  🔜
Fase 4 — Funcionalidades Avançadas    Semanas 27–38  ░░░░░░░░░░░░░░░░  🔜
Fase 5 — Qualidade e Lançamento       Semanas 39–48  ░░░░░░░░░░░░░░░░  🔜
```

Prazo total estimado: **12 meses** para o lançamento da v1.0.

<br/>

## 🏗️ Arquitetura

A Mozayca é construída sobre uma **arquitetura de microsserviços** com comunicação via REST e mensageria assíncrona (Kafka/RabbitMQ). Cada domínio funcional é um serviço independente, garantindo escalabilidade horizontal e isolamento de falhas.

```
                        ┌─────────────────┐
          Web / Mobile  │   API Gateway   │  Rate limiting · Auth · Roteamento
                        └────────┬────────┘
                                 │
          ┌──────────┬───────────┼───────────┬──────────┐
          ▼          ▼           ▼           ▼          ▼
     auth-svc   user-svc   content-svc  feed-svc  ranking-svc
          │          │           │           │          │
          └──────────┴───────────┴───────────┴──────────┘
                                 │
                    ┌────────────┼────────────┐
                    ▼            ▼            ▼
               PostgreSQL      Redis     Elasticsearch
               (dados SQL)    (cache)     (busca)
                                 │
                    ┌────────────┼────────────┐
                    ▼            ▼            ▼
              media-svc      ai-svc       live-svc
              (FFmpeg)    (Python/ML)   (AWS IVS)
                    │
              AWS S3 + CloudFront CDN
```

<br/>

## 🔒 Segurança e Moderação

A plataforma adota um modelo de moderação em três camadas:

1. **IA automática** — AWS Rekognition analisa todo conteúdo enviado antes da publicação
2. **Comunidade** — botão de denúncia em todas as publicações com SLA de revisão em 24h
3. **Equipe humana** — painel interno de trust & safety para casos escalados

Conformidade com **LGPD** (Lei 13.709/2018): exportação e exclusão de dados pelo próprio usuário, consentimento explícito e Privacy by Design desde o início.

<br/>

## 🤝 Como Contribuir

Contribuições são bem-vindas! Veja como participar:

```bash
# 1. Fork o repositório
# 2. Crie sua branch
git checkout -b feature/minha-feature

# 3. Faça suas alterações e commit
git commit -m "feat: adiciona funcionalidade X"

# 4. Envie para sua branch
git push origin feature/minha-feature

# 5. Abra um Pull Request
```

Por favor, leia o [CONTRIBUTING.md](CONTRIBUTING.md) antes de enviar um PR e siga o padrão de commits [Conventional Commits](https://www.conventionalcommits.org/pt-br/).

<br/>

## 📄 Documentação

A documentação técnica completa do projeto está disponível em:

- [`docs/Mozayca_Documentacao_Tecnica.docx`](docs/Mozayca_Documentacao_Tecnica.docx) — documento Word com requisitos, arquitetura, modelagem de banco, cronograma, stack detalhada, gestão de riscos e métricas de sucesso.

<br/>

## 📜 Licença

Distribuído sob a licença MIT. Veja [`LICENSE`](LICENSE) para mais informações.

<br/>

---

<div align="center">

feito com ✦ pela equipe Mozayca

*"Da mesma forma que um mosaico — fragmentos distintos que, juntos, formam algo belo."*

</div>
