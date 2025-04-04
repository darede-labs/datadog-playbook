# Configuração do Amazon Aurora RDS

Siga estes passos para ajustar corretamente os parâmetros do Amazon Aurora e liberar o acesso necessário.

## 1. Configuração do Parameter Group

No AWS RDS Console:

- Acesse **Parameter Groups**.
- Crie ou edite um Parameter Group existente para sua instância Aurora com MySQL.
- Ajuste os parâmetros conforme o arquivo de exemplo [`aurora-parameter-group.json`](../arquivos/aurora-parameter-group.json)

Parâmetros para o Parameter Group:

| Parâmetro                                                    | Valor sugerido |
| ------------------------------------------------------------ | -------------- |
| `performance_schema`                                         | `1` ou `ON`    |
| `performance_schema_instrument`                              | `% = ON`       |
| `performance_schema_consumer_events_statements_current`      | `ON`           |
| `performance_schema_consumer_events_statements_history`      | `ON`           |
| `performance_schema_consumer_events_statements_history_long` | `ON`           |
| `max_digest_length`                                          | `4096`         |
| `performance_schema_max_digest_length`                       | `4096`         |
| `performance_schema_max_sql_text_length`                     | `4096`         |

> ⚠️ Após aplicar essas alterações, será necessário reiniciar o cluster Aurora.

## 2. Configuração do Security Group

Para garantir o acesso do Datadog Agent ao seu banco Aurora:

- Vá até o painel EC2 → **Security Groups**.
- Adicione uma regra permitindo entrada na porta `3306` (MySQL) a partir do IP da sua máquina EC2 ou do Datadog Agent.

Pronto, agora sua instância Aurora está configurada corretamente!
