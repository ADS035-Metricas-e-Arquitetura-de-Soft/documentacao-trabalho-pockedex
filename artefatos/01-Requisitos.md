# REQUISITOS

## Lista de Artefatos (Índice)

- [ ] **01-Requisitos**
- [ ] [02-Definição de Componentes](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documentacao-trabalho-pockedex/blob/main/artefatos/02-DefinicaoDeComponentes.md)
- [ ] [03-Diagrama Arquitetural](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documentacao-trabalho-pockedex/blob/main/artefatos/03-DiagramaArquitetural.md)
- [ ] [04-Arquétipos](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documentacao-trabalho-pockedex/blob/main/artefatos/04-Arquetipos.md)
- [ ] [05-Diagramas de Caso de Uso (sem a documentação)](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documentacao-trabalho-pockedex/tree/main/artefatos/05-DiagramasCasosDeUso.md)
- [ ] [06-Diagramas de Componentes](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documentacao-trabalho-pockedex/blob/main/artefatos/06-DiagramasDeComponentes.md)
- [ ] [07-Diagramas de Sequência](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documentacao-trabalho-pockedex/blob/main/artefatos/07-DiagramasDeSequencia.md)
- [ ] [08-Construção de API (Código e Documentação)](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documentacao-trabalho-pockedex/tree/main/artefatos/08-API.md)
- [ ] [09-BPMN](https://github.com/ADS035-Metricas-e-Arquitetura-de-Soft/documentacao-trabalho-pockedex/blob/main/artefatos/09-BPMN.md)

---

## Lista de Artefatos
### Requisitos Funcionais

- [x] ![Buffer Badge](https://img.shields.io/badge/SISTEMA-368900?logo=buffer&logoColor=fff&style=flat) RF 1 - Pesquisar Pokémon
- [x] ![Buffer Badge](https://img.shields.io/badge/SISTEMA-368900?logo=buffer&logoColor=fff&style=flat) RF 2 - Visualizar Pokémon
- [ ] ![Buffer Badge](https://img.shields.io/badge/API-ff0d00?logo=buffer&logoColor=fff&style=flat) RF 3 - Validar Resposta API
- [ ] ![Buffer Badge](https://img.shields.io/badge/API-ff0d00?logo=buffer&logoColor=fff&style=flat)RF 4 - Consultar API
- [ ] ![Buffer Badge](https://img.shields.io/badge/API-ff0d00?logo=buffer&logoColor=fff&style=flat) RF 5 - Mostrar Resposta API

### Requisitos Não-Funcionais
- [x] RNF 1 - Design Responsivo (Usabilidade)
- [x] RNF 2 - Tratamento de Erros (Confiabilidade)

### Regras de Negócio
- [x] RGN 1 - Formato das Credenciais
- [x] RGN 2 - Validação de E-mail
- [x] RGN 3 - Tempo de Bloqueio
- [x] RGN 4 - Expiração da Senha
- [x] RGN 5 - Integração com Outros Sistemas

---

## Legenda
* RF - `Requisito Funcional`
* RNF - `Requisito Não Funcional`
* RGN - `Regra de Negócio`
* RC - `Requisito Complementar`

---

### Requisitos Funcionais

#### RF 1. Pesquisar Pokémon
##### DESCRIÇÃO: O sistema deve permitir que o usuário busque Pokémon existentes no sistema com base em diferentes critérios.

* O sistema deve fornecer uma interface de pesquisa que permita ao usuário inserir os critérios de busca.
* Os critérios de busca devem incluir pelo menos:
  * Nome do Pokémon
  * Tipo do Pokémon
* O sistema pode oferecer critérios de busca adicionais, como:
  * Número da Pokédex
  * Habilidade
* O sistema deve realizar a busca no banco de dados com base nos critérios fornecidos.
* O sistema deve exibir os resultados da pesquisa ao usuário.
* Se a pesquisa retornar múltiplos resultados, o sistema deve apresentar os resultados em um formato paginado ou rolável.
* Se a pesquisa não retornar resultados, o sistema deve exibir uma mensagem apropriada ao usuário.

#### RC 4. Ordenação dos Resultados
* O sistema deve permitir que o usuário ordene os resultados da pesquisa por diferentes critérios (e.g., nome, número da Pokédex).
* O sistema deve fornecer opções para ordenação ascendente e descendente.
  
#### RC 5. Filtragem dos Resultados
* O sistema deve permitir que o usuário refine os resultados da pesquisa aplicando filtros adicionais (e.g., filtrar por um subconjunto de tipos, filtrar por geração).

#### RC 6. Exibição Detalhada na Lista
* Além do nome, a lista de resultados da pesquisa deve exibir informações adicionais resumidas sobre cada Pokémon (e.g., uma pequena imagem, o tipo primário).

#### RC 7. Sugestões de Pesquisa
* O sistema deve fornecer sugestões de pesquisa enquanto o usuário digita os critérios (autocomplete), ajudando a encontrar Pokémon com nomes semelhantes ou a corrigir erros de digitação.


* [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O sistema deve conter dados de Pokémon para serem pesquisados.
* [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O usuário deve ter acesso à funcionalidade de pesquisa.
* [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema exibe os resultados da pesquisa ao usuário, ou uma mensagem informando que nenhum resultado foi encontrado.


#### RF 3. Listar Pokemon
##### DESCRIÇÃO: O sistema deve permitir que o usuário visualize uma lista de todos os Pokémon cadastrados no sistema.

* O sistema deve recuperar a lista de Pokémon do banco de dados.
* O sistema deve exibir a lista de Pokémon na interface do usuário.
* A lista deve apresentar informações resumidas sobre cada Pokémon, como:
  * Nome
  * Número da Pokédex
  * Tipo(s)
  * Imagem (opcional, pode ser um thumbnail)
* Se houver um grande número de Pokémon, o sistema deve implementar paginação ou rolagem infinita para exibir os resultados de forma eficiente.
* O sistema deve permitir que o usuário selecione um Pokémon da lista para visualizar os detalhes completos (caso de uso "Visualizar Pokémon").

#### RC 8. Ordenação da Lista:

* O sistema deve permitir que o usuário ordene a lista de Pokémon por diferentes critérios.
* Critérios de ordenação suportados:
  * Nome (ascendente e descendente)
  * Número da Pokédex (ascendente e descendente)

#### RC 9. Filtragem da Lista:

* O sistema deve permitir que o usuário filtre a lista de Pokémon por tipo(s).
* O usuário deve poder selecionar um ou mais tipos para filtrar a lista.

#### RC 10. Tamanho da Página Configurável:

* Se a lista for paginada, o sistema deve permitir que o usuário configure o número de Pokémon exibidos por página.
* Opções de tamanho de página: 10, 20, 50.

#### RC 11. Exibição de Detalhes Resumidos:

* A lista deve exibir informações resumidas para cada Pokémon, além do nome e número.
* Informações exibidas:
  * Miniatura da imagem do Pokémon
  * Tipo primário do Pokémon

#### RC 12. Opção de Exportar a Lista:

* O sistema deve fornecer uma opção para o usuário exportar a lista de Pokémon para um formato de arquivo (e.g., CSV).

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O sistema deve conter dados de Pokémon para serem listados.
- [x] ![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O usuário deve ter acesso à funcionalidade de listar Pokémon.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema exibe a lista de Pokémon ao usuário, ou uma mensagem informando que nenhum Pokémon foi encontrado.


#### RF 4. Visualizar Pokémon

* O sistema deve permitir que o usuário faça logout da sua sessão.
* O sistema deve invalidar a sessão do usuário após o logout.

#### RC 11. O sistema deve definir um período de tempo para o bloqueio da conta (e.g., 5 minutos, 1 hora). 

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O usuário deve ter inserido credenciais incorretas um número específico de vezes.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema deve impedir o acesso à conta até que o bloqueio seja removido.

---

### Requisitos Não Funcionais

#### RNF 1. Design Responsivo (Usabilidade)

##### DESCRIÇÃO: A interface do usuário deve se adaptar a diferentes tamanhos e tipos de dispositivos.

* O sistema deve garantir que a interface seja acessível em dispositivos móveis, tablets e desktops.
* O sistema deve manter a usabilidade e a agradabilidade visual em diferentes resoluções de tela.
* O sistema pode usar técnicas de design responsivo, como media queries em CSS.


#### RNF 2. Tratamento de Erros (Confiabilidade)

##### DESCRIÇÃO: O sistema deve lidar com erros de forma adequada e fornecer feedback informativo ao usuário.

* O sistema deve tratar a entrada inválida do usuário (e.g., pesquisa por um termo inexistente).
* O sistema deve lidar com a situação em que um item procurado não existe (e.g., "Pokémon não encontrado").
* O sistema deve tratar erros de conexão com a API ou outras falhas de comunicação.
* O sistema deve exibir mensagens de erro claras e compreensíveis para o usuário.

---

### Regras de Negócio

#### RGN 1. Unicidade do Nome do Pokémon

* O nome de usuário deve ter no mínimo X caracteres e no máximo Y caracteres.
* A senha deve ter no mínimo A caracteres, conter pelo menos um caractere maiúsculo, um caractere minúsculo, um número e um caractere especial.

#### RC 1. As configurações do sistema de login (e.g., número de tentativas de login, tempo de bloqueio) devem ser facilmente alteráveis.


#### RGN 2. Validade dos Tipos de Pokémon

* O e-mail fornecido para recuperação de senha deve ser um e-mail válido.

#### RC 4. O sistema deve verificar a força da senha durante o cadastro e fornecer feedback ao usuário.  


#### RGN 3. Intervalo Válido para Atributos

* A conta do usuário deve ser bloqueada por N minutos após M tentativas de login inválidas.

#### RC 10. O sistema deve permitir que o usuário escolha o método de MFA preferido.


#### RGN 4. Número da Pokédex Único
##### DESCRIÇÃO: O número da Pokédex atribuído a cada Pokémon deve ser único dentro do sistema. Não deve ser permitido cadastrar ou atualizar um Pokémon com um número de Pokédex que já esteja atribuído a outro Pokémon.

* Ao inserir um novo Pokémon, o sistema deve realizar uma verificação para garantir que o número da Pokédex fornecido pelo usuário (ou gerado automaticamente) não existe no banco de dados.
* Ao atualizar um Pokémon, se o número da Pokédex for modificado, o sistema deve realizar a mesma verificação de unicidade antes de salvar as alterações.
* Se o número da Pokédex já existir, o sistema deve exibir uma mensagem de erro clara e informativa ao usuário, impedindo a operação de inserção ou atualização.

#### RC 11. Geração Automática do Número da Pokédex
* O sistema deve manter um controle do último número da Pokédex utilizado ou consultar o banco de dados para determinar o próximo número disponível.
* O número gerado automaticamente deve ser atribuído ao novo Pokémon.
* O usuário deve ter a opção de aceitar o número gerado ou inserir um número manualmente (sujeito à regra de unicidade).

#### RC 11. Mensagem de Erro Detalhada
* A mensagem de erro deve incluir o número da Pokédex que já está em uso.
* A mensagem de erro deve incluir o nome do Pokémon que já possui esse número da Pokédex.
* A mensagem deve sugerir ações corretivas ao usuário (por exemplo, inserir um número diferente ou pesquisar o Pokémon existente).

#### RC 11. Configuração do Início da Numeração (Opcional)
* Um administrador do sistema deve poder definir o valor do primeiro número da Pokédex a ser utilizado.
* Essa configuração deve ser persistente.

#### RC 11. Validação do Formato (Opcional)
* O sistema deve verificar se o valor inserido é um número.
* O sistema deve verificar se o número é um inteiro.
* O sistema deve verificar se o número é maior que zero.

#### RGN 5. Formato da Imagem
##### DESCRIÇÃO: Se o sistema permitir o upload de imagens para os Pokémon, as imagens devem estar em um formato válido (e.g., JPG, PNG) e podem ter restrições de tamanho ou dimensões.

* Ao inserir ou atualizar um Pokémon, se uma imagem for fornecida, o sistema deve verificar se o formato do arquivo é suportado.
* O sistema pode verificar se o tamanho do arquivo da imagem não excede um limite máximo.
* O sistema pode verificar se as dimensões da imagem estão dentro de limites aceitáveis.

#### RC 11: Unicidade do Nome do Pokémon
##### RGN X: O nome de cada Pokémon deve ser único no sistema.
* Se o usuário tentar inserir um Pokémon com um nome já existente, o sistema deve fornecer sugestões de nomes alternativos (e.g., adicionando um número ao final do nome).
* O sistema deve exibir uma lista de sugestões ao usuário, permitindo que ele escolha um dos nomes sugeridos ou insira um nome diferente.

#### RC 12: Unicidade do Nome do Pokémon
##### RGN X: Cada Pokémon deve ter pelo menos um e no máximo dois tipos válidos
* O sistema deve fornecer uma interface amigável para a seleção de tipos, como uma lista de seleção ou botões de opção, em vez de exigir que o usuário insira os tipos manualmente.
* A interface deve exibir os ícones ou cores associados a cada tipo para facilitar a identificação.

#### RC 12: Unicidade do Nome do Pokémon
* O sistema deve validar os tipos selecionados em tempo real, fornecendo feedback imediato ao usuário se ele selecionar um número inválido de tipos.

#### RC 12: Exibição de Intervalos
* O sistema deve exibir os intervalos válidos para cada atributo na interface do usuário, para que o usuário saiba quais valores são aceitáveis.

#### RC 12: Ajuste Automático de Valores
* Se o usuário inserir um valor fora do intervalo válido, o sistema deve ajustá-lo automaticamente para o limite mais próximo (mínimo ou máximo) em vez de apenas exibir um erro.
* O sistema deve fornecer feedback visual ao usuário quando um valor for ajustado automaticamente.

#### RC 12: Geração Automática (Opcional)
* O sistema deve oferecer a opção de gerar automaticamente o próximo número da Pokédex disponível, em vez de exigir que o usuário o insira manualmente.

#### RC 12: Mensagem de Erro Detalhada
* Se o usuário tentar inserir um Pokémon com um número de Pokédex já existente, a mensagem de erro deve incluir o nome do Pokémon que já possui esse número.

#### RC 12: Pré-visualização da Imagem
* O sistema deve exibir uma pré-visualização da imagem que o usuário está tentando enviar antes de salvá-la, para que ele possa verificar se está correta.

#### RC 12: Pré-visualização da Imagem
* Se o usuário enviar uma imagem em um formato não suportado, o sistema deve tentar convertê-la automaticamente para um formato válido (se possível) em vez de apenas rejeitá-la.
