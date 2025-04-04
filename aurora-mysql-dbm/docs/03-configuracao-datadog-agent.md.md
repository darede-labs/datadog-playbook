# Configuração do Datadog Agent

Agora vamos instalar e configurar o Datadog Agent na máquina EC2.

## 1. Instalação do Datadog Agent

Siga a [documentação oficial do Datadog](https://docs.datadoghq.com/agent/) para instalar o Agent no sistema operacional desejado.

## 2. Configuração do arquivo `conf.yaml`

Edite o arquivo `/etc/datadog-agent/conf.d/mysql.d/conf.yaml`, utilizando o exemplo abaixo ([conf.yaml](../arquivos/conf.yaml)):

```yaml
instances:
  - host: "<ENDPOINT_AURORA>" 
    port: 3306
    username: "datadog"
    password: "<SENHA>"  
    dbm: true
```

Substitua:

- `<ENDPOINT_AURORA>` pelo endpoint do seu Aurora, não pelo endpoint do Cluster.
- `<SENHA>` pela senha configurada para o usuário Datadog no MySQL. Use 'ENC[<SENHA>]' em caso de ter a senha criptografada por um vault.

## 3. Reinicie o Datadog Agent

```sudo systemctl restart datadog-agent´´´




