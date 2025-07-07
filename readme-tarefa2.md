# 📊 Atividade — Relacionamento de Entidades no Diagrama EER | Projeto CellShop

## 🎯 Objetivo da Atividade

Construir no **MySQL Workbench** os relacionamentos entre as tabelas do projeto **CellShop**, usando o **Editor EER Diagrams**, com base nas entidades já criadas no banco de dados.

---

## 🧱 Tabelas disponíveis no banco

As tabelas **já estão criadas** com seus respectivos campos e chaves primárias (`PK`). São elas:

- `cliente`
- `venda`
- `produto`
- `itemVenda`
- `pagamento`

---

## 🔗 Instruções da Atividade

### 1. Criar Diagrama EER no MySQL Workbench

- Vá em **File > New Model**
- No menu lateral, clique em **Add Diagram**
- Use **“Add Table”** para importar ou representar as tabelas existentes

### 2. Criar os Relacionamentos entre as tabelas

Utilize as ferramentas visuais do Workbench para **definir os relacionamentos** a seguir:

| Relacionamento            | Tipo   | Tabela origem     | Tabela destino     | Campo FK                  |
|---------------------------|--------|-------------------|---------------------|---------------------------|
| Cliente → Venda           | 1:N    | `cliente`         | `venda`             | `cliente_id_cliente`      |
| Venda → ItemVenda         | 1:N    | `venda`           | `itemVenda`         | `venda_id_venda`          |
| Produto → ItemVenda       | 1:N    | `produto`         | `itemVenda`         | `produto_id_produto`      |
| Venda → Pagamento         | 1:1    | `venda`           | `pagamento`         | `venda_id_venda`          |

> ⚠️ **Atenção:**  
> Certifique-se de que os campos estrangeiros (`FK`) estão corretamente nomeados e conectados às suas respectivas chaves primárias (`PK`).

---


## ✅ Entregáveis

- Diagrama EER completo com os relacionamentos criados
- Tabelas conectadas pelas FKs corretas
- Arquivo `.mwb` salvo e entregue ao professor

---

## 🎓 Reflexão

> *"Relacionar tabelas é como conectar ideias: quando tudo conversa no banco de dados, o sistema pensa por você."*

---

**Boa prática e que a modelagem esteja com você!** ⚔️📘
