# 052 - Starter in Monitoring and Observability

Este laboratório será utilizado para o curso 052 - Starter in Monitoring and Observability.

## Como executar o laboratório

Para subir o ambiente completo do laboratório, execute o seguinte comando:

```bash
vagrant up
```

Este comando irá provisionar duas máquinas virtuais com todas as ferramentas necessárias para o curso.

## O que está habilitado no laboratório

### Servidor Zabbix (server-zbx - 172.16.1.110)
- **Zabbix Server 6.0**: Sistema principal de monitoramento
- **Zabbix Frontend**: Interface web para gerenciamento
- **MariaDB**: Banco de dados para armazenamento dos dados do Zabbix
- **Apache2**: Servidor web para o frontend
- **Zabbix Agent**: Agente local para monitoramento do servidor

**Credenciais padrão:**
- Usuário do banco: `zabbix` / Senha: `4linux`
- Usuário de monitoramento: `zbx_monitor` / Senha: `4linux`

### Servidor de Aplicação (app - 172.16.1.111)
- **Docker**: Plataforma de containers
- **Zabbix Agent2**: Agente avançado com plugins para monitoramento
- **Coffee Shop App**: Aplicação de exemplo executando em container (porta 8080)

### Recursos configurados
- Comunicação entre os servidores via /etc/hosts
- Swap desabilitado (requisito para algumas aplicações)
- Locale configurado para pt_BR.UTF-8
- Templates personalizados do Zabbix para monitoramento MySQL

### URLs de acesso
- **Zabbix Frontend**: http://172.16.1.110/zabbix
- **Coffee Shop App**: http://172.16.1.111:8080

O ambiente está totalmente automatizado com Ansible e pronto para uso após a execução do `vagrant up`.
