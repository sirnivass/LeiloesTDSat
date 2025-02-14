# Sistema de Leilões

Este projeto é um sistema de leilões desenvolvido em Java utilizando a biblioteca Swing para a interface gráfica e JDBC para a conexão com o banco de dados MySQL. O sistema permite o cadastro, listagem e venda de produtos.

## Funcionalidades

- **Cadastro de Produtos**: Permite cadastrar novos produtos com nome, valor e status inicial "À Venda".
- **Listagem de Produtos**: Exibe uma tabela com os produtos cadastrados, incluindo ID, nome, valor e status.
- **Venda de Produtos**: Permite realizar a venda de um produto informando seu ID.
- **Consulta de Vendas**: (Funcionalidade planejada, mas não implementada no código fornecido).

## Estrutura do Projeto

### Classes Principais

1. **`cadastroVIEW`**:
   - Interface gráfica para o cadastro de produtos.
   - Campos para entrada de nome e valor do produto.
   - Botão para cadastrar o produto e outro para consultar a lista de produtos.

2. **`listagemVIEW`**:
   - Interface gráfica para listar os produtos cadastrados.
   - Exibe uma tabela com os produtos e permite realizar a venda de um produto informando seu ID.

3. **`ProdutosDTO`**:
   - Classe de transferência de dados (DTO) para representar os produtos.
   - Contém os atributos: `id`, `nome`, `valor` e `status`.

4. **`ProdutosDAO`**:
   - Classe de acesso a dados (DAO) para manipular os produtos no banco de dados.
   - Métodos:
     - `cadastrarProduto`: (Implementação pendente) Cadastra um novo produto no banco de dados.
     - `listarProdutos`: Retorna uma lista de produtos cadastrados.

5. **`conectaDAO`**:
   - Classe responsável pela conexão com o banco de dados MySQL.
   - Método:
     - `connectDB`: Estabelece a conexão com o banco de dados.

### Banco de Dados

- O sistema utiliza um banco de dados MySQL chamado `uc11`.
- A conexão é configurada no método `connectDB` da classe `conectaDAO`.

### Interface Gráfica

- Desenvolvida utilizando o NetBeans GUI Builder.
- Componentes principais:
  - **JTable**: Para exibir a lista de produtos.
  - **JTextField**: Para entrada de dados no cadastro de produtos.
  - **JButton**: Para ações como cadastrar, listar e vender produtos.

## Requisitos

- **Java**: Versão 8 ou superior.
- **MySQL**: Banco de dados para armazenar os produtos.
- **NetBeans**: IDE utilizada para o desenvolvimento do projeto.

## Configuração do Ambiente

1. Clone o repositório do projeto.
2. Configure o banco de dados MySQL:
   - Crie um banco de dados chamado `uc11`.
   - Configure as credenciais de acesso no método `connectDB` da classe `conectaDAO`.
3. Importe o projeto no NetBeans.
4. Compile e execute o projeto.

## Como Usar

1. **Cadastro de Produtos**:
   - Abra a interface de cadastro.
   - Insira o nome e o valor do produto.
   - Clique no botão "Cadastrar".

2. **Listagem de Produtos**:
   - Abra a interface de listagem.
   - Visualize os produtos cadastrados na tabela.

3. **Venda de Produtos**:
   - Na interface de listagem, insira o ID do produto no campo correspondente.
   - Clique no botão "Vender".

## Autor

- **Nome**: Adm