# 📅 Agenda PHP com PDO e Bootstrap

Bem-vindo ao projeto de uma agenda simples desenvolvida em PHP usando PDO para manipulação de banco de dados e estilizada com Bootstrap. A aplicação permite gerenciar contatos com facilidade.

## 🚀 Funcionalidades

- **Adicionar Contatos**: Insira novos contatos na agenda.
- **Editar Contatos**: Atualize informações dos contatos existentes.
- **Excluir Contatos**: Remova contatos da agenda.
- **Visualizar Contatos**: Veja todos os contatos listados.

## 🛠️ Tecnologias Utilizadas

- **PHP**: Linguagem de programação server-side para desenvolvimento web.
- **PDO (PHP Data Objects)**: API de acesso a banco de dados para operações seguras e eficientes.
- **Bootstrap**: Framework front-end para estilização e design responsivo.
- **MySQL**: Sistema de gerenciamento de banco de dados relacional.

## 📝 Licença
Este projeto está licenciado sob a Licença MIT. Veja o arquivo LICENSE para mais detalhes.

## 📫 Contato
Se você tiver alguma dúvida ou sugestão, sinta-se à vontade para abrir uma issue ou entrar em contato através dos canais fornecidos.


## 🖥️ Como Criar um Servidor Local

Para rodar a aplicação localmente, você precisará configurar um servidor web e um banco de dados no seu computador. Siga os passos abaixo para configurar um servidor local utilizando XAMPP, WAMP, ou MAMP. Essas ferramentas fornecem uma maneira fácil de configurar um ambiente de desenvolvimento PHP com MySQL.

### 1. Instalar um Ambiente de Desenvolvimento Local

Escolha uma das seguintes ferramentas e siga as instruções para instalação:

- **[XAMPP](https://www.apachefriends.org/index.html)** (Windows, macOS, Linux)
  - **Download**: Baixe e instale o XAMPP para seu sistema operacional.
  - **Iniciar**: Após a instalação, abra o painel de controle do XAMPP e inicie os módulos **Apache** e **MySQL**.

- **[WAMP](http://www.wampserver.com/en/)** (Windows)
  - **Download**: Baixe e instale o WAMP.
  - **Iniciar**: Após a instalação, inicie o WAMP e verifique se os ícones do Apache e MySQL estão verdes.

- **[MAMP](https://www.mamp.info/en/)** (macOS, Windows)
  - **Download**: Baixe e instale o MAMP.
  - **Iniciar**: Após a instalação, abra o MAMP e inicie os servidores Apache e MySQL.

### 2. Configurar o Banco de Dados

1. **Acessar o phpMyAdmin**:
   - Abra o navegador e vá para `localhost/phpmyadmin`.

2. **Criar um Novo Banco de Dados**:
   - No phpMyAdmin, clique em **"Databases"**.
   - Crie um novo banco de dados e nomeie-o, por exemplo, `agenda_db`.

3. **Importar Estrutura do Banco de Dados**:
   - Se você tiver um arquivo SQL para a estrutura do banco de dados, clique na aba **"Import"** e carregue o arquivo `database.sql` (ou equivalente) para criar as tabelas necessárias.

### 3. Configurar a Conexão com o Banco de Dados

1. **Editar Configurações do Banco de Dados**:
   - Navegue até o arquivo `config/database.php` no diretório do projeto.
   - Configure as variáveis com suas credenciais do banco de dados. Por exemplo:

     ```php
     <?php
     $host = 'localhost';
     $db = 'agenda_db';
     $user = 'root';
     $pass = '';

     try {
         $pdo = new PDO("mysql:host=$host;dbname=$db", $user, $pass);
         $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
     } catch (PDOException $e) {
         echo 'Connection failed: ' . $e->getMessage();
     }
     ?>
     ```

   - Ajuste `$host`, `$db`, `$user`, e `$pass` conforme necessário para sua configuração.

### 4. Colocar os Arquivos do Projeto no Servidor

1. **Mover os Arquivos**:
   - Copie a pasta do projeto `agenda-php-pdo-bootstrap` para o diretório de documentos do seu servidor local:
     - **XAMPP**: `C:\xampp\htdocs\`
     - **WAMP**: `C:\wamp\www\`
     - **MAMP**: `/Applications/MAMP/htdocs/`

2. **Acessar a Aplicação**:
   - Abra o navegador e vá para `http://localhost/agenda-php-pdo-bootstrap/` para acessar a aplicação.

### 5. Testar a Aplicação

- **Acessar**: Navegue até as diferentes páginas da aplicação para garantir que tudo esteja funcionando corretamente.
- **Adicionar, Editar e Excluir Contatos**: Teste as funcionalidades de adicionar, editar e excluir contatos para garantir que o sistema está funcionando conforme esperado.

---

Com esses passos, você terá um servidor local configurado e pronto para rodar a aplicação. Se você encontrar problemas, verifique os logs de erro do servidor e ajuste as configurações conforme necessário.

