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
  - Atributos básicos: CPF, telefone, nome.

- **Empréstimo:** 
  - ID de empréstimo como chave primária identificando cada empréstimo feito.
  - Atributos básicos: data do empréstimo, data de devolução.

### Requisitos Adicionais

- **Livro:** 
  - Tipo de capa, faixa de idade indicada, número de cópias na biblioteca, localização, assunto abordado.

- **Pessoa:** 
  - Superclasse para agrupar atributos semelhantes entre funcionário e usuário.

- **Funcionário (Especialização):** 
  - Gerente com adicional salarial como atributo.

- **Empréstimo:** 
  - Adicional de multa como atributo composto.

- **Departamento:** 
  - Nome, número de funcionários, tipo.

- **Autor:** 
  - Nome do livro mais solicitado como atributo adicional.

- **Editora:** 
  - CNPJ como chave, nome, quantidade de livros, contato.

- **Equipamento:** 
  - ID do equipamento como chave.
  - Atributos: quantidade, restrito (booleano), descrição.

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

- **Empréstimo:** 
  - Autorizado por um funcionário.
  - Livro pode ser solicitado para um empréstimo.
  - Empréstimo pode ser solicitado por um leitor.

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
