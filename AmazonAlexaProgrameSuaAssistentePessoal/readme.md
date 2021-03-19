# Amazon Alexa Programe a sua assistente pessoal

## Aula 1
* Uma skill é nada mais do que uma aplicação para interagir com a Alexa
* Uma skill pode ser hospedado pela Alexa na AWS e já vem com alguns recursos integrados no AWS Lambda e S3
* No entanto, uma skill não precisa usar a infraestrutura da AWS e pode usar um outro provedor
* A skill possui um código associado, que pode ser Python ou Node.js
* No Python, a classe LanchRequestHandler é responsável por iniciar a interação
* Para tratar a entrada humana, existem intenções (intents), também representadas através de classes

## Aula 2

* Já existem algumas intents por padrão
* A intent define as perguntas que a disparam (utterance)
* Na definição da intent, devemos definir o slot
    * Um slot é uma variável que define alguns valores que precisam extrair da frase
    * Um slot possui um nome e tem um ou mais valores associados
    * Os valores podem ter sinônimos
    * Um slot pode ser obrigatório
    * Existem vários tipos de slots já pré-definidos
* Uma intent possui uma classe `IntentHandler` associada
    * No Handler, pegamos o valor do slot e buscamos informações

## Aula 3

* Ajustamos o handler da skill para realmente buscar as informações dinamicamente na web
    * Para tal, usamos a biblioteca Python `yfinance` e instalamos ela no AWS Lambda

## Aula 4

* Que existem intents e handlers auxiliares, como `HelpIntentHandler`, `CancelOrStopIntentHandler` ou `SessionEndedRequestHandler`
* Como usar o aplicativo mobile da Alexa para testar a interação
* Que, pelo aplicativo, é possível testar as skills de desenvolvimento
* Que é possível passar a intent e o slot na mesma frase

## Aula 5

* Que o Flash Briefing é uma intent já pré-definida para a leitura de notícias no formato JSON ou RSS
* Que, ao selecionar o modelo Flash Briefing é preciso definir seus próprios recursos (endpoint, storage, etc)
* Que, para o nosso Flash Briefing, usamos um bucket AWS S3

A skill é ainda estática e lê apenas as informações do JSON. Na próxima aula, vamos atualizar dinamicamente as informações.