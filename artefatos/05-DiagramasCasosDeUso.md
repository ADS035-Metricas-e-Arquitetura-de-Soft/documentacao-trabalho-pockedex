# DIAGRAMAS DE CASOS DE USO

### Lista de Casos de Uso da Pokedex
- [ ] Manter Pokemon
    - [x] Inserir Pokémon (?)
    - [ ] Pesquisar Pokémon
    - [ ] Listar Pokémon
    - [ ] Visualizar Pokémon
- [ ] Manter API
    - [ ] Consultar API
    - [ ] Validar respostas da API (?)
    - [ ] Mostrar respostas da API (?)

### Casos de Uso Geral

![Diagrama de Caso de Uso Geral](https://plantuml.com/download)

### Script de Caso de Uso Geral [PlantUML]()
    <|-- s

    

### Casos de Uso Inserir Pokémon
![Diagrama de Caso de Uso Inserir Pokémon](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documento-requisitos/blob/main/caso-de-uso-login-v1.svg)

### Script de Caso de Uso Inserir Pokémon [PlantUML](https://www.plantuml.com/plantuml/uml/SyfFKj2rKt3CoKnELR1Io4ZDoSa70000)
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
