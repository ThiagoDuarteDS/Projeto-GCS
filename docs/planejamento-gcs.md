# Plano de Gerência de Configuração de Software (GCS)

Projeto: Página de Apresentação da Equipe
Ferramenta: Git + GitHub

## 1. Itens de configuração (ICs)

Itens que serão colocados sob controle de versão:

| Item | Local | Descrição |
|---|---|---|
| Código-fonte | `src/` | Páginas HTML, CSS e scripts |
| Documentação | `docs/` | Plano de GCS e demais documentos |
| README | `README.md` | Descrição do projeto |
| Guia de contribuição | `CONTRIBUTING.md` | Regras de commit, branch e PR |
| Configuração do Git | `.gitignore` | Arquivos ignorados pelo controle de versão |

Não são versionados: arquivos temporários, logs e arquivos específicos do editor de cada integrante.

## 2. Convenções de nomeação

**Arquivos e pastas:** minúsculas, sem espaços e sem acentos, separando palavras com hífen (ex.: `planejamento-gcs.md`).

**Branches:** `tipo/descricao-curta`, em minúsculas e com hífen.

- `feature/rodape`
- `fix/titulo`
- `docs/atualiza-readme`

**Commits:** `tipo: descrição curta no imperativo` (ex.: `feat: adiciona rodapé`). Tipos aceitos: `feat`, `fix`, `docs`, `style`, `refactor`, `chore`.

**Tags:** `vMAJOR.MINOR.PATCH` (ex.: `v1.0.0`).

## 3. Política de versionamento

Adotamos **versionamento semântico** (`MAJOR.MINOR.PATCH`):

- **MAJOR:** mudanças grandes ou incompatíveis (ex.: `1.0.0` → `2.0.0`).
- **MINOR:** novas funcionalidades compatíveis (ex.: `1.0.0` → `1.1.0`).
- **PATCH:** correções pequenas (ex.: `1.0.0` → `1.0.1`).

As tags são criadas pelo Gestor de Configuração sobre a branch `main`, depois que o merge for aprovado.

| Versão | Marco |
|---|---|
| v1.0.0 | Primeira versão estável (estrutura inicial e primeiras funcionalidades) |
| v2.0.0 | Versão com todas as contribuições da equipe e conflitos resolvidos |

## 4. Política de branching

Modelo simplificado inspirado no Git Flow:

| Branch | Função | Quem altera |
|---|---|---|
| `main` | Versão estável, pronta para entrega. Protegida. | Somente via merge aprovado |
| `develop` | Integração do trabalho da equipe | Via Pull Request |
| `feature/*` | Uma funcionalidade por branch | Dono da branch |
| `fix/*` | Correção de bugs | Dono da branch |
| `docs/*` | Mudanças de documentação | Dono da branch |

**Regras**

1. Ninguém faz commit direto na `main` ou na `develop`.
2. Cada integrante cria sua branch a partir da `develop`.
3. Todo merge acontece por Pull Request com pelo menos **1 aprovação** do Revisor de código.
4. Conflitos são resolvidos por quem abriu o Pull Request, atualizando a própria branch antes do merge.
5. Branches já mescladas podem ser apagadas.
6. Exceção: a configuração inicial do repositório (estrutura, README, plano e versão `v1.0.0`) foi feita diretamente na `main` pelo Gestor de Configuração, antes da criação das branches de desenvolvimento.

## 5. Papéis

| Papel | Integrante | Responsabilidades |
|---|---|---|
| Gestor de Configuração | Thiago Duarte | Cria o repositório, define regras, protege a `main`, cria as tags, resolve conflitos de seus Pull Requests e organiza o relatório |
| Desenvolvedora principal | Crisnelly Nobre | Mantém o código base e as funcionalidades centrais |
| Revisor de código | Leandro Pires | Revisa e aprova os Pull Requests, fazendo o merge, e também desenvolve correções em branch própria |

Como a equipe tem 3 integrantes, todos também atuam como desenvolvedores em suas próprias branches. Nenhum Pull Request é aprovado por quem o abriu.

## 6. Estratégia de backup e recuperação

**Backup**

- O repositório remoto no GitHub é a cópia central do projeto.
- Cada integrante mantém um clone local (`git clone`), o que gera cópias redundantes.
- Antes de cada versão, as tags marcam pontos de restauração.
- Cópia extra opcional: baixar um `.zip` do repositório (botão *Code → Download ZIP*) a cada versão.

**Recuperação**

| Situação | O que fazer |
|---|---|
| Voltar a uma versão marcada | `git checkout v1.0.0` |
| Desfazer um commit já publicado | `git revert <hash-do-commit>` |
| Recuperar um arquivo apagado | `git checkout <hash> -- caminho/arquivo` |
| Branch apagada por engano | Localizar o commit com `git reflog` e recriar a branch |
| Repositório local corrompido | Clonar novamente do GitHub |
| Conta ou repositório indisponível | Restaurar a partir de um clone local de outro integrante |

## 7. Controle de mudanças

Toda mudança segue o fluxo: **branch → commits → Pull Request → revisão → merge → tag (quando for uma versão)**. Assim fica registrado quem mudou, o quê, quando e por quê.
