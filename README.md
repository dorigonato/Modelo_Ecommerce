# **Modelo de Banco de Dados para E-commerce**

## 📌 Descrição do Projeto
Este projeto contém um modelo de banco de dados relacional desenvolvido para um sistema de e-commerce. O objetivo é garantir a organização e escalabilidade do banco, permitindo a gestão eficiente de pedidos, pagamentos, entregas e transportadoras.

## 📌 Entidades e Relacionamentos
### 🔹 1. Cliente
- Representa os usuários do sistema.
- **Relacionamentos:**
  - Um cliente pode fazer vários pedidos **(1:N)**.
  - Um cliente pode ter várias formas de pagamento cadastradas **(1:N)**.

### 🔹 2. Pedido
- Contém as informações de compra de um cliente.
- **Relacionamentos:**
  - Um pedido pode conter vários produtos **(N:N via Item_Pedido)**.
  - Um pedido pode gerar múltiplas entregas **(1:N)**.

### 🔹 3. Produto
- Armazena informações sobre os produtos disponíveis na loja.
- **Relacionamentos:**
  - Um produto pode ter vários fornecedores **(N:N via Produto_Fornecedor)**.
  - Um produto pode estar em vários estoques **(N:N via Produto_Estoque)**.

### 🔹 4. Fornecedor
- Armazena informações dos fornecedores dos produtos.
- **Relacionamentos:**
  - Fornece produtos para a loja **(N:N via Produto_Fornecedor)**.

### 🔹 5. Estoque
- Gerencia os locais de armazenamento dos produtos.
- **Relacionamentos:**
  - Armazena vários produtos **(N:N via Produto_Estoque)**.

### 🔹 6. Transportadora
- Contém informações sobre as empresas responsáveis pelo transporte das entregas.
- **Relacionamentos:**
  - Uma transportadora pode ser responsável por várias entregas **(1:N)**.

### 🔹 7. Entrega
- Armazena as informações de rastreamento e status de envio.
- **Relacionamentos:**
  - Cada entrega pertence a um pedido **(N:1)**.
  - Cada entrega é feita por uma única transportadora **(N:1)**.

### 🔹 8. Forma de Pagamento
- Armazena os métodos de pagamento cadastrados pelos clientes.
- **Relacionamentos:**
  - Está associada a um cliente **(N:1)**.
  - Cada forma de pagamento pertence a um tipo específico **(N:1)**.

### 🔹 9. Tipo de Pagamento
- Define os diferentes métodos de pagamento disponíveis (Cartão, Boleto, Pix, etc.).
- **Relacionamentos:**
  - Um tipo de pagamento pode ser usado em várias formas de pagamento **(1:N)**.

### 🔹 10. Item_Pedido
- Entidade de relacionamento entre Pedido e Produto.
- Armazena a quantidade e preço unitário dos produtos no momento da compra.

## 📌 Tecnologias Utilizadas
- **MySQL** para armazenamento dos dados.
- **Workbench** para modelagem e estruturação.
- **GitHub** para versionamento do projeto.


