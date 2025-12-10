# 🕹️ Loja Games API – NestJS

API RESTful para gerenciar uma loja de games, incluindo cadastro de produtos, categorias e relacionamento entre ambos.
Projeto desenvolvido para a atividade prática do Bootcamp Generation Brasil – Módulo NestJS.

🚀 Tecnologias utilizadas

Node.js

NestJS

TypeORM

MySQL

Insomnia (testes)

🗂 Recursos da API
✔ Categoria

Criar categoria

Listar categorias

Buscar por ID

Buscar por nome

Atualizar categoria

Deletar categoria

✔ Produto

Criar produto

Listar produtos

Buscar por ID

Buscar por nome

Atualizar produto

Deletar produto

Relacionamento Many-to-One com Categoria

🔗 Relacionamento

Cada Produto pertence a uma Categoria
Cada Categoria pode ter vários Produtos

Modelo aplicado no TypeORM:

@OneToMany(() => Produto, produto => produto.categoria)
produtos: Produto[];

@ManyToOne(() => Categoria, categoria => categoria.produtos, { onDelete: 'CASCADE' })
categoria: Categoria;

🧪 Testes com Insomnia

Foram realizados testes de:

CRUD de Categorias

CRUD de Produtos

Validação de categoria inexistente

Retorno adequado de erros (404 e 400)

Verificação do relacionamento na resposta JSON

📦 Como executar o projeto

1. Instalar dependências
npm install

2. Configurar o arquivo .env
DB_HOST=localhost
DB_PORT=3306
DB_USERNAME=root
DB_PASSWORD=sua_senha
DB_DATABASE=loja_games

3. Rodar o projeto
npm run start:dev

✨ Feito por

Thatiana Mattos
Desenvolvedora Full Stack em formação
GitHub: <https://github.com/ThatianaMattos>

LinkedIn: <https://www.linkedin.com/in/thatiana-mattos/>
