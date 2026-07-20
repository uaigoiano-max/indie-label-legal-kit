# 🎼 Indie Label Legal Kit

### Kit de automação jurídica para selos independentes, editoras e artistas

---

## ⚠️ Aviso Legal

Este projeto **não substitui aconselhamento jurídico profissional**. Os templates, cláusulas e fluxos aqui presentes são pontos de partida estruturados para acelerar a criação e revisão de contratos musicais — não são, em nenhuma hipótese, minutas prontas para assinatura.

Antes de usar qualquer documento gerado a partir deste kit:

- Revise com um advogado licenciado na jurisdição aplicável ao seu contrato;
- Adapte valores, prazos e territórios ao caso concreto;
- Verifique a legislação local, já que direitos autorais e contratos musicais variam significativamente entre países.

Os mantenedores deste repositório não se responsabilizam por contratos gerados, adaptados ou assinados com base neste material.

---

## 🎯 O que é o Indie Label Legal Kit

O **Indie Label Legal Kit** é um conjunto estruturado de instruções, templates e cláusulas modulares, desenhado para funcionar como uma *Skill* de IA (compatível com agentes como o Claude) especializada em contratos da indústria musical.

Ele ajuda a:

- Padronizar a criação de contratos (artista, fonograma, publishing, sincronização, NDA);
- Revisar contratos existentes e identificar riscos e lacunas;
- Estruturar deals com clareza sobre direitos, remuneração e prazos;
- Apoiar negociações com diferentes posturas, conforme o contexto do acordo;
- Trabalhar em português e inglês, com templates bilíngues prontos para operações internacionais.

## 🧩 Para quem é este projeto

- **Selos independentes** que precisam de contratos padronizados sem depender de um departamento jurídico interno;
- **Editoras musicais** pequenas e médias que administram catálogos próprios ou de terceiros;
- **Artistas e managers** que querem entender melhor o que estão prestes a assinar antes de negociar;
- **Desenvolvedores** construindo ferramentas jurídicas ou agentes de IA para o mercado musical.

---

## 🏗️ Arquitetura do sistema

O kit é organizado em **camadas independentes e integráveis**, cada uma com uma função clara dentro do fluxo jurídico:

```
indie-label-legal-kit/
│
├── .claude-plugin/
│   └── marketplace.json         → manifesto da marketplace (instalação via /plugin)
│
├── plugins/
│   └── indie-label-legal-kit/
│       ├── .claude-plugin/
│       │   └── plugin.json      → manifesto do plugin
│       │
│       └── skills/
│           └── legal-kit/
│               ├── SKILL.md                     → núcleo de regras e comportamento da IA
│               │
│               ├── agents/                      → como a IA pensa e age
│               │   ├── contract_writer.md
│               │   ├── contract_reviewer.md
│               │   ├── legal_strategist.md
│               │   └── negotiation_engine.md
│               │
│               ├── scripts/                      → como a tarefa é executada, passo a passo
│               │   ├── contract_generation.md
│               │   ├── contract_analysis.md
│               │   ├── deal_structuring.md
│               │   └── negotiation_protocol.md
│               │
│               ├── templates/                    → base contratual por tipo de contrato
│               │   ├── artist_agreement_aggressive.md
│               │   ├── artist_agreement_balanced.md
│               │   ├── artist_agreement_friendly.md
│               │   ├── phonogram_agreement.md
│               │   ├── publishing_agreement.md
│               │   ├── distribution_agreement.md
│               │   ├── rights_management_agreement.md
│               │   ├── sync_license.md
│               │   ├── sync_license_advanced.md
│               │   ├── split_sheet.md
│               │   └── nda.md
│               │
│               ├── templates_bilingual/          → versões PT/EN para operações internacionais
│               │   ├── artist_agreement_bilingual.md
│               │   ├── phonogram_agreement_bilingual.md
│               │   ├── publishing_agreement_bilingual.md
│               │   └── sync_license_bilingual.md
│               │
│               ├── clauses/                      → biblioteca modular de cláusulas reutilizáveis
│               │   ├── royalties.md
│               │   ├── recoup.md
│               │   ├── audit.md
│               │   ├── liability.md
│               │   └── termination.md
│               │
│               └── references/                   → base de conhecimento jurídico
│                   ├── internal_playbook.md
│                   ├── market_practices.md
│                   ├── revenue_flows.md
│                   ├── risk_matrix.md
│                   ├── legal_framework.md
│                   ├── legal_identity.md          → template de identidade da sua empresa
│                   └── legal_library/
│                       ├── public_official/       → legislação e normas oficiais
│                       ├── public_sanitized/       → padrões de mercado, anonimizados
│                       ├── extended/               → cláusulas avançadas de referência
│                       ├── licensed/                → estrutura para materiais licenciados (uso privado)
│                       ├── own_contracts/           → seus próprios contratos (privado, fora do Git por padrão)
│                       └── intake_policy.md         → regras de governança da biblioteca
│
├── LICENSE
├── .gitignore
└── README.md
```

---

## ⚙️ Fluxo operacional

```
ENTRADA (tipo de contrato, partes, território, idioma)
        ↓
SKILL.md            → regras gerais
        ↓
AGENT               → define comportamento (escrever, revisar, negociar, estruturar)
        ↓
SCRIPT              → executa o passo a passo
        ↓
TEMPLATE            → estrutura base do contrato
        ↓
CLAUSES             → refinamento com cláusulas modulares
        ↓
LEGAL LIBRARY       → consulta à base de conhecimento
        ↓
VALIDAÇÃO FINAL     → checagem de consistência e lacunas
        ↓
SAÍDA (contrato ou análise pronta para revisão humana)
```

---

## 🧠 As camadas em detalhe

### 1. Camada de inteligência — `SKILL.md`
O núcleo do sistema: define as regras jurídicas gerais, prioridades e o comportamento geral da IA ao lidar com qualquer solicitação contratual.

### 2. Camada de comportamento — `agents/`
Define **como a IA age** em cada tipo de tarefa:

| Agente | Função |
|---|---|
| `contract_writer` | Redige contratos completos a partir de templates e cláusulas |
| `contract_reviewer` | Analisa contratos existentes, identifica riscos e sugere correções |
| `legal_strategist` | Estrutura operações e deals do ponto de vista jurídico-estratégico |
| `negotiation_engine` | Recomenda a postura de negociação mais adequada ao contexto |

### 3. Camada de execução — `scripts/`
Define **o passo a passo** de cada tarefa: geração de contrato, análise jurídica, estruturação de deal e protocolo de negociação.

### 4. Camada de estrutura — `templates/`
A base contratual, cobrindo os principais tipos de acordo do mercado musical: contrato de artista, fonograma, publishing, sincronização, distribuição, gestão de direitos, split sheet e NDA.

### 5. Camada internacional — `templates_bilingual/`
Versões adaptadas para operações globais, com estrutura bilíngue (PT/EN) pensada para contratos com contrapartes estrangeiras.

### 6. Camada de precisão — `clauses/`
Biblioteca modular de cláusulas reutilizáveis (royalties, recoup, auditoria, responsabilidade, rescisão), que podem ser inseridas em qualquer template conforme o caso.

### 7. Camada de conhecimento — `references/legal_library/`
Base de inteligência jurídica, organizada por origem e nível de uso permitido:

- **`public_official/`** — legislação e normas de domínio público (ex.: Lei 9.610/98, LGPD, funcionamento do ECAD);
- **`public_sanitized/`** — padrões de mercado e estruturas de contrato genéricas, sem dados de terceiros;
- **`extended/`** — cláusulas avançadas de referência (governing law, arbitragem, monetização, tecnologias futuras);
- **`licensed/`** — pasta reservada para materiais obtidos de terceiros com autorização; **conteúdo aqui nunca deve ser redistribuído publicamente** sem confirmação explícita da licença de uso.

### 8. Camada estratégica — `references/internal_playbook.md`
Orienta quando usar cada postura de negociação (`aggressive`, `balanced`, `friendly`) conforme o contexto do próprio deal — por exemplo, volume de investimento envolvido, tipo de relação (pontual vs. contínua) e grau de urgência — e não como uma régua fixa baseada no porte da outra parte.

### 9. Camada de validação
Aplicada ao final de qualquer saída do sistema, garantindo:

- consistência jurídica entre as cláusulas usadas;
- ausência de lacunas essenciais (partes, objeto, prazo, remuneração, rescisão);
- alinhamento com a postura de negociação escolhida.

---

## 🎚️ Posturas de negociação

O kit oferece três posturas configuráveis para templates de contrato, escolhidas conforme o contexto do acordo — não conforme o poder de barganha da outra parte:

| Postura | Quando costuma fazer sentido |
|---|---|
| **Aggressive** | Alto investimento envolvido, risco elevado, necessidade de proteção reforçada |
| **Balanced** | Relações contínuas, deals de porte médio, equilíbrio entre as partes |
| **Friendly** | Parcerias de confiança já consolidada, flexibilidade prioritária sobre controle |

---

## ⚖️ Base jurídica de referência

O conteúdo do kit foi estruturado tendo como referência:

- Lei de Direitos Autorais (Lei nº 9.610/98 — Brasil);
- Práticas comuns da indústria musical internacional;
- Estruturas contratuais frequentemente usadas por gravadoras e editoras de grande porte;
- Modelo de arbitragem internacional (ICC) para contratos multijurisdicionais.

Isso **não significa** que o conteúdo seja válido automaticamente em qualquer país — sempre confirme a legislação local antes de usar.

---

## 🔐 Governança do repositório

- Nenhum documento com dados pessoais (CPF, RG, endereço, dados bancários etc.) deve ser incluído em qualquer pasta deste repositório;
- Todo material incluído em `legal_library/` deve ter origem identificável;
- Conteúdo classificado como `licensed/` nunca deve ser redistribuído publicamente sem autorização confirmada;
- Contribuições devem manter a estrutura modular (agente → script → template → cláusula → referência).

---

## 🚀 Como usar

### Opção A — Instalar como plugin do Claude Code (recomendado, com atualizações automáticas)

Este repositório já está estruturado como uma **Plugin Marketplace** do Claude Code. Para instalar:

```
/plugin marketplace add uaigoiano-max/indie-label-legal-kit
/plugin install indie-label-legal-kit@indie-label-legal-kit
```

A partir daí, o Claude Code passa a atualizar automaticamente a marketplace e o plugin em segundo plano — quando sair uma nova versão do kit, ela chega para quem instalou sem precisar refazer nada manualmente (pode ser necessário rodar `/reload-plugins` quando avisado, ou reiniciar a sessão). Para ativar isso manualmente também: rode `/plugin`, vá em **Marketplaces**, selecione o `indie-label-legal-kit` e habilite **Enable auto-update**.

### Opção B — Uso manual (Claude Projects, Claude Desktop, ou outro agente)

1. Baixe ou clone o repositório;
2. Aponte seu agente de IA para a pasta `plugins/indie-label-legal-kit/skills/legal-kit/` (onde está o `SKILL.md`);
3. Descreva o caso: tipo de contrato, partes envolvidas, território, idioma e postura de negociação desejada;
4. O agente seleciona o template adequado, aplica as cláusulas necessárias e consulta a base de conhecimento;
5. Revise a saída com atenção — e sempre com apoio jurídico profissional antes de qualquer assinatura.

### Alimentando o agente com seus próprios contratos

Cole seus contratos já praticados (anonimizados) em `plugins/indie-label-legal-kit/skills/legal-kit/references/legal_library/own_contracts/` — essa pasta fica de fora do controle de versão por padrão (`.gitignore`), então o agente aprende o seu padrão sem que isso vaze para o repositório público.

---

## 🤝 Contribuindo

Contribuições são bem-vindas, especialmente:

- Novas cláusulas modulares para cenários específicos (ex.: NFTs, licenciamento para games, podcasts);
- Adaptações para outras jurisdições além do Brasil;
- Melhorias nos templates bilíngues;
- Correções e clareza na documentação.

Abra uma issue ou pull request descrevendo a mudança proposta.

---

## 📄 Licença

Este projeto é disponibilizado sob licença MIT — livre para uso, adaptação e redistribuição, mantendo o aviso legal e os créditos originais.

---

## 🙌 Créditos

Este projeto foi originalmente desenvolvido pela **Monkey In Space Music Group**, uma operação independente de gravadora e editora musical, que estruturou este sistema para uso interno antes de disponibilizá-lo à comunidade da indústria musical como ferramenta open-source.
