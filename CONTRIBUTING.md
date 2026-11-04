# Guia de contribuição

## Mensagens de commit

Formato: `tipo: descrição curta no imperativo`

| Tipo | Quando usar | Exemplo |
|---|---|---|
| `feat` | nova funcionalidade | `feat: adiciona rodapé à página` |
| `fix` | correção de erro | `fix: corrige erro de digitação no título` |
| `docs` | documentação | `docs: atualiza README` |
| `style` | formatação, sem mudar lógica | `style: ajusta espaçamento do menu` |
| `refactor` | reorganização de código | `refactor: separa estilos do HTML` |
| `chore` | tarefas de manutenção | `chore: atualiza .gitignore` |

Regras: escrever em português, com no máximo 72 caracteres, sem ponto final.

## Branches

- `main`: versão estável, só recebe merge de `develop` ou `hotfix/*`.
- `develop`: integração do trabalho da equipe.
- `feature/<nome>`: nova funcionalidade (ex.: `feature/rodape`).
- `fix/<nome>`: correção de bug (ex.: `fix/titulo`).
- `docs/<nome>`: mudanças só de documentação.

## Pull Requests

1. Abrir o PR da sua branch para a `develop`.
2. Título no mesmo padrão dos commits (ex.: `feat: adiciona rodapé`).
3. Descrever em 1 ou 2 linhas o que mudou.
4. Pedir revisão do Revisor de código.
5. Só fazer o merge depois da aprovação.
6. Se houver conflito, quem abriu o PR resolve e atualiza a branch.

## Versionamento

Versionamento semântico: `vMAJOR.MINOR.PATCH` (ex.: `v1.0.0`, `v1.1.0`, `v2.0.0`).
