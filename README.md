# BD1_2024.1--Pedro_Benedito
# Relatório

## Aluno: Pedro Benedito
## Disciplina: Banco de Dados 1

### Descrição
O projeto escolhido foi sobre a biblioteca com o objetivo de construir um modelo de entidade relacional usando o software brmodelo sob orientação do professor Lucas.

### Requisitos Mínimos

- **Livro:** 
  - ISBN como chave primária.
  - Atributos básicos: título, número de páginas e gênero.

- **Autor:** 
  - Nome completo como unicidade.
  - Atributos básicos: data de nascimento e número de livros escritos.

- **Funcionário:** 
  - CPF como chave primária.
  - Atributos básicos: nome, salário, data de admissão e turno.

- **Leitor/Usuário:** 
  - CPF como chave primária.
  - Atributos básicos:telefone, nome.

- **Empréstimo:** 
  - ID de empréstimo como chave primária identificando cada empréstimo feito.
  - Atributos básicos: data do empréstimo, data de devolução.

### Requisitos Adicionais

- **Livro:** 
  - tipo de capa, faixa de idade indicada, número de copias na biblioteca, localização, assunto abordado, esses atributos foram adicionados com base em análises de um uma biblioteca real  
- **Pessoa:** 
  - fiz essa superclasse pois tinham funcionário e usuário com atributos CPF, nome e telefone semelhantes  

- **Funcionário (Especialização):** 
  -  como especialização de funcionário coloquei gerente pois é essencial alguém que coordene os demais funcionários e coloquei um adicional salarial como atributo pois é o que geralmente acontece com gerentes  

- **Empréstimo:** 
  - fiz um adicional de multa para que caso o usuário não devolva livro no tempo limite terá uma a multa que é um atributo composto, pois será dividida em acumulativa e fixa onde acumulativa é por quantidades de dia de atraso e a fixa para atraso 

(observação) coloquei como relações de livro, usuário e funcionário com empréstimo então fiquei em dúvida se especificava o nome de quem solicitou empréstimo e quem autorizou e o livro emprestado como atributos de empréstimo ou não, decidi não os deixar como atributo pois ficou redundante.

- **Departamento:** 
  - criei essa entidade pois funcionários de um tipo específico são agrupados em departamentos exemplo limpeza, segurança, atendimento e administração da biblioteca, defini como atributos nome departamento, número de funcionários que trabalham nesse departamento e o tipo desse departamento  

- **Autor:** 
  - adicionei como atributos o nome do livro mais solicitado, achei interessante ter esse dado  

- **Editora:** 
  - adicionei essa entidade com cnpj de chave e nome, quantidade de livros e contato adicionei essa entidade com tais atributos pois acho valido ter dados de quem fornece os livros para biblioteca  

- **Equipamento:** 
  - defini como chave o id do equipamento e adicionei os demais atributos quantidade de equipamentos, restrito (booleano para saber se é restrito para funcionários de um departamento ou não) e descrição de equipamento. Defini essa entidade e atributos pensando em como ocorre um controle itens que tem em uma biblioteca até para fins de solicitação de adicionar mais (exemplo quantidade de computadores disponíveis, quais são de uso restrito e quais não são) 

  ### EXTRA
  **Fila de espera:** 
   - coloquei a fila de espera como adicional extra para caso um livro tenha sido solicitado por muitos usuarios ou não tenha disponibilidade suficiente do mesmo, como atrbutos coloquei limite da lista para não ficar muito grande, numero de pessoas contidas na lista para saber se é possivel entrar , id da lista para registrar qual fila de espera está entrando,numero na fila pra saber sua colocação para pegar o livro( primeiro, segundo e etc) e por ultimo adicionei o atributo tempo medio de espera. Relações da fila de espera são  com o livro que está contido para esssa lista de espera e com 
   o usuario que se inscreve em uma ou mais listas de espera 
### Relações

As relações geradas a partir dessas entidades foram:

- **Livro:** 
  - Escrito por um ou mais autores.
  - Publicado por uma ou mais editoras.
  - Autorizado para um ou mais empréstimos.

- **Funcionário:** 
  - Trabalha em um departamento.
  - Autoriza um ou mais empréstimos.

- **Usuário/Leitor:** 
  - Solicita um ou mais empréstimos.
  - usa um ou mais itens (não restrito)

- **Empréstimo:** 
  - Autorizado por um funcionário.
  - Livro pode ser solicitado para um empréstimo.
  - pode ser solicitado por um leitor.

- **Departamento:** 
  - Gerido por um gerente.
  - Tem funcionários de um tipo trabalhando nele.
  - Possui equipamentos.

- **Autor:** 
  - Escreve um ou mais livros.

- **Editora:** 
  - Publica um ou mais livros.

- **Equipamento:** 
  - Usado por um departamento ou vários.
  - Usado por um ou mais usuários.
