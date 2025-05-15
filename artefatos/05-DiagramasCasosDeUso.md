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
    
