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

