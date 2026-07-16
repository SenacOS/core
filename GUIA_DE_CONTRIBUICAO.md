# 📖 Guia de Contribuição e Navegação — SenacOS

Este documento é a "Constituição" da organização: como participar, como ganhar seu broche de membro, como se organizar em times, como nomear e versionar seu projeto acadêmico, e onde encontrar cada frente da comunidade.

---

## 1. Modelo de Membresia: Contribuidor x Membro

No GitHub existem dois níveis de relação com a nossa comunidade — entenda a diferença antes de começar:

| | **Contribuidor** | **Membro da Organização** |
|---|---|---|
| **Como participa** | Abre uma Issue, entra numa Discussion, ou envia um Pull Request em qualquer repositório público | Convite oficial para o quadro `People` |
| **Pré-requisito** | Nenhum — qualquer aluno (ou visitante externo) pode contribuir | Ter uma contribuição real reconhecida pela comunidade |
| **Onde aparece** | Card "Contributors" do repositório específico onde contribuiu | 🏅 Logo do SenacOS no perfil pessoal do GitHub |
| **Acesso interno** | Nenhum — participação pública padrão | Visibilidade/interação em espaços internos da organização |

Sua primeira contribuição não precisa ser um Pull Request de código. Corrigir um erro de digitação na Biblioteca Livre, responder uma dúvida numa Discussion, ou sugerir uma melhoria de documentação também conta. O que importa é contribuir de verdade — não o quão avançado você já é.

> ⚠️ **Atenção ao aceitar o convite de membro:** por padrão, o GitHub deixa sua filiação à organização como **Privada**. Para o broche aparecer no seu perfil, acesse a página da org → `People` → seu perfil → mude a visibilidade para **Public**.

---

## 2. Organização e Times (GitHub Teams)

O SenacOS usa **GitHub Teams** — no formato "flat" (sem hierarquia entre times) — para identificar grupos dentro da comunidade, de forma parecida com "roles" em servidores de comunidade. Isso não concede privilégios administrativos: é só uma forma de facilitar comunicação e notificação.

**Times previstos:**

| Time (sigla) | Curso (nome completo) | Para que serve |
|---|---|---|
| `@SenacOS/professores` | — | Docentes convidados como referência técnica; dúvidas mais avançadas |
| `@SenacOS/ads` | Análise e Desenvolvimento de Sistemas | Assuntos específicos do curso |
| `@SenacOS/cc` | Ciência da Computação | Assuntos específicos do curso |
| `@SenacOS/eng-software` | Engenharia de Software | Assuntos específicos do curso |
| `@SenacOS/sistemas-info` | Sistemas de Informação | Assuntos específicos do curso |

> Novos times por curso podem ser criados conforme a organização crescer — a lista acima não é fechada. Os times usam sigla por convenção, para ficar consistente com o prefixo de nomenclatura dos repositórios acadêmicos (Seção 3) — a coluna "nome completo" acima serve de referência para quem ainda não decorou as siglas.

**Como marcar o time certo:**

Em qualquer Issue, Discussion ou Pull Request, mencione o time com `@SenacOS/nome-do-time` para notificar todos os seus integrantes de uma vez — por exemplo:

- Travou numa dúvida técnica mais avançada? `@SenacOS/professores`
- Quer que alguém do seu curso revise seu Pull Request? `@SenacOS/ads` (ou o time do seu curso)

**Descoberta para quem está fora da organização:**

Embora os times internos usem siglas, os repositórios acadêmicos recebem **Topics/Tags com o nome do curso por extenso** (ex.: `ciencia-da-computacao`, `analise-e-desenvolvimento-de-sistemas`) — assim, recrutadores e visitantes externos que não conhecem as abreviações do SenacOS ainda conseguem filtrar e encontrar projetos pelo nome completo do curso.

> 🚧 **Planejado:** um formulário de onboarding para novos membros, com checkbox de seleção do curso (por extenso), que os direciona automaticamente ao time correspondente na aceitação do convite.

---

## 3. Convenção de Nomenclatura para Projetos Acadêmicos

Cada projeto acadêmico deve viver em **seu próprio repositório individual** dentro da organização — nunca como uma pasta dentro de um repositório compartilhado. Isso evita conflitos de merge entre grupos diferentes e mantém as abas de Issues/Pull Requests/Projects utilizáveis pelos professores para avaliação individual de cada equipe.

**Formato obrigatório:**

```
[CURSO]-[SEMESTRE]-[NomeDoProjeto]
```

- **CURSO:** sigla do curso, a mesma usada nos Times (Seção 2) — `ADS`, `CC`, `ENG-SOFTWARE`, `SISTEMAS-INFO`.
- **SEMESTRE:** número do semestre seguido de `S` — `1S`, `2S`, `3S`, etc.
- **NomeDoProjeto:** nome do projeto em `CamelCase`, sem espaços ou acentos.

**Exemplos:**
- `ADS-3S-ClinicaNutricao`
- `CC-1S-RpgTextual`
- `SISTEMAS-INFO-2S-ControleEstoque`

Esse padrão organiza a aba de repositórios em ordem alfabética por curso automaticamente, sem precisar de nenhuma ação manual de organização.

**Complemento de descoberta — Topics/Tags:**

Além do prefixo no nome, adicione **Topics** ao repositório no GitHub:
- O nome completo do curso (ex.: `ciencia-da-computacao`) — para visitantes externos, conforme decidido na Seção 2.
- O semestre (ex.: `3-semestre`).
- Tecnologias usadas (ex.: `spring-boot`, `angular`).

Isso permite filtrar a lista de repositórios da organização por tag, algo que a ordenação alfabética sozinha não resolve.

> 💡 **Repository Template:** para reduzir o atrito de quem está criando seu primeiro repositório, use o [`Template-Projeto-Academico`](https://github.com/SenacOS/Template-Projeto-Academico) como ponto de partida — ele já vem com `.gitignore`, licença MIT e `README.md` estruturado prontos. Clique em "Use this template", dê o nome já no formato acima, e o projeto nasce pronto.

**Autonomia de criação:** membros têm liberdade total para criar repositórios de projetos acadêmicos a qualquer momento, sem necessidade de aprovação prévia de um moderador — dado o peso avaliativo desses projetos, exigir espera por autorização seria contraproducente para o cronograma acadêmico dos alunos.

---

## 4. Padrões de Desenvolvimento e Git Flow

### Commits Semânticos

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

### Fluxo de Branches

A organização adota um fluxo simples de duas camadas:

- **`main`** — reflete sempre o estado estável e "publicável" do projeto. Protegida por **GitHub Rulesets** (Seção 6): ninguém commita direto nela, só chega código ali via Pull Request aprovado.
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

---

## 5. Ecossistema de Repositórios

| Repositório | Propósito | Status |
|---|---|---|
| [`core`](https://github.com/SenacOS/core) | Regras, Rulesets, templates de gestão ágil e este guia | ✅ Ativo |
| [`Template-Projeto-Academico`](https://github.com/SenacOS/Template-Projeto-Academico) | Repository Template para novos projetos acadêmicos | ✅ Ativo |
| `[CURSO]-[SEMESTRE]-*` | Projetos de turma e projetos integradores dos alunos | ✅ Ativo |
| `comunidade` (GitHub Discussions) | Fórum da comunidade — dúvidas, avisos, bate-papo, sem poluir Issues de projetos sérios | 🚧 Em construção |
| `me-contrata` | Vitrine de portfólios e busca por oportunidades | 🚧 Em construção |
| `biblioteca-livre` | Curadoria de livros, cursos e documentações gratuitas de programação e T.I | 🚧 Em construção |
| `desafios-codigo` | Laboratório de lógica, estruturas de dados, algoritmos e projetos lúdicos | 🚧 Em construção |

> 🔒 **Nota de privacidade:** ao postar no `me-contrata`, evite expor dados sensíveis (CPF, endereço completo, telefone pessoal) — é um repositório público e indexável.

---

## 6. Metodologia & Integridade do Ecossistema

- **Gestão Ágil Integrada:** templates padronizados conectados ao **GitHub Projects** (Kanban) para organizar entregas acadêmicas.
- **Governança Automatizada:** branches principais protegidas por **GitHub Rulesets**, garantindo revisão mínima antes de qualquer código chegar à vitrine pública.
- **Hábitos Profissionais:** commits semânticos, Pull Requests descritivos e rastreamento de issues fazem parte da cultura de desenvolvimento da comunidade.

---

*Dúvidas? Abra uma Discussion em `comunidade` ou marque `@SenacOS/professores`.*