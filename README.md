# integration-plataform
Impacta Streaming

# Impacta Streaming – Aula Prática Kafka (Data Integration)
Curso: MBA em Data Engineering  
Disciplina: Integrated Data Platforms  
Aluna: Talita Nobrega  

📋 Sobre o Projeto

Este repositório contém o projeto da aula prática de integração de dados com Apache Kafka, utilizando Docker, JupyterLab e Kafka UI para simular um cenário de streaming de dados.

🎯 Objetivo

- Geração de eventos `producer.ipynb`
- Transporte dos eventos por meio de um cluster Kafka
- Consumo dos eventos `consumer.ipynb`
- Persistência dos dados em arquivos CSV para análise posterior

- `producer.ipynb`: Gera mensagens simulando eventos de usuários
- `consumer.ipynb`: Consome as mensagens e grava em CSV

🏗️ Arquitetura da Solução

- Zookeeper: Coordenação do cluster Kafka
- Kafka Brokers: Dois brokers para simular ambiente distribuído
- Kafka UI: Interface web para inspecionar tópicos e mensagens
- JupyterLab: Ambiente para executar os notebooks

📁 Estrutura de Pastas

mba-integration-platform/
├─ docker-compose.yml
├─ notebooks/
│  ├─ producer.ipynb
│  ├─ consumer.ipynb
│  ├─ run_jupyterlab.sh
│  ├─ requirements.txt
│  ├─ data/ Arquivos CSV gerados pelo consumer
│  └─ imagens/

🚀 Como Executar

1. Clone o repositório: bash git clone https://github.com/seu-usuario/impacta_streaming.git cd impacta_streaming
2. Suba o Docker com `docker-compose up -d`
3. Instale as dependências Python: bash pip install -r notebooks/requirements.txt
4. Acesse o JupyterLab em `http://localhost:8888` (verifique o token no log do container ou use o script run_jupyterlab.sh).
5. Execute os notebooks: producer.ipynb: Gera e envia eventos para o Kafka | consumer.ipynb: Consome eventos do Kafka e salva em CSV na pasta data.
6. Acesse o Kafka UI em `http://localhost:8080`: para monitorar tópicos e mensagens.

⚡ Observações de Performance

- Escrita em CSV com buffer e encoding UTF-8
- Processamento em lote para maior eficiência
- Producer com flush periódico

📋 Requisitos

- Docker e Docker Compose
- Python 3.8+
- Navegador web

📄 Licença

Uso acadêmico.
