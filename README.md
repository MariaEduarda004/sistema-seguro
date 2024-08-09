# **Projeto Laravel: Implementação de Recursos Básicos de Segurança**

## **Descrição do Projeto**

Este projeto é um sistema web desenvolvido em Laravel que implementa recursos básicos de segurança, incluindo hashing de senhas, controle de sessões, e uma funcionalidade para recuperação de senha. O objetivo é demonstrar como aplicar boas práticas de segurança em uma aplicação web utilizando as ferramentas e funcionalidades nativas do Laravel.

## **Funcionalidades**

- **Cadastro de Usuário com Senha Hasheada**: As senhas dos usuários são armazenadas de forma segura no banco de dados utilizando um algoritmo de hashing.
- **Autenticação e Controle de Sessões**: Após o login, o sistema valida o acesso do usuário às áreas protegidas utilizando controle de sessões.
- **Recuperação de Senha**:
  - O sistema envia um e-mail com um link para redefinição de senha, que expira após 60 minutos.
  - Medidas de segurança são aplicadas para prevenir ataques de força bruta durante o processo de redefinição de senha.

## **Requisitos**

- PHP >= 8.1
- Composer
- Laravel 10.x
- MySQL
- Node.js & npm
- [Mailtrap](https://mailtrap.io) para testes de envio de e-mail (opcional, mas recomendado)
  
## **Instalação**

1. **Clone o Repositório**

   ```bash
   git clone https://github.com/MariaEduarda004/sistema-seguro.git
   cd sistema-seguro
2. **Instale as Dependências PHP**

   ```bash
   composer install
3. **Instale as Dependências JavaScript**

   ```bash
   npm install
4. **Crie o arquivo .env a partir do exemplo:**
    ```bash
   cp .env.example .env
5. **Gere uma chave para a aplicação**
   ```bash
   php artisan key:generate
6. **Configure o Banco de Dados**
   ```bash
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=seguranca_informacao
    DB_USERNAME=root
    DB_PASSWORD=
7. **Excecute as migrações**
   ```bash
    php artisan migrate
8. **Configuração de E-mail (utilizei os recursos fornecidos pela Mailtrap devido a seguranças no meu e-mail pessoal)**
   ```bash
    MAIL_MAILER=smtp
    MAIL_HOST=sandbox.smtp.mailtrap.io
    MAIL_PORT=2525
    MAIL_USERNAME=edac292d6780ef
    MAIL_PASSWORD=664269e54453eb
    MAIL_ENCRYPTION=tls
    MAIL_FROM_ADDRESS="emailTeste@gmail.com"
    MAIL_FROM_NAME="${APP_NAME}"
9. **Compilação**
   ```bash
    npm run 
    
   ```bash
    php artisan serve

    
Acesse o projeto em http://localhost:8000/login.

