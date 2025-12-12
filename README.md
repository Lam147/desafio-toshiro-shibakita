# Projeto Toshiro Shibakita - Docker com Microsserviços 🚀

Projeto desenvolvido como desafio do bootcamp da **Digital Innovation One (DIO)**, baseado na live coding do instrutor **Denilson Bonatti**.

## Arquitetura Implementada

Aplicação de microsserviços containerizada com Docker, composta por:

- **MySQL**: Banco de dados para persistência de informações
- **Aplicação PHP**: Responsável por gerar nomes japoneses aleatórios e salvá-los no banco
- **Nginx**: Atuando como reverse proxy e load balancer

## Funcionalidades

- Geração automática de nomes japoneses aleatórios
- Persistência dos dados gerados no MySQL
- Escalabilidade horizontal utilizando múltiplos containers
- Deploy completo em ambiente cloud (AWS) com compartilhamento de volumes via NFS

## Execução Local

```bash
docker-compose up --build
```

Acesso à aplicação: http://localhost:8080
Deploy na AWS

3 instâncias EC2 (Ubuntu 20.04):
1 instância configurada como NFS Server
2 instâncias como Application Nodes rodando os containers Docker

Configuração de NFS para garantir alta disponibilidade e persistência dos dados
Nginx configurado como load balancer distribuindo requisições entre os nodes

Testes de Performance

Ferramenta utilizada: loader.io
Testes de carga simulando aumento gradual de clientes concurrentes
Resultados demonstraram boa escalabilidade da arquitetura com Docker

Conclusão
O projeto foi executado tanto localmente quanto em ambiente cloud, comprovando na prática os benefícios do uso de containers Docker em cenários de microsserviços: isolamento, portabilidade, escalabilidade e facilidade de gerenciamento.

#DIO #Docker #Microsserviços #AWS #DevOps #CloudComputing

