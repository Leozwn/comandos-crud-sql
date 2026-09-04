# Comando CRUD para o banco de dados Fly By Night

## INSERT na tabela de Fornecedores

```sql
INSERT INTO fornecedores (nome) VALUES('Eletrônicos Tabajara');

INSERT INTO fornecedores (nome) VALUES
('Games ABCD'),
('Supermercado Tem de Tudo'),
('Livraria Demais da Conta');
```

## INSERT na tabela de Produtos
```sql
INSERT INTO produtos (nome, descricao, preco, quantidade, fornecedor_id) 
VALUES(
    'Smartphone Galaxy S26',
    'Equipamento com sistema Android e câmera Full HD e etc e tal',
    7899.99,
    20,
    1 -- id do forncedor ELetrônicos Tabajara
);

INSERT INTO produtos (nome, descricao, preco, quantidade, fornecedor_id) 
VALUES(
    'Senhor dos Anéis: As Duas Torres',
    'Volume 2 da série de livros criados pelo autor J.R.R Tolkien',
    80.99,
    100,
    4 -- id do forncedor Livraria
);

INSERT INTO produtos (nome, descricao, preco, quantidade, fornecedor_id) 
VALUES(
    'Tv Led',
    'Tela de 50 polegadas, resolução 4K, 4 entradas HDMI e etc e tal',
    3490,
    12,
    1 -- id do forncedor ELetrônico Tabajara
);
```


## INSERT na tabela de Lojas
```sql
-- Insira as lojas: Casas Bahia, Shopping Zona Leste, Bazar das Coisas e Americanas
INSERT INTO lojas(nome) VALUE('Casas Bahia');
INSERT INTO lojas(nome) VALUE('Shopping Zona Leste');
INSERT INTO lojas(nome) VALUE('Bazar das Coisas');
INSERT INTO lojas(nome) VALUE('Americanas');
```

## INSERT na tabela  Lojas-Produtos

Esta é uma tabela intermediária (também conhecida como **tabela pivot**), ou seja, ela se relaciona  com outras duas tabelas: **produtos** e **lojas** através de chaves estrangeiras.

```sql
INSERT INTO lojas_produtos(loja_id, produto_id, estoque) VALUES(2, 1, 20);


```
