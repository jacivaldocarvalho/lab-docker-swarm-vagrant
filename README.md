# Lab Docker Swarm com Vagrant

## **Objetivo**
Este repositório tem como objetivo fornecer uma solução prática para o **provisionamento de um cluster de máquinas virtuais utilizando Vagrant**, configurado para rodar um **Docker Swarm**. Com esse setup, é possível criar um ambiente de orquestração de containers altamente escalável e gerenciável em um ambiente local.

Este projeto é ideal para quem deseja aprender a configurar e gerenciar clusters Docker utilizando **Vagrant** e **Docker Swarm** de maneira automatizada.


## **Estrutura do Projeto**

O repositório contém os seguintes arquivos principais para configurar e iniciar o ambiente:

- **Vagrantfile**: Arquivo de configuração principal do Vagrant, responsável pela criação das máquinas virtuais.
- **docker.sh**: Script de instalação e configuração do Docker nas máquinas virtuais.
- **master.sh**: Script para configurar a máquina principal do cluster Docker Swarm.
- **worker.sh**: Script para configurar as máquinas de trabalho (workers) do Docker Swarm.


## **Como Usar**

### **1. Requisitos**
Antes de começar, você precisará de:
- **Vagrant**: Para provisionamento de máquinas virtuais.
- **VirtualBox**: Como provedor de virtualização.
- **Docker**: Para a configuração do Docker Swarm.

### **2. Clonando o Repositório**

Clone o repositório para sua máquina local:

```bash
git clone https://github.com/jacivaldocarvalho/lab-docker-swarm-vagrant.git
cd lab-docker-swarm-vagrant
```

### **3. Inicializando o Vagrant**

Execute o Vagrant para criar e iniciar as máquinas virtuais:

```bash
vagrant up
```

Isso vai provisionar as VMs e configurar o Docker Swarm automaticamente.

### **4. Verificando o Cluster Docker Swarm**

Após a configuração, acesse a máquina master e verifique o status do cluster Docker Swarm:

```bash
vagrant ssh master
docker node ls
```


## **Evoluções Possíveis para o Projeto**

### 1. **Automação de Deploy com Docker Compose**
Implemente o **Docker Compose** para facilitar a definição e execução de aplicações multi-containers no cluster. Isso permitirá a automação do deploy de containers em todos os nós do Swarm.

### 2. **Adição de Mais Nó Worker**
Adicione mais nós workers ao cluster para testar a escalabilidade do Docker Swarm em um número maior de máquinas. Isso pode ser feito facilmente editando o Vagrantfile e os scripts de provisionamento.

### 3. **Monitoramento e Logs**
Implemente ferramentas como **Prometheus** e **Grafana** para monitorar o estado e desempenho do Docker Swarm. A adição de um serviço de logs centralizados, como o **ELK stack (Elasticsearch, Logstash, Kibana)**, também seria uma excelente evolução.

### 4. **Implementação de CI/CD**
Adicione uma pipeline de **Integração Contínua e Deploy Contínuo (CI/CD)** utilizando **GitHub Actions** ou **Jenkins** para automatizar o processo de build, testes e deploy de containers.

## Contribuições

Se você tiver sugestões de melhorias ou encontrar problemas com o script, sinta-se à vontade para abrir um **issue** ou submeter um **pull request**.

## Contatos e Network

- **LinkedIn**: [LinkedIn](https://www.linkedin.com/in/jacivaldocarvalho/) 👔
- **E-mail**: [E-mail](mailto:jacivaldocarvalho@gmail.com) 📧
- **GitHub**: [GitHub](https://github.com/jacivaldocarvalho) 🐙
- **Medium**: [Medium](https://medium.com/@jacivaldocarvalho) ✍️

Sempre aberto a novas conexões e oportunidades de aprendizado!

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).


## **Referências Bibliográficas**

Para aprender mais sobre os conceitos utilizados neste projeto, consulte as seguintes fontes:

- [Documentação Oficial do Docker](https://docs.docker.com/)
- [Guia do Docker Swarm](https://docs.docker.com/engine/swarm/)
- [Vagrant - Documentação](https://www.vagrantup.com/docs)
- [Como Usar Docker e Docker Swarm](https://www.docker.com/blog/docker-swarm-overview/)
  
