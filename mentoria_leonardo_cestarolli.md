> Tópicos e insights da mentoria com Leonardo Cestarolli, Gerente de Arquitetura de Dados, Banco Carrefour.

## Contexto geral

- Uma gama vasta de tecnologias
  
- Ferramentas necessitam de manutenção
  
- Arquitetura de dados com muitos formatos, origens e destinos
  
- Uma combinação é sempre favorável
  
- Soluções bem pensadas
  

### SQL

- Esquema de dados rígido
  
- Permite um modelo muito bem definido
  
- Apropriado para situações onde é preciso integridade de relacionamentos e constraints garantida
  
- Feito para os OLTP
  
- Propriedades ACID (Atomicidade, Consistência, Isolamento e Durabilidade)
  

### NoSQL

- Mais flexível nos esquemas
  
- Maior gama de possibilidades de relacionamentos
  
- Maior escalabilidade horizontal
  
- Capacidade para maior volume e tipos de dados
  
- Reduz complexidade da consulta, evitando JOINs complexos
  
- É possível armazenar informação de acordo com a própria consulta
  
- Persistência por timestamps
  

> As tecnologias são complementares e podem/devem ser utilizadas juntas

## Como encontrar algo armazenado quando não se sabe a estrutura? Como isso pode peformar?

- As chaves de consulta são importantes
  
- Pensar a forma como vai se consultar é importante
  
- Redis para cache de APIs
  
- Aplicação deve saber como lidar com a falta de previsibilidade do esquema
  
- Que tipos de informações podem ser desprezadas ou não
  
- A modelagem da informação ainda é essencial
  
- Criar índices em JSON
  
- Preparar os dados de maneira mais rica, com uma solução como Spark
  

## Como começar

- Conhecer a fundo o contexto do SGBD
  
- Entender para qual propósito eles foram criados
  
- Não se apegar a um nome ou tipo, mas pensar no objetivo da aplicação e modelo de negócio
  
- Conhecer a API
  

> Comenta-se sobre ter uma visão técnica bem pragmática sobre a escolha de uma ferramenta

##

## Dicas de ferramentas

- Ambiente híbrido
  
- Oracle para BI on-premises
  
- Na nuvem (big data) - HDFS - Hadoop
  
- Repositório de metadados HBASE para cadastro das informações sendo armazenadas
  
- Em operações transacionais - MongoDB
  
- As ferramentas de ingestão são importantes (Spark)
  
- Ambientes multicloud são comuns
  

#### Data Bricks e Data Lakes

- O lake é a camada inicial de armazenamento de dado bruto, mas deve ser pensada sua arquitetura
  
- Já é possível conseguir as propriedades ACID dentro de um data lake
  
- Conceito de Lake House
  
- Garantir a arquitetura de um conjunto de dados no data lake
  
- Sistemas de arquivos HDFS
  
- Storages: GC storage, S3 - soluções de baixo custo e grande capacidade
  
- 5 camadas a serem garantidas: Ingestão, Armazenamento, Disponibilidade, Segurança e Governança
  

### Maiores desafios do ETL

- O maior desafio é a manipulação dos dados
  
- Tão importante quanto o cron, ou schedule de processos de ETL, é o monitoramento constante
  
- No Carrefour existem mais de 1000 processos, sendo administrados por uma ferramenta especializada.
  

## Complexidade

- As ferramentas abstraem bastante da complexidade do ETL, porém é importante pensar na arquitetura do banco de dados.
  
- Existem plugins, ferramentas de integração que facilitam os processos.
  

## Como é gerada a demanda dos dados no Banco Carrefour

- Times multidisciplinares contribuem para um ambiente híbrido técnico e estratégico
  
- Engenheiros de dados dão suporte ao negócio, para tirar insights de um contexto específico
  

### Pontos importantes para ser um engenheiro de dados no banco Carrefour

- Curiosidade
  
- Conhecimentos em estatística e conceitos
  
- Visão crítica
  
- Técnicas de gestão de dados e transformação de dados
  
- GCP, Spark
