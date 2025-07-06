# 📦 CellShop — Visão Geral da Modelagem de Dados

Este projeto simula o funcionamento de uma loja de celulares e acessórios, com ênfase na estrutura de banco de dados relacional.  
Ideal para alunos que estão aprendendo modelagem de dados, SQL e fundamentos de relacionamento entre entidades.

---

## 🧠 Objetivo

Demonstrar como criar um **modelo lógico de banco de dados**, representado por entidades, atributos e relacionamentos, com base no cenário de vendas em uma loja fictícia chamada **CellShop**.

---

## 🧱 Entidades e Atributos

### 🧑‍💼 Cliente
Armazena os dados dos compradores.

- `id_cliente` — Chave primária
- `nome`
- `cpf`
- `email`
- `telefone`

📘 Um cliente pode fazer várias compras. Cada cliente tem um identificador único.

---

### 📱 Produto
Representa os itens disponíveis para venda.

- `id_produto` — Chave primária
- `descricao`
- `preco`
- `garantia_meses`

📘 Os produtos são vendidos em diferentes transações e precisam ser identificados de forma única.

---

### 🧾 Venda
Registra cada transação realizada.

- `id_venda` — Chave primária
- `data_venda`
- `id_cliente` — Chave estrangeira que referencia `Cliente`

📘 Cada venda é feita por um cliente específico. Uma venda pode conter vários itens.

---

### 📦 ItemVenda
Detalha os produtos vendidos em cada transação.

- `id_item` — Chave primária
- `id_venda` — Chave estrangeira que referencia `Venda`
- `id_produto` — Chave estrangeira que referencia `Produto`
- `quantidade`
- `subtotal`

📘 Representa os produtos incluídos na venda. Cada item está ligado a uma venda e a um produto.

---

### 💳 Pagamento
Define como a compra foi quitada.

- `id_pagamento` — Chave primária
- `id_venda` — Chave estrangeira que referencia `Venda`
- `forma_pagamento` — Cartão, Pix, Boleto etc.
- `valor_pago`
- `parcelas`

📘 Cada venda possui uma forma de pagamento. O número de parcelas é importante para controle financeiro.

---

## 🔗 Relacionamentos entre Entidades

| Relacionamento             | Tipo     | Descrição                                                                 |
|----------------------------|----------|----------------------------------------------------------------------------|
| Cliente → Venda            | 1:N      | Um cliente pode realizar várias vendas, mas cada venda tem um único cliente |
| Venda → ItemVenda          | 1:N      | Uma venda pode conter diversos itens                                     |
| Produto → ItemVenda        | 1:N      | Um produto pode aparecer em vários itens de venda                         |
| Venda → Pagamento          | 1:1      | Cada venda possui um pagamento associado                                 |

---

## 🧩 Diagrama ER (Resumo Visual)
[Cliente]───<Venda>───[ItemVenda]───[Produto] │ │ │ 
└────────────<Pagamento>────────────┘

![18](https://github.com/user-attachments/assets/0a634dc9-10e8-4f70-aaf4-395cf364e3d0)

![19](https://github.com/user-attachments/assets/278e31d4-fe00-4448-8ffe-7a8d46ebb846)

![20](https://github.com/user-attachments/assets/b06a174e-9314-4eef-b4b3-2c684c721fe7)

![21](https://github.com/user-attachments/assets/fc26e92c-dc66-4654-a59b-2eac304ae25d)

![22](https://github.com/user-attachments/assets/27855702-ce85-44be-85b5-c4dd2267384a)


## 📚 Aprendizado Esperado

- Identificar entidades e atributos em sistemas reais
- Compreender e aplicar chaves primárias e estrangeiras
- Representar relacionamentos e cardinalidades
- Preparar a estrutura lógica para implementação em SQL
