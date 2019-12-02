# Playbook para implantação de um ambiente de monitoramento usando o Prometheus + Grafana + Alertmanager:

## HOSTS
Para executar essa playbook será necessário como primeiro passo ajustar o arquivo 'hosts' dentro do diretório "*inventory*" para informar qual será o servidor que a role executará as tarefas.

A role **ansible-docker** realizar a instalação do docker e docker-compose e em seguida executa o arquivo docker-compose.yml e provisiona os seguintes containeres:

  - prometheus
  - alertmanager
  - grafana
  - blackbox-exporter
  - docker-exporter
  - node-exporter
  - cAdvisor
  - fregate (free mobile sms api)
  - ovirt-prometheus-bridge

Na pasta **configs** estão todos os arquivos de configuração das aplicações listadas acima, edite os arquivos de acordo com o seu ambiente.


A role **ipa-auth** é opcional caso utilize o FreeIPA como gerenciado de identidade e seu ambiente, você pode está utilizando essa role para cadastrar o servidor no FreeIPA.

