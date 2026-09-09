```sql  
-- Usuarios

-- Ana Silva, editora
INSERT INTO usuarios (nome, email, senha, tipo)
VALUES ('Ana Silva', 'ana@email.com', '123abc', 'editor');

-- Bruno Souza, administrador
INSERT INTO usuarios (nome, email, senha, tipo)
VALUES ('Bruno Souza', 'bruno@email.com', 'abc456', 'admin');

-- Carla Mendes, editora
INSERT INTO usuarios (nome, email, senha, tipo)
VALUES ('Carla Mendes', 'carla@email.com', '789xyz', 'editor');

-- categorias
INSERT INTO categorias (nome) VALUES
('Tecnologia'),
('Educação'),
('Entretenimento');

--noticias

-- Notícia 1: Tecnologia, responsável Ana Silva (id 1), destaque
INSERT INTO noticias (titulo, resumo, texto, imagem, destaque, usuario_id, categoria_id)
VALUES (
    'IA revoluciona o mercado de trabalho',
    'Ferramentas de inteligência artificial estão transformando diversas profissões.',
    'Nos últimos anos, a inteligência artificial deixou de ser ficção científica e passou a integrar o dia a dia de empresas de todos os portes. Setores como saúde, direito e educação já sentem os impactos dessa transformação.',
    'ia-mercado.jpg',
    1,          -- destaque: sim
    1,          -- Ana Silva
    1           -- categoria: Tecnologia
);

-- Notícia 2: Educação, responsável Bruno Souza (id 2), sem destaque
INSERT INTO noticias (titulo, resumo, texto, imagem, destaque, usuario_id, categoria_id)
VALUES (
    'SENAC abre novas vagas para cursos técnicos em 2026',
    'Instituição amplia oferta de cursos na área de tecnologia e saúde.',
    'O SENAC São Paulo anunciou a abertura de centenas de vagas para cursos técnicos gratuitos e subsidiados. Entre as novidades estão os cursos de Informática para Internet, Enfermagem e Design Gráfico.',
    'senac-vagas.jpg',
    0,          -- destaque: não
    2,          -- Bruno Souza
    2           -- categoria: Educação
);

-- Notícia 3: Entretenimento, responsável Carla Mendes (id 3), destaque
INSERT INTO noticias (titulo, resumo, texto, imagem, destaque, usuario_id, categoria_id)
VALUES (
    'Festival de Cinema de SP anuncia programação 2026',
    'Evento traz produções inéditas de mais de 40 países para as telas paulistanas.',
    'O Festival Internacional de Cinema de São Paulo divulgou sua grade oficial. Serão exibidos mais de 200 filmes ao longo de duas semanas, com sessões gratuitas e debates com diretores.',
    'festival-cinema.jpg',
    1,          -- destaque: sim
    3,          -- Carla Mendes
    3           -- categoria: Entretenimento
);

-- Notícia 4: Tecnologia, responsável Ana Silva (id 1), sem destaque
INSERT INTO noticias (titulo, resumo, texto, imagem, destaque, usuario_id, categoria_id)
VALUES (
    'Brasil avança no ranking global de cibersegurança',
    'País sobe posições após investimentos em infraestrutura e capacitação profissional.',
    'Relatório divulgado pela União Internacional de Telecomunicações (UIT) mostra que o Brasil avançou 15 posições no índice global de cibersegurança. O resultado reflete os investimentos públicos e privados na área nos últimos dois anos.',
    'ciberseguranca-brasil.jpg',
    0,          -- destaque: não
    1,          -- Ana Silva
    1           -- categoria: Tecnologia
);
```