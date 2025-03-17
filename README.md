# Santander dev week - Decola Tech 2025

Java RESTful API criada para a Santander Dev Week.

## Instalação
Como pré-requisito, você precisa ter: 
- Java versão 17
- Spring Boot versão 3.1.2 

## Outras tecnologias utilizadas
Spring Data, Swagger e Railway. 

## Diagrama de classes (Domínio da API)

```mermaid
classDiagram
class User {
-String name
-Account account
-Feature[] features
-Card card
-News[] news
}

class Account {
-String number
-String agency
-Number balance
-Number limit
}

class Feature {
-String icon
-String description
}

class Card {
-String number
-Number limit
}

class News {
-String icon
-String description
}

User "1" *-- "1" Account
User "1" *-- "N" Feature
User "1" *-- "1" Card
User "1" *-- "N" News
```