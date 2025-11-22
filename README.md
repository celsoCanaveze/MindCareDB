# MindCareDB

1. Introdução

O projeto MindCareDB consiste na estruturação e disponibilização dos dados utilizados pelo sistema MindCare, incluindo scripts SQL, arquivos JSON para carga e documentos auxiliares para importação em bancos relacionais e NoSQL. Este repositório tem como finalidade organizar, padronizar e facilitar a persistência dos dados utilizados na aplicação.

2. Objetivo

O objetivo central deste módulo é fornecer:

O modelo de banco de dados,

Scripts SQL de criação,

Dados iniciais em formato JSON,

Guia de importação para ferramentas de banco relacional e MongoDB.

3. Fundamentação Técnica

O MindCareDB utiliza uma combinação de tecnologias de armazenamento, permitindo experimentação em bancos SQL e NoSQL:

SQL estruturado (DDL/DML) para bancos relacionais;

Arquivos JSON para preenchimento de coleções/documentos em bancos não-relacionais;

MongoDB como alternativa para persistência orientada a documentos.

4. Estrutura do Repositório
MindCareDB/

│── MindCareDB.sql    

│── usuarios.json      

│── historico_mood.json    

│── tarefas.json             

│── competencias.json        

│── usuario_competencia.json  

│── usuario_tarefa.json        

│── tarefa_competencia.json  

│── importsMongoDB.txt

6. Procedimentos de Execução
5.1. Importação em Banco Relacional

Abra o Oracle SQL Developer ou similar.

Crie uma conexão e selecione o schema desejado.

Execute o arquivo:

MindCareDB.sql


Após created tables, realize inserts conforme necessário.

5.2. Importação em MongoDB

Executar comandos (descritos no importsMongoDB.txt):

mongoimport --db MindCare --collection usuarios --file usuarios.json --jsonArray


Repetir para cada coleção JSON.

6. Considerações Finais

O módulo MindCareDB representa a base de dados oficial da solução MindCare, garantindo coerência, rastreabilidade e uniformidade nas execuções acadêmicas, testes e integrações com os demais módulos.
