# REQUISITOS

## Referência do Projeto
[Como criar uma Pokedex com HTML, CSS e JavaScript | Projeto Completo](https://www.youtube.com/watch?v=SjtdH3dWLa8)

## Legenda
* RF - `Requisito Funcional`
* RNF - `Requisito Não Funcional`
* RGN - `Regra de Negócio`
* RC - `Requisito Complementar`

### Requisitos Funcionais

#### RF 1.  Inserir Pokemon

##### DESCRIÇÃO: O sistema deve permitir que o usuário cadastre novos Pokémon no sistema, fornecendo as informações necessárias sobre o Pokémon.
##### DESCRIÇÃO: O sistema deve permitir que o usuário cadastre novos Pokémon no sistema, fornecendo as informações necessárias sobre o Pokémon.

* O sistema deve apresentar um formulário de inserção que permita ao usuário fornecer os dados do Pokémon.
* O formulário deve incluir campos para:
  * Nome do Pokémon
  * Tipo(s) do Pokémon
  * Atributos do Pokémon (e.g., HP, Ataque, Defesa, Velocidade)
  * Habilidades do Pokémon
  * Imagem do Pokémon (opcional)
* O sistema deve validar os dados fornecidos pelo usuário antes de salvar o Pokémon. As validações devem incluir:
  * Verificar se o nome do Pokémon é único.
  * Verificar se os tipos do Pokémon são válidos (pertencem a uma lista predefinida).
  * Verificar se os valores dos atributos estão dentro de um intervalo válido.
  * Verificar se a imagem (se fornecida) está em um formato válido.
  * Se os dados forem válidos, o sistema deve salvar as informações do Pokémon no banco de dados.
* Após a inserção bem-sucedida, o sistema deve exibir uma mensagem de confirmação ao usuário.
* Se ocorrerem erros durante a inserção, o sistema deve exibir mensagens de erro claras e informativas ao usuário, indicando os campos que contêm erros e a natureza dos erros.


#### RC 1. O sistema deve fornecer uma lista de seleção para os tipos de Pokémon, permitindo que o usuário escolha entre os tipos válidos.
#### RC 2. O sistema deve permitir que o usuário visualize uma prévia da imagem antes de salvar o Pokémon.
#### RC 3. O sistema deve fornecer mensagens de erro detalhadas que expliquem como corrigir cada erro de validação.

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O usuário deve estar autenticado no sistema e ter permissão para inserir Pokémon.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O Pokémon deve ser armazenado no banco de dados.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema deve exibir uma mensagem de confirmação ou erro ao usuário.

### Fluxo Principal (Sucesso) [RF1]

1) O usuário inicia o processo de inserção de um novo Pokémon no sistema.
2) Exibição do Formulário: O sistema exibe o formulário de inserção, contendo os campos necessários para coletar as informações do Pokémon (nome, tipo, atributos, etc.).
3) Preenchimento do Formulário: O usuário preenche todos os campos obrigatórios e opcionais do formulário com os dados do Pokémon.
4) Validação dos Dados: O sistema valida os dados inseridos pelo usuário, verificando se atendem aos critérios de validação predefinidos (unicidade do nome, tipos válidos, intervalos de atributos, etc.).
5) Salvamento do Pokémon: Se os dados forem considerados válidos, o sistema salva as informações do Pokémon no banco de dados.
6) Confirmação de Sucesso: O sistema exibe uma mensagem de confirmação ao usuário, indicando que o Pokémon foi inserido com sucesso.
7) Fim do Caso de Uso: O caso de uso é concluído. O sistema pode retornar à tela anterior ou exibir a lista de Pokémon.

#### Fluxo Alternativo

##### 1a. Dados Inválidos:
* O usuário preenche o formulário de inserção.
* O sistema valida os dados inseridos.
* O sistema identifica um ou mais erros de validação.
* O sistema exibe uma mensagem de erro ao usuário, indicando quais campos contêm erros e a natureza dos erros.
* O sistema mantém o usuário no formulário de inserção, permitindo que ele corrija os dados.
* O caso de uso retorna ao passo em que o usuário preenche o formulário (ou um passo anterior, dependendo da implementação).

##### 1b. Cancelamento da Inserção:
* O usuário inicia o processo de inserção.
* O sistema exibe o formulário de inserção.
* O usuário decide cancelar a inserção.
* O sistema abandona o processo de inserção e retorna à tela anterior (ou a um menu principal).

##### 1c. Erro de Sistema ao Salvar:
* O usuário preenche o formulário de inserção.
* O sistema valida os dados inseridos.
* Os dados são considerados válidos.
* O sistema encontra um erro ao tentar salvar o Pokémon no banco de dados (e.g., falha de conexão, erro de banco de dados).
* O sistema exibe uma mensagem de erro ao usuário, indicando que não foi possível salvar o Pokémon.
* O sistema pode oferecer opções para o usuário tentar novamente ou cancelar a operação.

* ##### 1c. Tempo Expirado da Sessão:
* O usuário inicia o processo de inserção.
* O sistema exibe o formulário de inserção.
* O usuário demora muito para preencher o formulário.
* A sessão do usuário expira.
* O sistema redireciona o usuário para a tela de login ou exibe uma mensagem informando sobre a expiração da sessão.


#### RF 2. Pesquisar Pokemon

* O sistema deve permitir que o usuário solicite a recuperação de senha.
* O sistema deve solicitar um identificador do usuário (ex: e-mail, nome de usuário).
* O sistema deve enviar um link ou código de recuperação para o identificador fornecido.
* O sistema deve permitir que o usuário defina uma nova senha após a verificação do link/código.

#### RC 4. O sistema deve implementar medidas de segurança para prevenir o uso indevido da funcionalidade de recuperação de senha (e.g., limitação de tentativas). 

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O usuário deve ter uma conta registrada no sistema com um e-mail válido associado.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema deve permitir que o usuário defina uma nova senha.


#### RF 3. Listar Pokemon

* O sistema deve bloquear a conta do usuário após um número configurável de tentativas de login inválidas.
* O sistema deve informar ao usuário que a conta foi bloqueada e o tempo para desbloqueio ou o procedimento para desbloqueá-la.

#### RC 10. O sistema deve definir um período de tempo para o bloqueio da conta (e.g., 5 minutos, 1 hora).

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O sistema deve definir um período de tempo para o bloqueio da conta (e.g., 5 minutos, 1 hora). 
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O usuário deve ter inserido credenciais incorretas um número específico de vezes.


#### RF 4. Visualizar Pokémon

* O sistema deve permitir que o usuário faça logout da sua sessão.
* O sistema deve invalidar a sessão do usuário após o logout.

#### RC 11. O sistema deve definir um período de tempo para o bloqueio da conta (e.g., 5 minutos, 1 hora). 

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O usuário deve ter inserido credenciais incorretas um número específico de vezes.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema deve impedir o acesso à conta até que o bloqueio seja removido.


#### RF 5. Exibir Mensagens de Erro

* O sistema deve exibir mensagens de erro claras e informativas para falhas de login (e.g., credenciais inválidas, conta bloqueada). 

#### RC 12. As mensagens de erro devem ser localizadas para diferentes idiomas.

- [x] [![Faculdade Badge](https://img.shields.io/badge/-PRÉ_CONDIÇÕES-gold)]() O usuário deve ter inserido credenciais inválidas.
- [x] [![Faculdade Badge](https://img.shields.io/badge/-PÓS_CONDIÇÕES-red)]() O sistema deve permanecer na tela de login, aguardando novas tentativas ou ações do usuário.

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


#### RNF 3. Usabilidade

##### DESCRIÇÃO: A interface de login deve ser acessível a usuários com deficiência visual (e.g., suporte a leitores de tela). 

* A interface de login deve ser intuitiva e fácil de usar.
* As mensagens de erro devem ser claras e informativas.
* O sistema deve fornecer feedback visual ao usuário durante o processo de login.


#### RNF 4. Manutenibilidade

* O código do módulo de login deve ser modular e fácil de manter.
* As configurações de segurança (ex: número de tentativas de login) devem ser facilmente configuráveis.

#### RC 11. O sistema deve implementar mecanismos de redundância e failover para garantir a alta disponibilidade. 

### Regras de Negócio

#### RGN 1. Formato das Credenciais

* O nome de usuário deve ter no mínimo X caracteres e no máximo Y caracteres.
* A senha deve ter no mínimo A caracteres, conter pelo menos um caractere maiúsculo, um caractere minúsculo, um número e um caractere especial.

#### RC 1. As configurações do sistema de login (e.g., número de tentativas de login, tempo de bloqueio) devem ser facilmente alteráveis.


#### RGN 2. Validação de E-mail

* O e-mail fornecido para recuperação de senha deve ser um e-mail válido.

#### RC 4. O sistema deve verificar a força da senha durante o cadastro e fornecer feedback ao usuário.  


#### RGN 3. Tempo de Bloqueio

* A conta do usuário deve ser bloqueada por N minutos após M tentativas de login inválidas.

#### RC 10. O sistema deve permitir que o usuário escolha o método de MFA preferido.


#### RGN 4. Expiração da Senha

* A senha do usuário deve expirar a cada D dias, forçando a troca.

#### RC 11. O sistema deve definir um processo para reativar contas inativas. 


#### RGN 5. Integração com Outros Sistemas

* O sistema de login deve ser capaz de se integrar com outros sistemas da empresa (e.g., CRM, ERP).

#### RC 11. A integração deve ser baseada em padrões de autenticação abertos (e.g., OAuth 2.0, SAML)

---

## Artefatos Elaborados e Entregues
### Requisitos Funcionais
- [x] RF 1 - Autenticar Usuário
- [x] RF 2 - Recuperar Senha
- [x] RF 3 - Bloquear Conta
- [x] RF 4 - Logout
- [x] RF 5 - Exibir Mensagens de Erro

### Requisitos Não-Funcionais
- [x] RNF 1 - Segurança
- [x] RNF 2 - Desempenho
- [x] RNF 3 - Usabilidade
- [x] RNF 4 - Manutenibilidade
- [x] RNF 5 - Confiabilidade

### Regras de Negócio
- [x] RGN 1 - Formato das Credenciais
- [x] RGN 2 - Validação de E-mail
- [x] RGN 3 - Tempo de Bloqueio
- [x] RGN 4 - Expiração da Senha
- [x] RGN 5 - Integração com Outros Sistemas
