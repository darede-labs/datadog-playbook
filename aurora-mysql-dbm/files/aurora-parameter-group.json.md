### ⚙️ `aurora-parameter-group.json`
Exemplo de parâmetros recomendados para Aurora MySQL.

```json
[
  {"ParameterName": "performance_schema", "ParameterValue": "1"},
  {"ParameterName": "performance_schema_instrument", "ParameterValue": "%=ON"},
  {"ParameterName": "performance_schema_consumer_events_statements_current", "ParameterValue": "ON"},
  {"ParameterName": "performance_schema_consumer_events_statements_history", "ParameterValue": "ON"},
  {"ParameterName": "performance_schema_consumer_events_statements_history_long", "ParameterValue": "ON"},
  {"ParameterName": "max_digest_length", "ParameterValue": "4096"},
  {"ParameterName": "performance_schema_max_digest_length", "ParameterValue": "4096"},
  {"ParameterName": "performance_schema_max_sql_text_length", "ParameterValue": "4096"}
]
```
