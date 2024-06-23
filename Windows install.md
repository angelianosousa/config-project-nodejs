# Guia de Instalação para NVM, VS Code, Git e PostgreSQL no Windows

Este guia irá orientá-lo na instalação das ferramentas NVM (Node Version Manager), VS Code, Git e PostgreSQL no sistema operacional Windows.

## 1. Instalar NVM para Windows

O NVM permite que você gerencie várias versões do Node.js no seu sistema.

1. **Baixe o instalador do NVM para Windows**:
    - Acesse [nvm-windows releases](https://github.com/coreybutler/nvm-windows/releases).
    - Baixe o arquivo `nvm-setup.zip` e extraia o conteúdo.

2. **Execute o instalador**:
    - Execute o arquivo `nvm-setup.exe` e siga as instruções do instalador.

3. **Instale uma versão do Node.js**:
    - Abra o Prompt de Comando como Administrador.
    - Execute o comando para instalar a versão mais recente do Node.js:

      ```bash
      nvm install latest
      ```

    - Defina a versão instalada como a versão padrão:

      ```bash
      nvm use latest
      ```

4. **Verifique a instalação**:

    - Verifique a versão do Node.js e do npm:

      ```bash
        node -v
        npm -v
      ```

## 2. Instalar Visual Studio Code (VS Code)

O Visual Studio Code é um editor de código-fonte desenvolvido pela Microsoft para Windows, Linux e macOS.

1. **Baixe o instalador do VS Code**:
    - Acesse [VS Code Download](https://code.visualstudio.com/download).
    - Baixe o instalador apropriado para o Windows.

2. **Execute o instalador**:
    - Execute o arquivo baixado e siga as instruções do instalador.

3. **Verifique a instalação**:

    - Abra o Prompt de Comando e verifique a versão do VS Code:

      ```bash
        code --version
      ```

## 3. Instalar Git

Git é um sistema de controle de versão distribuído.

1. **Baixe o instalador do Git**:
    - Acesse [Git for Windows](https://gitforwindows.org/).
    - Baixe o instalador.

2. **Execute o instalador**:
    - Execute o arquivo baixado e siga as instruções do instalador.

3. **Verifique a instalação**:

    - Abra o Git Bash ou o Prompt de Comando e verifique a versão do Git:

      ```bash
      git --version
      ```

4. **Configure seu nome de usuário e email**:

    - No Git Bash ou Prompt de Comando, execute os seguintes comandos:

      ```bash
        git config --global user.name "Seu Nome"
        git config --global user.email "seuemail@exemplo.com"
      ```

## 4. Instalar PostgreSQL

PostgreSQL é um sistema de gerenciamento de banco de dados relacional avançado e de código aberto.

1. **Baixe o instalador do PostgreSQL**:
    - Acesse [PostgreSQL Downloads](https://www.postgresql.org/download/windows/).
    - Baixe o instalador.

2. **Execute o instalador**:
    - Execute o arquivo baixado e siga as instruções do instalador.
    - Durante a instalação, você pode ser solicitado a configurar uma senha para o usuário `postgres`.

3. **Verifique a instalação**:
    - Abra o Prompt de Comando e verifique a versão do PostgreSQL:

      ```bash
      psql --version
      ```

4. **Acesse o PostgreSQL**:
    - Abra o Prompt de Comando ou o aplicativo pgAdmin.
    - Conecte-se ao servidor PostgreSQL usando as credenciais configuradas durante a instalação.

5. **Crie um banco de dados e um usuário** (opcional):

    - No pgAdmin ou no Prompt de Comando (usando `psql`), execute os seguintes comandos:

      ```sql
      CREATE DATABASE mydatabase;
      CREATE USER myuser WITH ENCRYPTED PASSWORD 'mypassword';
      GRANT ALL PRIVILEGES ON DATABASE mydatabase TO myuser;
      ```

## Conclusão

Com estes passos, você instalou com sucesso o NVM, VS Code, Git e PostgreSQL no seu sistema operacional Windows. Agora você está pronto para começar a desenvolver suas aplicações com essas ferramentas poderosas.
