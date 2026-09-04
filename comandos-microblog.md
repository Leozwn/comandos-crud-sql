```sql  
-- Usuarios

-- editor
INSERT INTO usuarios (nome, email, senha, tipo)
VALUES ('Leozera', 'Leozwn@email.com', '123abc', 'editor');

-- administrador
INSERT INTO usuarios (nome, email, senha, tipo)
VALUES ('Cristinao Ronaldo', 'Cr7@email.com', 'abc456', 'admin');

-- editor
INSERT INTO usuarios (nome, email, senha, tipo)
VALUES ('Harry Kane', 'HarryK@email.com', '789xyz', 'editor');

-- categorias
INSERT INTO categorias (nome) VALUES
('Tecnologia'),
('Educação'),
('Entretenimento');

--noticias

-- Notícia 1: Tecnologia, responsável Leozera 
INSERT INTO noticias (titulo, resumo, texto, imagem, destaque, usuario_id, categoria_id)
VALUES (
    'IA revoluciona o mercado de trabalho',
    'Ferramentas de inteligência artificial estão transformando diversas profissões.',
    'Nos últimos anos, a inteligência artificial deixou de ser ficção científica e passou a integrar o dia a dia de empresas de todos os portes. Setores como saúde, direito e educação já sentem os impactos dessa transformação.',
    'ia-mercado.jpg',
    1,          -- destaque: sim
    1,          -- Leozera
    1           -- categoria: Tecnologia
);
-- noticia 2:
-- noticia 3:
-- noticia 4:
```