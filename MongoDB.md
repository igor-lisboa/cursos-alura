# Curso Mongo

## Aula 1

* Acessando o cliente MongoDB:
> mongo

* Criando a base de dados use alunos

* Criando a coleção alunos:
> db.createCollection("alunos")

* Para inserir o aluno descrito utilizamos o comando insert():

```javascript
db.alunos.insert({
     "nome": "Felipe",
     "data_nascimento": new Date(1994, 02, 26),
     "notas": [10, 9, 4.5],
     "curso": {
         "nome": "Sistemas de informação"
     },
     "habilidades": [
         {
             "nome": "Inglês",
             "nível": "Avançado"
         }
     ] 
 })
```

***

* Uma situação onde o MongoDB é bastante usado é quando precisamos realizar buscas por proximidade, como, por exemplo, localizar a pizzaria mais próxima de você.

* Situações onde o uso do MongoDB não é indicado são cenários onde precisamos fazer muitas operações de agregação em uma única query, isso tem muito custo para o MongoDB.

***

* para listá-los, basta utilizar o comando find(), sem nenhum argumento:

> db.alunos.find()

* Para remover um aluno usamos o seguinte comando:

> db.alunos.remove({"_id": ObjectId("578b87a7239a421f908ed46b")})
* Perceba que o id pode variar. Este é apenas um exemplo com um id qualquer. Os que aparecem para você serão diferentes.

## Aula 2

* Para restringir as buscas no Mongo precisamos passar um exemplo, no caso {"nome": "Felipe"}, assim o Mongo busca todos que seguem o exemplo

```javascript
db.alunos.find({"nome":"Felipe"})
```

* Para buscar usando a clausula and, basta adicionar outro campo no json passado como exemplo

```javascript
db.alunos.find({"nome": "Felipe", "data_nascimento": new Date(1994, 02, 26)})
```

* No MongoDB conseguimos navegar em um documento através do .

```javascript
db.alunos.find({"habilidades.nome": "inglês"})
```

* Busque todos os alunos dos cursos de Sistemas de informação ou de Ciências da computação
    * Esse exercício pode ser resolvido através do uso dos operadores $or ou $in

```javascript
db.alunos.find({$or:
    [
        {"curso.nome": "Sistemas de informação"},
        {"curso.nome": "Ciências da computação"}

    ]
 }).pretty()
```
ou
```javascript
db.alunos.find({"curso.nome": {$in:
    [
        "Sistemas de informação",
        "Ciências da computação"
    ]
 }}).pretty()
```