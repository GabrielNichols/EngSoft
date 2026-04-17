# EngSoft — Flask App com CI/CD na Vercel

Aplicação Flask simples desenvolvida para os exercícios de CI/CD da disciplina de Engenharia de Software — Mackenzie.

Fork de [ProfJuliani/EngSoft](https://github.com/ProfJuliani/EngSoft).

## Estrutura

```
.
├── api/
│   └── index.py          # Aplicação Flask (entry point da Vercel)
├── .github/
│   ├── dependabot.yml    # Atualização automática de dependências
│   └── workflows/
│       └── main_mackenzie.yml  # Pipeline CI/CD (build + deploy Vercel)
├── requirements.txt      # Dependências Python
├── vercel.json           # Configuração de roteamento da Vercel
└── README.md
```

## Como rodar localmente

```bash
pip install -r requirements.txt
flask --app api/index run
```

Acesse: http://localhost:5000

## Deploy

O deploy é feito automaticamente na **Vercel** a cada push na branch `main` via GitHub Actions.

Secrets necessários no repositório GitHub:
- `VERCEL_TOKEN` — token de autenticação da Vercel
- `VERCEL_ORG_ID` — ID da organização na Vercel
- `VERCEL_PROJECT_ID` — ID do projeto na Vercel
