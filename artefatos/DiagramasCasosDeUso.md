# DIAGRAMAS DE CASOS DE USO

### Lista de Casos de Uso da Pokedex
- [ ] Manter Pokemon
    - [ ] Inserir Pokémon (?)
    - [ ] Pesquisar Pokémon
    - [ ] Listar Pokémon
    - [ ] Visualizar Pokémon
- [ ] Manter API
    - [ ] Consultar API
    - [ ] Validar respostas da API (?)
    - [ ] Mostrar respostas da API (?)

### Casos de Uso Geral
![Diagrama de Caso de Uso Geral](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documentacao-trabalho-pockedex/tree/main/artefatos/img#:~:text=..-,01%2Dcaso%2Dde%2Duso%2Dgeral%2Dpokedex.svg,-Inserindo%20estrutura%20para)

### Script de Caso de Uso Geral [PlantUML]()
    @startuml
    left to right direction
    actor "Usuário" as User
    
    rectangle "Sistema Pokédex" {
      usecase "Manter Pokémon" as ManterPokemon
      usecase "Manter API" as ManterAPI
    
      usecase "Inserir Pokémon" as InserirPokemon
      usecase "Pesquisar Pokémon" as PesquisarPokemon
      usecase "Listar Pokémon" as ListarPokemon
      usecase "Visualizar Pokémon" as VisualizarPokemon
    
      usecase "Consultar API" as ConsultarAPI
      usecase "Validar respostas da API" as ValidarAPI
      usecase "Mostrar respostas da API" as MostrarAPI
    }
    
    User -- ManterPokemon
    User -- ManterAPI
    
    ManterPokemon .> InserirPokemon : include
    ManterPokemon .> PesquisarPokemon : include
    ManterPokemon .> ListarPokemon : include
    ManterPokemon .> VisualizarPokemon : include
    
    ManterAPI .> ConsultarAPI : include
    ManterAPI .> ValidarAPI : include
    ManterAPI .> MostrarAPI : include
    
    @enduml

    

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
