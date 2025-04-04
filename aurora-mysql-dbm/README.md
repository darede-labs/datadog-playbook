# 🐬 Aurora MySQL + Datadog DBM

Passo a passo para instrumentação do Database Monitoring do Datadog em uma instância Amazon Aurora RDS com MySQL.

---

## 📂 Estrutura do guia

```
📁 aurora-mysql-dbm/
├── README.md
├── docs/
│   ├── 01-introducao.md
│   ├── 02-configuracao-aurora.md
│   ├── 03-configuracao-datadog-agent.md
│   ├── 04-configuracao-datadog-integration.md
│   ├── 05-validacao.md
│   └── imagens/
├── arquivos/
│   ├── conf.yaml
│   └── aurora-parameter-group.json
└── .gitignore
```

---

## ✅ Checklist do processo

- [ ] Criar e configurar Parameter Group no Aurora
- [ ] Ajustar Security Group para liberar porta 3306
- [ ] Criar usuário `datadog` no MySQL
- [ ] Configurar o Agent na EC2
- [ ] Validar dados no painel do Datadog

---

## 📥 Arquivos de configuração

Estão disponíveis em [`files/`](files/) para download e aplicação direta.

---

## 📸 Screenshots e diagramas

Estão incluídos em [`docs/imagens/`](docs/imagens/) para apoio visual.

---

## ✍️ Autor

Criado por Jean Franco. Contribuições são bem-vindas!