# S.O. 2024.2 - Projeto exemplo de Python+Postgres+Docker

## Informações gerais

- **Objetivo do repositório**: Repositório com os códigos e configurações de um projeto Django com serviços usando docker
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- disciplina: **SO** Sistemas Operacionais
- professor: [Leonardo A. Minora](https://github.com/leonardo-minora)

## Sequência de passos

1. Criar o projeto `projeto`
2. No projeto,
   1. Executar a migração `makemigrations` e `migrate`
   2. Executar o projeto com `runserver`
3. Criar a aplicação `cursos`
4. Na aplicação `cursos`
   1. Criar a função `index` para exibir a lista de cursos usando inicialmente `HttpResponse`
   2. Criar o arquivo `urls.py`
   3. Registrar a rota _root_ em urls para `view.index`
5. No projeto, 
   1. Modificar `projeto/urls.py` adicionar rota para aplicação `cursos`
   2. Testar a rota `http://localhost:8000/cursos`
6. Na aplicação `cursos`
   1. Criar o modelo `Curso`
   2. Executar a migração novamente `makemigrations cursos` e `migrate`
   3. Criar o template `templates/cursos/index.html`
   4. Modificar a função `index` de `HttpResponse` para `render`
   5. Criar e carregar o _seed_ para cursos
   6. Criar a função `curso_detalhar` com `HttpResponse`
   7. Registrar rota `<pk>` para detalhar dados do curso
7. No projeto,
   1. Testar novamente a rota `http://localhost:8000/cursos`
8. Mudar a configuração para postgres
   1. Parar o `runserver`
   2. Configurar o `settings.py` para o postgres
   3. Criar um `Dockerfile` para o Postgres
   4. Criar um `docker-compose.yml`
   5. Executar o serviço do postgres no docker
   6. Criar superusuário do banco de dados
   7. Executar o migrate
   8. Carregar os dados do _seed_
   9. Executar o `runserver` novamente
   10. Testar a rota `http://localhost:8000/cursos`
