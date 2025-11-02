# Desafio QA Beedo

A proposta do desafio é analisar um módulo de cursos do website da Beedoo e, a partir dele, criar user stories e casos de teste, fazendo a documentação de todo o processo e dos bugs encontrados.

## Metodologia

Para realizar o desafio, apliquei os seguintes passos e técnicas:

* Exploração das páginas e funções/features com olhar crítico e detalhista.
* Criação de user stories baseado no que foi entendido do comportamento do software.
* Elaboração de casos de teste de diferentes tipos de teste a partir das user stories e das funcionalidades encontradas.
* Documentação das etapas e dos bugs achados.

Link da documentação: https://drive.google.com/drive/folders/1xIUCkBjmQHQbVwc5jjtaI-y4OucfIoIi?usp=drive_link



## Setup

A análise do website e execução dos casos de teste foram feitas nas seguintes configurações:

* Windows 11 Versão 25h2 (compilação do SO 26200.6901)
    Máquina onde este projeto foi realizado.

* Google Chrome Versão 140.0.7339.128 (Versão oficial) 64 bits
    Análise e execução dos casos de teste.
    DevTools para visualização de logs e validação de dimensão de dispositivos móveis (utilizado dimensões padrão Iphone 12).

* Visual Studio Code 1.105.1 x64
    Escrita do markdown e utilização do terminal.

* Git 2.51.0.windows.1
    Upload do markdown para o repositório github.


## User Stories

As user stories (US) a seguir seguem o padrão "Como **usuário**, quero **ação**, para **objetivo**", utilizado em metodologias ágeis, e foram estabelecidos alguns critérios de aceite (AC), que são características obrigatórias no desenvolvimento das user stories. 

Essa parte da documentação foi elaborada a partir da análise do website como um gerenciador de cursos e como ele deve atender ao público-alvo do ponto de vista do usuário (a motivação da escolha de cada user story está melhor descrita no item Objetivo de cada US).

### US01 - Exibir página com lista de cursos

Como usuário,
Quero acessar a página Lista de Cursos,
Para visualizar uma lista de todos cursos cadastrados no sistema

AC01 - A página deve exibir o título "Lista de cursos".
AC02 - Uma lista de todos os cursos deve ser exibida contendo os campos:
AC03 - O Menu deve exibir os seguites links alinhados à direita: "LISTAR CURSOS", "CADASTRAR CURSO".

Para criar essa user story e critérios de aceite 

### US02 - Exibir página de cadastro de cursos

Como usuário,
Quero acessar a página Cadastrar Curso,
Para visualizar um formulário de cadastro de cursos

AC04 - A página deve exibir o título "Cadastro de curso"
AC05 - Um formulário de cadastro deve ser exibido contendo os campos obrigatórios:
    Título
    Descrição
    Instrutor
    Url da imagem de capa
    Data de início
    Data de fim
    Número de vagas
    Tipo de curso
    Link de inscrição
    Endereço
    Botão: Cadastrar Curso
    
AC06 - O campo título não deve exceder 70 caractéres.
AC07 - O campo descrição não deve exceder 5000 caractéres.
AC08 - O campo instrutor não deve exceder 50 caractéres.
AC09 - O número de vagas não deve aceitar 0 ou valores negativos.


### US03 - Campos obrigatórios do formulário

Como usuário,
Quero ver uma mensagem de erro ao tentar cadastrar um curso sem preencher todas as informações,
Para garantir que não vou cadastrar um curso incompleto

AC10 - Os campos de data devem permitir entrada manual e seleção via calendário, no formato dd/mm/aaaa.
AC11 - Os campos de data inicial e final não deve aceitar valores anteriores ao dia atual e a data final não pode ser anterior a data inicial.
AC12 - O campo "Tipo de curso" deve ser um dropdown com as opções "Presencial", "Online".
AC13 - O campo de endereço só deve aparecer caso o tipo de curso seja presencial.
AC14 - O campo de endereço deve aceitar valores no formato rua, número, bairro, cidade/Estado.
AC15 - O campo de link de inscrição só deve aparecer caso o tipo de curso seja online.
AC16 - Ao clicar no botão "Cadastrar Curso" sem preencher todas as informações, deve ser exibida uma mensagem de erro indicando quais campos faltam ser preenchidos.

### US04 - Menu de navegação

Como usuário,
Quero clicar nos links do menu,
Para navegar entre as páginas do website


AC17 - Ao clicar nos links do menu, o usuário deve ser redirecionado para as respectivas páginas.
AC18 - O menu deve permanecer fixo quando rolar pela tela.

### US05 - Lista de cursos

Como usuário,
Quero ver uma lista de cursos cadastrados na página Lista de Cursos,
Para ver os cursos disponíveis


AC19 - Os cursos devem ser exibidos em quadros verticais, lado a lado, com 2 cursos por fileira.
AC20 - O quadro deve conter os seguintes valores na seguinte ordem:
    Imagem obtida da URL inserida no cadastro do curso
    Tipo de curso
    Título do curso
    Descrição do curso
    Data de início
    Data de fim
    Número de vagas restantes
    Botão "EXCLUIR CURSO"

AC21 - As imagens mostradas no quadro de cada curso devem se enquadrar nas dimensões: 250 width x 200 height.
AC22- - A dimensão das divs que comportam cada curso na lista deve ter as seguintes dimensões fixas: 250 width x 450 height.


### US06 - Exclusão de cursos

Como usuário,
Quero excluir um curso através de um botão,
Para eliminar os cursos que não quero utilizar

AC23 - Ao clicar no botão excluir curso, a mensagem "Curso excluído com sucesso!" deve aparecer e o curso deve desaparecer da lista.


## Cenários e casos de teste

Partindo do princípio que os cenários de teste são uma versão mais abrangente do teste de uma feature e os casos de teste são mais específicos, foram desenvolvidos cenários de teste em menor quantidade enunciar o teste de funcionalidades e casos de teste em maior quantidade que abordassem diferentes perspectivas e inputs dos cenários de teste.

Link do Google Sheets com os cenários e casos de teste (dividídos em 2 abas): https://docs.google.com/spreadsheets/d/1bcPuv4CcUD6sIy8JmHYRllqPat2WtI3YBphi74TMS2g/edit?usp=drive_link

## Bug report

Para reportar os bugs encontrados, utilizei uma planilha separada que contém as informações mais importantes de um bug report e linkei cada bug à evidências de casos de teste ou testes exploratórios (printscreens) e logs achados no DevTools. Com foco em um report o mais reproduzível possível e com clareza quanto ao erro.

Link da planilha de bugs: https://docs.google.com/spreadsheets/d/1jwQ_oUpTBlAVaUyA4ev8VVYEbWjaXrOoglmJUPcd16I/edit?usp=drive_link
