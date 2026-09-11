# SQL SELECT - Ezemplos de consultas ao banco Fly By Night

O comando `SELECT` é usado para **consultar dados armazenadis nas tabekas do banco de dados**.

## SELECT básico

Consultar todos os dados de uma tabela:
```sql
SELECT * FROM produtos;
```

## SELECT para apenas determinadas colunas

```sql
SELECT nome, preco FROM produtos;
```

## Alterando o nome de exibição das colunas
Usamos o comando `AS` para criar un **apelido (alias)**

```sql
SELECT
    nome AS produto,
    preco AS valor
FROM produtos;
```

## Filtrando registros com WHEREW
O `WHERE` permite determinar **quais registros deven aparecer** no resultado. Na prática, são condições para execução do `SELECT`.

```sql
SELECT * FROM produtos WHERE quantidade = 0;
```

### Comparação de maior 

```sql
SELECT nome, preco FROM produtos WHERE preco > 1000;
```

### Comparação de menor ou igual
```sql
SELECT nome, preco FROM produtos WHERE preco <= 100;
```

### Comparação de diferença
Normalmente se usa o operador `<>` em vez do `!=`;

```sql
SELECT * FROM produtos WHERE fornecedor_id <> 1;
```
```sql
SELECT nome, preco, quantidade FROM produtos
WHERE preco < 500 AND quantidade > 20;
```

### Operador OR (OU)
Exibir os produtos que custem mais de 3000 ou com quantidade zerada.

```sql
SELECT nome, preco, quantidade FROM produtos
WHERE preco > 3000 OR quantidade = 0;
```

### Operador NOT (nao)
Exibir os produtos que **não possuem preço acima de 1000**
```sql
SELECT nome, preco FROM produtos WHERE NOT preco > 1000;
```

**Obs.:** o uso do `NOT` não é obrigatório, desde que você consiga o mesmo resultado usando uma lógica diferente, como no exemplo:

`SELECT nome, preco FROM produtos WHERE preco <= 1000;`

### BETWEEN
Exibir produtos com preço **entre 100 e 500**
```sql
SELECT nome, preco FROM produtos
WHERE preco, BETWEEN 100 and 500;
```

### IN

exibir produtos que tenha o fornecedor ID 1, 4 ou 8;
```sql
SELECT * from produtos
where fornecedor_id in (1, 4, 8);
```

1. Where
2. GROUP BY/HAVING
3. ORDER BY 

---

## JOIN (juntar)

Até agora consultamos principalmente dados existentes em **uma única tabela**

Porém, nosso banco possui informações relacionadas **entre várias tabelas.**

Por exemplo:

- `produtos` possui `fornecedor_id`
- `fornecedores` possui o nome dos fornecedores

O `JOIN` permite **combinar informações de tabelas relacionadas** na consulta com `SELECT`. 

### INNER JOIN entre produtos e fornecedores

Exibir nome dos fornecedores de cada produto:

```sql
SELECT 
    -- tabela.coluna AS apelido
    -- especialmente para colunas com o mesmo nme
    produtos.nome AS produto, 
    produtos.preco, 
    fornecedores.nome AS fornecedor
FROM produtos

-- Fazendo a junção (JOIN) entre as tabelas
-- Neste casp, produtos com fornecedores
INNER JOIN forncedores

-- Definindo a condição de CRUZAMENTO entre as tabelas
    ON produtos.fornecedor_id = fornecedores.id;
```

### Apelidos (alias) para tabelas

Podemos usar apelidos para tornar consultas maiores mais compactas.

```sql
SELECT
    p.nome AS produtos
    p.preco,
    f.nome AS fornecedor

FROM produtos AS p
INNER JOIN fornecedores AS f
    ON p.fornecedor_id = f.id;
```
Neste exemplo :
    - `p` representa a tabela `produtos`;
    - `f` representa a tabela `fornecedores`;

**Dica:** versão ainda mais compacta omitindo o `AS`:

```sql
SELECT
    p.nome produto,
    p.preco,
    f.nome fornecedor

FROM produtos p
INNER JOIN fornecedores f
    ON p.fornecedor_id = f.id;
```

### JOIN com filtro

Exibir somente os produtos com preço superior a R$ 1000
mostrando também o nome de seus fornecedores

```sql
SELECT 
    produtos.nome AS produto,
    produtos.preco,
    fornecedores.nome AS fornecedor
FROM produtos INNER JOIN fornecedores 
    ON produtos.fornecedor_id = fornecedores.id
WHERE produtos.preco > 1000;
```

### Desafio: JOIN envolvendo 3 tabela

Objetivo: descobrir qual produto é vendido em qual loja e qual é seu estoque naquela loja.

```sql
    
```