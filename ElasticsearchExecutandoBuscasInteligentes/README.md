# [Elasticsearch: Executando buscas inteligentes](https://cursos.alura.com.br/course/elasticsearch-introducao)
## Instalação
* CURL
    * executar o seguinte comando no powershell
```sh
choco install curl --version 7.73.0  
```
* JVM
    * ter JVM instalado na máquina
* [ElasticSearch 7.4.2](https://www.elastic.co/pt/downloads/past-releases/elasticsearch-7-4-2)
* [Kibana 7.4.2](https://www.elastic.co/pt/downloads/past-releases/kibana-7-4-2)

## Inicialização
* executar `kibana-7.4.2-windows-x86_64\bin\kibana.bat`
    * testar fazendo um GET em `http://localhost:5601/`
* executar `elasticsearch-7.4.2\bin\elasticsearch.bat`
    * testar fazendo um GET em `http://localhost:9200/`
***
## Aula 1
* O que é e para que serve o ElasticSearch.
* Como fazer uma instalação básica do ElasticSeach a ser usada em uma única máquina.
* Como instalar o Kibana e o cURL.
* Como utilizar um cliente REST para criar e localizar documentos por identificador, listar todos os documentos ou aplicar um valor simples para consulta.