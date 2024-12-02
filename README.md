# Sistema de Autenticação - ETAPA 4

## Sobre o Projeto

Este projeto tem como objetivo criar um sistema de autenticação simples utilizando **Java** e conexão com o banco de dados **MySQL**. Ele inclui funcionalidades para verificar credenciais de usuários, implementadas na classe `User`.

## Estrutura do Código

### Classe: `User`

- **Objetivo:** Gerenciar a conexão com o banco de dados e a verificação de login de usuários.
- **Métodos:**
- `conectarBD()`: Estabelece conexão com o banco de dados.
- `verificarUsuario(String login, String senha)`: Verifica se as credenciais fornecidas são válidas.

## Configuração do Ambiente

1. Instale o MySQL e configure a tabela `usuarios` no banco de dados `test`:
   ```sql
   CREATE TABLE usuarios (
       id INT AUTO_INCREMENT PRIMARY KEY,
       login VARCHAR(50) NOT NULL,
       senha VARCHAR(50) NOT NULL,
       nome VARCHAR(100) NOT NULL
   );

   INSERT INTO usuarios (login, senha, nome) VALUES ('admin', 'admin123', 'Administrador');
