# [MongoDB: Modelagem de dados](https://cursos.alura.com.br/course/mongodb-modelagem-dados)
## Aula 1
* Habilitando extensão Azure Databases do vs code
* Vale a pena modelarmos o nosso banco de dados de acordo com a operação que fazemos com mais frequência
* Aprender a migrar os dados é essencial para a modelagem.
* É quase impossível acertar uma modelagem logo de primeira.

## Aula 2
* Mover os dados para uma nova estrutura.
* Utilizar o Aggregation Framework.
* Utilizar etapas da agregação como o `unwind`, `project` e `out`.

## Aula 3
* Qual o papel dos índices para melhorar as buscas.
* Que índices aumentam o tempo de inserção e isso deve ser levado em consideração.
* Índices únicos evitam que dados duplicados sejam inseridos no banco.

## Aula 4
* Utilizar o `forEach` para iterar sobre os resultados de uma busca.
* Utilizar o update em vários documentos de uma coleção com `{ multi:true }`
* Que performance é uma questão de escolher o que é feito com mais frequência e otimizar de acordo.

## Aula 5
* Ordenar e manipular os resultados de uma consulta com `sort` e `limit`.
* Remover o último elemento de um campo array utilizando o `$pop`.
* Inserir um elemento em um campo array utilizando o `$push`.
* Utilizar o `findOneAndUpdate` para retornar um documento modificado.