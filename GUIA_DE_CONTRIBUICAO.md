# 📖 Guia de Contribuição e Navegação — SenacOS

Este documento é a "Constituição" da organização: como participar, como ganhar seu broche de membro, como se organizar em times, como nomear e versionar seu projeto acadêmico, como usar o board ágil, e onde encontrar cada frente da comunidade.

---

## 1. Modelo de Membresia: Contribuidor x Membro

No GitHub existem dois níveis de relação com a nossa comunidade — entenda a diferença antes de começar:

| | **Contribuidor** | **Membro da Organização** |
|---|---|---|
| **Como participa** | Abre uma Issue, entra numa Discussion, ou envia um Pull Request em qualquer repositório público | Convite oficial para o quadro `People` |
| **Pré-requisito** | Nenhum — qualquer aluno (ou visitante externo) pode contribuir | Ter uma contribuição real reconhecida pela comunidade |
| **Onde aparece** | Card "Contributors" do repositório específico onde contribuiu | 🏅 Logo da SenacOS no perfil pessoal do GitHub |
| **Acesso interno** | Nenhum — participação pública padrão | Visibilidade/interação em espaços internos da organização |

Sua primeira contribuição não precisa ser um Pull Request de código. Corrigir um erro de digitação na Biblioteca Livre, responder uma dúvida numa Discussion, ou sugerir uma melhoria de documentação também conta. O que importa é contribuir de verdade — não o quão avançado você já é.

> ⚠️ **Atenção ao aceitar o convite de membro:** por padrão, o GitHub deixa sua filiação à organização como **Privada**. Para o broche aparecer no seu perfil, acesse a página da org → `People` → seu perfil → mude a visibilidade para **Public**.

---

## 2. Organização e Times (GitHub Teams)

A SenacOS usa **GitHub Teams** — no formato "flat" (sem hierarquia entre times) — para identificar grupos dentro da comunidade, de forma parecida com "roles" em servidores de comunidade. Isso não concede privilégios administrativos: é só uma forma de facilitar comunicação e notificação.

**Times previstos:**

| Time (abreviado) | Curso (nome completo) | Para que serve |
|---|---|---|
| `@SenacOS/professores` | — | Docentes convidados como referência técnica; dúvidas mais avançadas |
| `@SenacOS/dev-sistemas` | Análise e Desenvolvimento de Sistemas | Assuntos específicos do curso |
| `@SenacOS/ciencia-comp` | Ciência da Computação | Assuntos específicos do curso |
| `@SenacOS/eng-software` | Engenharia de Software | Assuntos específicos do curso |
| `@SenacOS/sistemas-info` | Sistemas de Informação | Assuntos específicos do curso |

> Novos times por curso podem ser criados conforme a organização crescer — a lista acima não é fechada. Os times usam sigla por convenção, para ficar consistente com o prefixo de nomenclatura dos repositórios acadêmicos (Seção 3) — a coluna "nome completo" acima serve de referência para quem ainda não decorou as siglas.

**Como marcar o time certo:**

Em qualquer Issue, Discussion ou Pull Request, mencione o time com `@SenacOS/nome-do-time` para notificar todos os seus integrantes de uma vez — por exemplo:

- Travou numa dúvida técnica mais avançada? `@SenacOS/professores`
- Quer que alguém do seu curso revise seu Pull Request? `@SenacOS/ads` (ou o time do seu curso)

**Descoberta para quem está fora da organização:**

Embora os times internos usem siglas, os repositórios acadêmicos recebem **Topics/Tags com o nome do curso por extenso** (ex.: `ciencia-da-computacao`, `analise-e-desenvolvimento-de-sistemas`) — assim, recrutadores e visitantes externos que não conhecem as abreviações da SenacOS ainda conseguem filtrar e encontrar projetos pelo nome completo do curso.

> 🚧 **Planejado:** um formulário de onboarding para novos membros, com checkbox de seleção do curso (por extenso), que os direciona automaticamente ao time correspondente na aceitação do convite.

---

## 3. Nomenclatura de Repositórios e Projetos Acadêmicos (Convenção de Nomes)

Cada projeto acadêmico deve viver em **seu próprio repositório individual** dentro da organização — nunca como uma pasta dentro de um repositório compartilhado. Isso evita conflitos de merge entre grupos diferentes e mantém as abas de Issues/Pull Requests/Projects utilizáveis pelos professores para avaliação individual de cada equipe.

**Formato obrigatório:**

```
[CURSO]-[SEMESTRE]-[NomeDoProjeto]
```

**CURSO:** sigla oficial do curso. A comunidade abraça todos os cursos de tecnologia, portanto a lista abaixo não é restritiva, mas serve de padrão para mantermos o ecossistema organizado utilizando as abreviações mais comuns do mercado:
- `ADS` — Análise e Desenvolvimento de Sistemas
- `CC` — Ciência da Computação
- `SI` — Sistemas de Informação
- `ES` — Engenharia de Software
- `EC` — Engenharia da Computação
- `RC` — Redes de Computadores
- `BD` — Banco de Dados
- `GTI` — Gestão da Tecnologia da Informação
- `STI` — Sistemas para Internet (ou SPI)

> A sigla do repositório deve ser curta conforme acima, independentemente de o time no GitHub possuir um nome mais extenso ou descritivo, como `@SenacOS/sistemas-info` ou `@SenacOS/eng-software`.

* **SEMESTRE:** número do semestre seguido de `S` — `1S`, `2S`, `3S`, etc.
* **NomeDoProjeto:** nome do projeto em `CamelCase`, sem espaços ou acentos.

**Exemplos:**

- `ADS-3S-ClinicaNutricao`
- `CC-1S-RpgTextual`
- `SI-2S-ControleEstoque`
- `ES-4S-SistemaDeVendas`

Esse padrão organiza a aba de repositórios em ordem alfabética por curso automaticamente, sem precisar de nenhuma ação manual de organização.

**Complemento de descoberta — Topics/Tags:**

Além do prefixo no nome, adicione **Topics** ao repositório no GitHub:
- O nome completo do curso (ex.: `ciencia-da-computacao`) — para visitantes externos, conforme decidido na Seção 2.
- O semestre (ex.: `3-semestre`).
- Tecnologias usadas (ex.: `spring-boot`, `angular`).

Isso permite filtrar a lista de repositórios da organização por tag, algo que a ordenação alfabética sozinha não resolve.

> 💡 **Repository Template:** para reduzir o atrito de quem está criando seu primeiro repositório, use o [`Template-Projeto-Academico`](https://github.com/SenacOS/Template-Projeto-Academico) como ponto de partida — ele já vem com `.gitignore`, licença MIT, `README.md` estruturado e Issue Templates de Módulo/Tarefa prontos. Clique em "Use this template", dê o nome já no formato acima, e o projeto nasce pronto.

**Autonomia de criação:** membros têm liberdade total para criar repositórios de projetos acadêmicos a qualquer momento, sem necessidade de aprovação prévia de um moderador — dado o peso avaliativo desses projetos, exigir espera por autorização seria contraproducente para o cronograma acadêmico dos alunos.

---

## 4. Padrões de Desenvolvimento e Git Flow (Commits, Branches e Rulesets)

### Commits Semânticos (Conventional Commits)

Todo commit deve seguir o padrão **Conventional Commits**, no formato `tipo: descrição breve`. Isso deixa o histórico do projeto legível e facilita a geração automática de changelogs no futuro.

| Prefixo | Quando usar |
|---|---|
| `feat:` | Uma nova funcionalidade foi adicionada |
| `fix:` | Correção de um bug |
| `docs:` | Alteração apenas em documentação (README, guias, comentários) |
| `refactor:` | Reorganização do código sem mudar o comportamento externo |
| `chore:` | Tarefas de manutenção (dependências, configuração, build) |
| `test:` | Adição ou ajuste de testes |
| `style:` | Formatação, espaçamento, ponto e vírgula — sem mudança de lógica |

**Exemplos:**
```
feat: adiciona cálculo automático de horário de término da consulta
fix: corrige sobreposição de horários no agendamento
docs: atualiza README com instruções de instalação
```

**Escopo (opcional):** entre o prefixo e os dois-pontos, você pode indicar em parênteses **qual parte do sistema** o commit afeta — `tipo(escopo): descrição`. Isso ajuda bastante quando o projeto já tem módulos bem definidos (ex.: `agenda`, `auth`, `api`, `ui`):

```
feat(agenda): adiciona cálculo automático de horário de término da consulta
fix(auth): corrige expiração prematura do token de login
chore(deps): atualiza versão do Spring Boot
test(agenda): adiciona testes para conflito de horários
refactor(api): extrai validação de entrada para um middleware
docs(readme): documenta variáveis de ambiente necessárias
```

O escopo pode ser praticamente qualquer módulo/área do seu projeto — não existe uma lista fechada. Use o mesmo nome que vocês já usam para o módulo no board/EAP (ex.: `agenda`, `auth`, `api`, `ui`, `deps`, `readme`), assim o histórico do Git e o board falam a mesma língua.

Não é obrigatório usar escopo — em commits pequenos ou projetos sem módulos claros, o padrão simples (`feat:`) continua válido. Mas em projetos maiores, principalmente os organizados por EAP (veja "Nomeando branches e issues com código EAP", logo abaixo), o escopo deixa o histórico bem mais fácil de filtrar.

### Fluxo de Branches (main, develop, feature/fix/refactor)

A organização adota um fluxo simples de duas camadas:

- **`main`** — reflete sempre o estado estável e "publicável" do projeto. Protegida por **GitHub Rulesets** (veja "Protegendo suas Branches", mais abaixo nesta mesma seção): ninguém commita direto nela, só chega código ali via Pull Request aprovado.
- **`develop`** — branch de integração contínua, onde as features são reunidas antes de seguir para a `main`. É a base para novas branches de trabalho.

**Branches de trabalho** nascem a partir da `develop`, com prefixo indicando o tipo de mudança:

```
feature/nome-da-funcionalidade
fix/nome-do-bug
refactor/nome-da-mudanca
```

**Fluxo resumido:**
1. Crie sua branch a partir de `develop` (ex.: `feature/calculo-horario-consulta`).
2. Commite seguindo o padrão semântico.
3. Abra um Pull Request de volta para `develop`, usando o `PULL_REQUEST_TEMPLATE.md`.
4. Após revisão e aprovação, a `develop` é periodicamente promovida para `main` (release).

> Por que proteger a `main` em vez de deixar todo mundo commitar direto nela? Porque a `main` é a "vitrine" do projeto — o que um professor avalia ou um recrutador vê primeiro. Manter a `develop` como buffer de integração evita que código quebrado ou incompleto chegue lá.

### Nomeando Branches e Issues com Código EAP (opcional)

Se o seu projeto usa uma **EAP (Estrutura Analítica de Projeto)** para quebrar o trabalho em módulos e tarefas numeradas, vale a pena carregar esse código no nome da branch e no título da issue — assim dá pra rastrear na hora qual item do planejamento aquele trabalho resolve, sem precisar abrir o board.

**Branches:** mantenha o prefixo de tipo (Seção 4) e insira o código EAP logo depois, separado por hífen:

```
feature/4.3.1-interface-agenda
fix/2.1-bug-login
refactor/3.2-reestrutura-api-usuarios
```

Formato: `tipo/CODIGO_EAP-descricao-curta`, com hífens no lugar de espaços, tudo em minúsculo e sem acentos — igual à convenção de nome de branch já usada no restante da seção.

**Issues:** prefixe o título com o código entre colchetes, seguido da descrição:

```
[4.3.1] Interface da agenda
[2.1] Login não expira o token corretamente
```

Isso deixa o título ordenável e fácil de cruzar visualmente com a EAP do projeto, sem depender de nenhuma label ou campo extra no board.

> 💡 Essa numeração combina bem com o escopo do commit (item acima): se a tarefa `4.3.1` é sobre o módulo `agenda`, o commit natural que fecha essa branch é algo como `feat(agenda): adiciona interface da agenda`, e o Pull Request pode referenciar `Closes #<issue-da-4.3.1>`. Três pontos diferentes (branch, commit, issue) contando a mesma história.

Essa convenção é **opcional**: só faz sentido para projetos que efetivamente montaram uma EAP. Projetos menores, sem WBS formal, seguem normalmente com `feature/nome-da-funcionalidade` como já descrito acima.

### Protegendo suas Branches — Importando o Ruleset Recomendado

A SenacOS opera no plano gratuito do GitHub, então Rulesets a nível de organização não estão disponíveis (esse recurso é exclusivo dos planos pagos Team/Enterprise). Isso significa que **cada repositório precisa da sua própria proteção configurada individualmente** — inclusive o seu.

Para isso não depender de você configurar tudo manualmente campo por campo, o `Template-Projeto-Academico` disponibiliza um arquivo pronto para importação: `ruleset-recipe.json`.

**Como aplicar no seu repositório:**

1. No seu repositório, vá em `Settings → Rules → Rulesets`.
2. Clique em `New ruleset → Import a ruleset`.
3. Selecione o arquivo `ruleset-recipe.json` (baixado do `Template-Projeto-Academico`).
4. Revise as regras importadas e clique em `Create`.

**O que essa configuração garante nas branches `main` e `develop`:**
- Bloqueio de exclusão das branches.
- Bloqueio de force-push (ninguém reescreve o histórico por cima do trabalho do colega).
- Exigência de Pull Request para qualquer mudança chegar lá — nada de push direto, nem para quem administra o repositório.
- Exigência de pelo menos 1 aprovação de revisão antes do merge.

> ⚠️ **Nota técnica:** a lista de exceções de bypass (quem pode ignorar as regras) não é incluída no arquivo exportado/importado, por padrão do próprio GitHub. Se quiser abrir uma exceção pontual (por exemplo, para você mesmo como administrador do repositório em algum caso excepcional), configure isso manualmente depois de importar, na própria tela do Ruleset.

Esse passo é rápido (menos de um minuto) e vale a pena fazer logo depois de criar seu repositório a partir do template — antes do primeiro Pull Request.

---

## 5. Labels — Como e Quando Usar (Nativas, Customizadas e o que Não é Label)

Todo repositório da organização já nasce com um conjunto padrão de labels configuradas a nível organizacional — você **não precisa criar nenhuma label manualmente**. Usar as labels certas na Issue ou Pull Request certo não é burocracia: é um sinal de boa prática de organização que ajuda colegas, professores e você mesmo a entender rapidamente o estado do projeto.

### Nativas do GitHub

Vêm prontas em qualquer repositório, sem configuração:

| Label | Quando usar |
|---|---|
| `bug` | Algo não está funcionando como deveria |
| `documentation` | Mudanças relacionadas apenas a documentação |
| `enhancement` | Sugestão de nova funcionalidade ou melhoria |
| `question` | Dúvida que não é bug nem sugestão |
| `good first issue` | Boa entrada para quem está contribuindo pela primeira vez |
| `help wanted` | O time do projeto sinaliza que precisa de ajuda externa |
| `duplicate` | Esta Issue/PR já existe em outro lugar |
| `invalid` | Isso não parece correto/aplicável |
| `wontfix` | Reconhecido, mas não será trabalhado |

> ⚠️ Não crie `bugfix`, `help-wanted` (com hífen) ou qualquer variação/tradução das labels acima. A label nativa já cobre o caso, e o PR que resolve um `bug` se conecta a ele via `Fixes #123` e o commit `fix:` (Seção 4) — criar uma label extra só duplicaria essa informação.

### Customizadas da SenacOS

Também já vêm prontas em todo repositório novo. Use para indicar **tipo** e **área** do trabalho:

| Label | Quando usar |
|---|---|
| `task` | Sub-issue de trabalho técnico |
| `epic` | Issue-pai/Módulo, agrupando várias tarefas |
| `frontend` | Interface, componentes visuais, UX |
| `backend` | API, regras de negócio, lógica de servidor |
| `banco-de-dados` | Schema, migrations, queries |
| `infra` | CI/CD, deploy, configuração de ambiente |
| `design` | Protótipos, identidade visual, UI Kit |
| `security` | Proteção de dados, autenticação, correção de vulnerabilidades |
| `functional` | Requisito funcional — recurso ou capacidade direta do sistema |
| `non-functional` | Requisito não-funcional — segurança, performance, escalabilidade |
| `mvp` | Funcionalidade essencial para a entrega mínima viável |
| `refinement` | Item ainda precisa de detalhamento antes de entrar no board |
| `blocked` | Não pode avançar por dependência externa ou outra tarefa pendente |

### O que **não** é label

Prioridade, tamanho/esforço e sprint **não** são labels — use os campos nativos do GitHub Projects (`Priority`, `Size`, `Iteration`) no board da sua equipe, detalhados na Seção 6. O mesmo vale para status (Todo/In Progress/Done): isso é coluna do Kanban, não label. Duas fontes rastreando a mesma informação tendem a dessincronizar — alguém move o card e esquece de trocar a label, por exemplo.

**Regra prática:** se a informação muda com frequência ao longo do trabalho (status, prioridade, sprint), ela vive no board. Se é uma característica que praticamente não muda depois de definida (é bug ou é feature, é frontend ou é backend), ela vive na label.

---

## 6. Gestão Ágil e GitHub Projects (Board, Campos Nativos e Automações)

Esta seção não é uma aula de Scrum — é um manual operacional de como usar o **GitHub Projects** (o Kanban da organização) na prática, incluindo como traduzir uma EAP/WBS para o board.

### Criando o Board (Novo Project)

Cada projeto acadêmico deve ter seu próprio Project vinculado ao repositório:

1. No seu repositório, aba `Projects` → `New project`.
2. Escolha o template **`SenacOS · Board Acadêmico`** (template oficial da organização, com Backlog, Board e Roadmap já configurados) — ou, na falta dele, o template embutido `Board`.
3. Vincule o Project ao repositório (`Settings do Project → Manage access` ou direto pela criação a partir do repo) para que Issues e PRs apareçam automaticamente como candidatos a entrar no board.
4. Em `Settings → Default repository`, selecione o repositório do seu projeto acadêmico — isso evita ter que escolher o repo manualmente toda vez que criar um item novo direto pelo board.

### Colunas do Board (Status)

| Coluna | Significado |
|---|---|
| **Backlog** *(opcional)* | Ideias e tarefas ainda não priorizadas para o ciclo atual |
| **Todo** | Já tem critérios de aceitação definidos, pronta para alguém pegar |
| **In Progress** | Alguém está trabalhando ativamente nisso agora |
| **In Review** | Pull Request aberto, aguardando revisão |
| **Done** | Mergeado e fechado |

Status é sempre coluna do board — nunca label (ver Seção 5).

### Campos Nativos: Priority, Size e Iteration (em vez de labels)

Adicione estes campos em `Project → ... → Settings → New field`:

| Campo | Tipo | Opções sugeridas | Substitui |
|---|---|---|---|
| `Priority` | Single select | 🔴 Alta / 🟡 Média / 🟢 Baixa | label `prioridade-*` |
| `Size` | Single select | XS, S, M, L, XL | label `complex` |
| `Iteration` | Iteration | Duração do seu ciclo (ex.: 1 ou 2 semanas) | label `sprint-01`, `sprint-02`... |

Esses três campos resolvem exatamente o que labels de prioridade/tamanho/sprint tentariam capturar, sem duplicar informação em dois lugares.

### Vinculando Issues e Pull Requests (Workflows/Automações)

O board se move sozinho quando você usa as palavras-chave certas:

- Ao abrir um Pull Request, escreva `Closes #<número-da-issue>` (ou `Fixes #<número>`) na descrição.
- Quando esse PR for mergeado, a Issue fecha automaticamente — e, se o Workflow abaixo estiver configurado, o card some da coluna `In Progress`/`In Review` e vai direto para `Done`.

**Automações nativas** (`Project → ... → Workflows`):

| Gatilho | Ação |
|---|---|
| Item adicionado ao Project | Status = `Todo` |
| Pull Request aberto referenciando a Issue | Status = `In Review` |
| Issue/PR fechado | Status = `Done` |

Ativar esses três workflows já cobre o ciclo básico sem precisar mover card manualmente na maior parte do tempo.

### Sub-issues Nativas (Módulo x Tarefa)

O `Template-Projeto-Academico` já vem com dois Issue Templates prontos para isso: `🧩 Módulo/Epic` e `📋 Tarefa`. Para vinculá-los:

1. Abra a Issue de Módulo.
2. Na sidebar, use `Create sub-issue` (ou adicione uma Tarefa já existente como sub-issue pelo mesmo menu).
3. O GitHub passa a mostrar uma barra de progresso automática no Módulo, calculada pelas sub-issues fechadas — sem precisar atualizar checklist manualmente.

### Traduzindo a EAP para o Board

Se o seu projeto usa EAP (ver "Nomeando Branches e Issues com Código EAP" na Seção 4), o fluxo fica assim:

1. Cada **módulo da EAP** (ex.: `4.3 Gestão de Agenda`) vira uma Issue usando o template `🧩 Módulo/Epic`, com o código da EAP no título: `[4.3] Gestão de Agenda`.
2. Cada **tarefa da EAP** (ex.: `4.3.1 Cálculo de horário`) vira uma sub-issue usando o template `📋 Tarefa`, título `[4.3.1] Cálculo de horário`, vinculada ao Módulo `4.3` via `Create sub-issue`.
3. No board, o card do Módulo mostra visualmente quantas das suas tarefas já foram concluídas — sua EAP inteira, em forma de Kanban, sem duplicar planejamento em dois documentos separados.

### Fluxo Resumido (Dia a Dia)

1. Issue nova entra com a label `refinement` até ter critérios de aceitação claros.
2. Uma vez pronta, entra em `Todo`, com `Priority` e `Size` preenchidos.
3. Alguém se atribui → move para `In Progress`.
4. Abre o Pull Request referenciando a Issue (`Closes #123`) → vira `In Review` automaticamente.
5. Aprovado e mergeado → Issue fecha → card vai para `Done` sozinho.

---

## 7. Ecossistema de Repositórios (Mapa da Organização)

| Repositório | Propósito | Status |
|---|---|---|
| [`.github`](https://github.com/SenacOS/.github) | Templates de issue/PR padrão, código de conduta e perfil público da organização | ✅ Ativo |
| [`core`](https://github.com/SenacOS/core) | Regras, Rulesets, templates de gestão ágil e este guia | ✅ Ativo |
| [`Template-Projeto-Academico`](https://github.com/SenacOS/Template-Projeto-Academico) | Repository Template para novos projetos acadêmicos | ✅ Ativo |
| `[CURSO]-[SEMESTRE]-*` | Projetos de turma e projetos integradores dos alunos | ✅ Ativo |
| `comunidade` (GitHub Discussions) | Fórum da comunidade — dúvidas, avisos, bate-papo, sem poluir Issues de projetos sérios | 🚧 Em construção |
| `me-contrata` | Vitrine de portfólios e busca por oportunidades | 🚧 Em construção |
| `biblioteca-livre` | Curadoria de livros, cursos e documentações gratuitas de programação e T.I | 🚧 Em construção |
| `desafios-codigo` | Laboratório de lógica, estruturas de dados, algoritmos e projetos lúdicos | 🚧 Em construção |

> 🔒 **Nota de privacidade:** ao postar no `me-contrata`, evite expor dados sensíveis (CPF, endereço completo, telefone pessoal) — é um repositório público e indexável.

---

## 8. Metodologia & Integridade do Ecossistema

- **Gestão Ágil Integrada:** templates padronizados conectados ao **GitHub Projects** (Kanban) para organizar entregas acadêmicas — ver Seção 6.
- **Governança Automatizada:** branches principais protegidas por **GitHub Rulesets**, garantindo revisão mínima antes de qualquer código chegar à vitrine pública.
- **Hábitos Profissionais:** commits semânticos, Pull Requests descritivos e rastreamento de issues fazem parte da cultura de desenvolvimento da comunidade.

---

*Dúvidas? Abra uma Discussion em `comunidade` ou marque `@SenacOS/professores`.*
