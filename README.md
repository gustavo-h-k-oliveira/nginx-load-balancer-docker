# Nginx Load Balancer com Docker

## Descrição:

Este projeto demonstra o uso do Nginx como balanceador de carga (load balancer) entre múltiplas instâncias de uma mesma aplicação web, cada uma executada em contêineres Docker independentes. O objetivo é simular o comportamento de um ambiente distribuído, onde o tráfego é dividido de forma cíclica entre os servidores.

## Estrutura do projeto:

```
* app/
  Contém o Dockerfile e o arquivo index.html usados para construir as instâncias da aplicação.
* nginx/
  Contém a configuração do Nginx responsável pelo balanceamento de carga.
* docker-compose.yml
  Define os serviços, redes e dependências entre os contêineres da aplicação e o Nginx.
```

## Execução:

1. Construa e inicie os contêineres:
```
   docker-compose up --build
```
2. Acesse no navegador:
```
   [http://localhost:8080](http://localhost:8080)
```
3. A página deve alternar entre as respostas das instâncias (APP1, APP2, APP3), indicando o balanceamento de carga.

Notas:

* O projeto foi desenvolvido para ser simples e didático, sem dependências externas.
* Pode ser expandido para incluir cache reverso, métricas ou estratégias de failover.
* Ideal para estudos sobre redes, infraestrutura e escalabilidade em ambientes Docker.
