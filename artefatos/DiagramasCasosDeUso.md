# CASOS DE USO

## Diagramas de Caso de Uso

### Lista de Casos de Uso da Pokedex
- [ ] Manter Pokemon
    - [ ] Inserir Pokemon (?)
    - [ ] Pesquisar Pokemon
    - [ ] Listar Pokemon
- [ ] Validar respostas da API (?)
- [ ] Caso de Uso V
- [ ] Caso de Uso VI
- [ ] Caso de Uso VII
- [ ] Caso de Uso VIII
- [ ] Caso de Uso IX
- [ ] Caso de Uso X
- [ ] Caso de Uso XI
- [ ] Caso de Uso XII

### Casos de Uso
![Diagrama de Caso de Uso de Login V1](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documento-requisitos/blob/main/caso-de-uso-login-v1.svg)

### Script de Caso de Uso [PlantUML](https://www.plantuml.com/plantuml/uml/SyfFKj2rKt3CoKnELR1Io4ZDoSa70000)
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
