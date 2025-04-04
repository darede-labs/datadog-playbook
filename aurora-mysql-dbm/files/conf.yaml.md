### ⚙️ `conf.yaml`
Exemplo de configuração do Datadog Agent para monitorar MySQL.

```yaml
instances:
  - host: "<ENDPOINT_AURORA>"
    port: 3306
    username: "datadog"
    password: "<SENHA>"
    dbm: true
```