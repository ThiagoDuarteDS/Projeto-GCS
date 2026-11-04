# Projeto GCS – Página de Apresentação da Equipe

Projeto simples desenvolvido para simular um ambiente de desenvolvimento com múltiplos desenvolvedores, aplicando conceitos de **Gerência de Configuração de Software (GCS)** com Git e GitHub.

## Objetivo

Praticar:

- controle de versão de artefatos de software;
- criação e merge de branches;
- resolução de conflitos;
- convenções de commit e versionamento.

## Equipe e papéis

| Integrante | Papel |
|---|---|
| Thiago Duarte | Gestor de Configuração |
| Crisnelly Nobre | Desenvolvedora principal |
| Leandro Pires | Revisor de código |

## Estrutura do repositório

```
.
├── README.md            # descrição do projeto
├── CONTRIBUTING.md      # regras de commit, branch e Pull Request
├── .gitignore
├── src/
│   └── index.html       # página do projeto
└── docs/
    └── planejamento-gcs.md   # plano de gerência de configuração
```

## Como rodar

Abra o arquivo `src/index.html` em qualquer navegador.

## Fluxo de trabalho resumido

1. Nunca commitar direto na `main`.
2. Criar uma branch a partir da `develop` (ex.: `feature/rodape`).
3. Fazer commits com mensagens padronizadas (veja `CONTRIBUTING.md`).
4. Abrir um Pull Request e aguardar aprovação do revisor.
5. Após o merge, o Gestor de Configuração cria as tags de versão.

Mais detalhes em [`docs/planejamento-gcs.md`](docs/planejamento-gcs.md).

## Versões

| Versão | Descrição |
|---|---|
| v1.0.0 | Primeira versão estável da página |
| v2.0.0 | Versão com as alterações da equipe e conflitos resolvidos |
