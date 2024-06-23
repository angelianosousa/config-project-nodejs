# Guia de Instalação para NVM, VS Code, Git e PostgreSQL no Linux

Este guia irá orientá-lo na instalação das ferramentas NVM (Node Version Manager), VS Code, Git e PostgreSQL no sistema operacional Linux.

## 1. Instalar NVM

O NVM permite que você gerencie várias versões do Node.js no seu sistema.

1. **Baixe e instale o script NVM**:

    ```bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
    ```

2. **Carregue o NVM** no seu shell atual:

    ```bash
    export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
    ```

3. **Verifique a instalação** do NVM:

    ```bash
    command -v nvm
    ```

4. **Instale a versão mais recente do Node.js**:

    ```bash
    nvm install node
    ```

5. **Verifique a instalação do Node.js**:

    ```bash
    node -v
    npm -v
    ```

## 2. Instalar Visual Studio Code (VS Code)

O Visual Studio Code é um editor de código-fonte desenvolvido pela Microsoft para Windows, Linux e macOS.

1. **Baixe o pacote .deb** do VS Code:

    ```bash
    wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
    sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/
    sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
    rm -f packages.microsoft.gpg
    ```

2. **Atualize os pacotes e instale o VS Code**:

    ```bash
    sudo apt update
    sudo apt install code
    ```

3. **Verifique a instalação**:

    ```bash
    code --version
    ```

## 3. Instalar Git

Git é um sistema de controle de versão distribuído.

### Passo a Passo

1. **Atualize os pacotes e instale o Git**:

    ```bash
    sudo apt update
    sudo apt install git
    ```

2. **Verifique a instalação**:

    ```bash
    git --version
    ```

3. **Configure seu nome de usuário e email**:

    ```bash
    git config --global user.name "Seu Nome"
    git config --global user.email "seuemail@exemplo.com"
    ```

## 4. Instalar PostgreSQL

PostgreSQL é um sistema de gerenciamento de banco de dados relacional avançado e de código aberto.

1. **Atualize os pacotes e instale o PostgreSQL**:

    ```bash
    sudo apt update
    sudo apt install postgresql postgresql-contrib
    ```

2. **Verifique o status do serviço PostgreSQL**:

    ```bash
    sudo systemctl status postgresql
    ```

3. **Acesse o PostgreSQL**:

    ```bash
    sudo -i -u postgres
    psql
    ```

4. **Crie um banco de dados e um usuário** (opcional):

    ```sql
    CREATE DATABASE mydatabase;
    CREATE USER myuser WITH ENCRYPTED PASSWORD 'mypassword';
    GRANT ALL PRIVILEGES ON DATABASE mydatabase TO myuser;
    ```

5. **Saia do PostgreSQL**:

    ```sql
    \q
    exit
    ```

## Conclusão

Com estes passos, você instalou com sucesso o NVM, VS Code, Git e PostgreSQL no seu sistema operacional Linux. Agora você está pronto para começar a desenvolver suas aplicações com essas ferramentas poderosas.
