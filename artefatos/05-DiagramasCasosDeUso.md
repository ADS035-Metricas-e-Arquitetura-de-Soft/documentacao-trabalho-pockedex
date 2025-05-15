# DIAGRAMAS DE CASOS DE USO

### Lista de Casos de Uso da Pokedex
- [ ] Pesquisar Pokémon
- [ ] Visualizar Pokémon
- [ ] Validar Resposta API
- [ ] Consultar API
- [ ] Mostrar Resposta API

### Casos de Uso Geral

![Diagrama de Caso de Uso Geral](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documentacao-trabalho-pockedex/blob/main/artefatos/img/caso-de-uso.svg)

### Script de Caso de Uso Geral
    @startuml
    left to right direction

    actor Sistema as s
    actor Usuário as u

    package Sistema {
      usecase "Pesquisar Pokémon" as UC0
      usecase "Visualizar Pokémon" as UC1
    }

    package API {
      usecase "Valida Resposta API" as UC2
      usecase "Consulta API" as UC3
      usecase "Mostra Resposta API" as UC4
    }

    u --> s
    s --> UC2
    s --> UC3
    s --> UC4
    u --> UC0
    u --> UC1

    @enduml
    

### Casos de Uso Inserir Pokémon
![Diagrama de Caso de Uso]()

### Script de Caso de Uso Inserir Pokémon [PlantUML](https://www.plantuml.com/plantuml/uml/SyfFKj2rKt3CoKnELR1Io4ZDoSa70000)
    ```@startuml
            left to right direction

    actor Sistema as s
    actor Usuário as u

    package Sistema {
      usecase "Pesquisar Pokémon" as UC0
      usecase "Visualizar Pokémon" as UC1
    }

    package API {
      usecase "Valida Resposta API" as UC2
      usecase "Consulta API" as UC3
      usecase "Mostra Resposta API" as UC4
    }

    u --> s
    s --> UC2
    s --> UC3
    s --> UC4
    u --> UC0
    u --> UC1

    @enduml

### Casos de Uso Pesquisar Pokémon
![Diagrama de Caso de Uso Pesquisar Pokémon](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documento-requisitos/blob/main/caso-de-uso-login-v1.svg)

### Script de Caso de Uso Pesquisar Pokémon [PlantUML](https://www.plantuml.com/plantuml/uml/SyfFKj2rKt3CoKnELR1Io4ZDoSa70000)
    @startuml
    left to right direction
    actor "Usuário" as User
    
    rectangle "Sistema de Login" {
      usecase "Autenticar Usuário" as Authenticate
      usecase "Recuperar Senha" as RecoverPassword
      usecase "Bloquear Conta" as BlockAccount
      usecase "Logout" as Logout
      usecase "Exibir Mensagens de Erro" as DisplayError
    }
    
    User -- Authenticate
    User -- RecoverPassword
    User -- Logout
    
    Authenticate --|> DisplayError : <<include>>
    RecoverPassword --|> DisplayError : <<include>>
    
    Authenticate ..> BlockAccount : <<extend>>
    
    @enduml

### Casos de Uso Listar Pokémon
![Diagrama de Caso de Uso Listar Pokémon](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documento-requisitos/blob/main/caso-de-uso-login-v1.svg)

### Script de Caso de Uso Listar Pokémon [PlantUML](https://www.plantuml.com/plantuml/uml/SyfFKj2rKt3CoKnELR1Io4ZDoSa70000)
    @startuml
    left to right direction
    actor "Usuário" as User
    
    rectangle "Sistema de Login" {
      usecase "Autenticar Usuário" as Authenticate
      usecase "Recuperar Senha" as RecoverPassword
      usecase "Bloquear Conta" as BlockAccount
      usecase "Logout" as Logout
      usecase "Exibir Mensagens de Erro" as DisplayError
    }
    
    User -- Authenticate
    User -- RecoverPassword
    User -- Logout
    
    Authenticate --|> DisplayError : <<include>>
    RecoverPassword --|> DisplayError : <<include>>
    
    Authenticate ..> BlockAccount : <<extend>>
    
    @enduml

### Casos de Uso Visualizar Pokémon
![Diagrama de Caso de Uso Visualizar Pokémon](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documento-requisitos/blob/main/caso-de-uso-login-v1.svg)

### Script de Caso de Uso Visualizar Pokémon [PlantUML](https://www.plantuml.com/plantuml/uml/SyfFKj2rKt3CoKnELR1Io4ZDoSa70000)
    @startuml
    left to right direction
    actor "Usuário" as User
    
    rectangle "Sistema de Login" {
      usecase "Autenticar Usuário" as Authenticate
      usecase "Recuperar Senha" as RecoverPassword
      usecase "Bloquear Conta" as BlockAccount
      usecase "Logout" as Logout
      usecase "Exibir Mensagens de Erro" as DisplayError
    }
    
    User -- Authenticate
    User -- RecoverPassword
    User -- Logout
    
    Authenticate --|> DisplayError : <<include>>
    RecoverPassword --|> DisplayError : <<include>>
    
    Authenticate ..> BlockAccount : <<extend>>
    
    @enduml
