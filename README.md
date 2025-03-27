# Sistema de Gerenciamento de Usuários

Este projeto é uma aplicação PHP para gerenciamento de usuários, com funcionalidades de **CRUD (Criar, Ler, Atualizar, Deletar)** e **confirmação de senha** para exclusão de usuários, garantindo segurança no processo de exclusão de registros.

## Funcionalidades

- **Cadastro de usuários:** Permite o cadastro de usuários, com nome, e-mail e data de nascimento.
- **Listagem de usuários:** Exibe todos os usuários cadastrados, com a possibilidade de visualizar, editar ou excluir.
- **Edição de dados do usuário:** Permite a atualização das informações do usuário, como nome, e-mail e data de nascimento.
- **Exclusão de usuário:** Requer a confirmação da senha do usuário para garantir a segurança antes de proceder com a exclusão.

## Tecnologias Utilizadas

- **PHP 7.4+**: A lógica de backend e as operações com o banco de dados são feitas em PHP.
- **MySQL**: O banco de dados utilizado para armazenar os dados dos usuários.
- **Bootstrap 5**: Framework CSS utilizado para estilização da interface.
- **HTML5 e CSS3**: Linguagens usadas para estruturar e estilizar o frontend.

## Requisitos

- **PHP 7.4 ou superior**
- **Servidor Apache ou Nginx** (recomendado)
- **Banco de Dados MySQL** (ou MariaDB)
- **Git** (para controle de versão e deploy no GitHub)

## Estrutura do Projeto

- `db_connect.php`: Arquivo responsável pela conexão com o banco de dados MySQL.
- `index.php`: Página principal que lista os usuários cadastrados.
- `visualizar.php`: Exibe os detalhes de um usuário específico.
- `editar.php`: Página para edição dos dados de um usuário.
- `excluir.php`: Página onde a exclusão do usuário é realizada, exigindo a confirmação da senha.
- `style.css`: Arquivo de estilos customizados (opcional, se desejar adicionar mais estilização).

## Funcionalidade de Exclusão com Confirmação de Senha

Uma das características chave deste sistema é a **exclusão de usuários com confirmação de senha**. Quando um usuário deseja excluir sua conta, é solicitado que ele insira sua senha atual para confirmar a ação. Isso garante maior segurança, prevenindo exclusões acidentais ou não autorizadas.

### Fluxo de Exclusão:
1. O usuário clica no botão de exclusão na página de listagem de usuários.
2. É exibido um formulário onde o usuário deve inserir sua senha.
3. O sistema compara a senha informada com a senha armazenada no banco de dados.
4. Se a senha for válida, o sistema exclui o usuário e exibe uma mensagem de sucesso.
5. Caso contrário, o sistema exibe uma mensagem de erro informando que a senha está incorreta.
