# Introdução

Este guia visa orientar a configuração completa do Database Monitoring (DBM) do Datadog para monitorar uma instância Amazon Aurora RDS com MySQL. Este procedimento esta baseado nesta documentação oficial da Datadog: [Setting Up Database Monitoring for Aurora managed MySQL](https://docs.datadoghq.com/database_monitoring/setup_mysql/aurora/?tab=mysql57)

## O que você vai alcançar com este guia?

- Coletar métricas detalhadas sobre consultas e desempenho do banco MySQL.
- Integrar seu Aurora com o Datadog, utilizando melhores práticas recomendadas.

## Requisitos

Antes de começar, certifique-se de que possui:

- Uma instância do Amazon Aurora MySQL ativa.
- Acesso ao console da AWS.
- Uma instância EC2 onde será instalado o Datadog Agent.
- Integração do Datadog ativa com uma conta AWS, incluindo a integração do módulo RDS.
