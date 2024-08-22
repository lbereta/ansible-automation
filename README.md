# Docker Nginx Setup com Ansible

Este projeto configura um servidor web Nginx usando Docker e Docker Compose, automatizando o processo com Ansible. O servidor Nginx serve uma página HTML simples para testar a configuração.

## Requisitos

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## Instalação

1. **Instale o Docker**

   Siga as instruções para instalar o Docker em [Docker Desktop para macOS](https://docs.docker.com/desktop/install/mac-install/), [Docker para Windows](https://docs.docker.com/desktop/install/windows-install/), ou [Docker para Linux](https://docs.docker.com/engine/install/).

   Para macOS, você pode instalar o Docker Desktop usando o Homebrew:

    ```bash
    brew install --cask docker
    ```

2. **Instale o Ansible**
    Se o Ansible ainda não estiver instalado, você pode instalá-lo usando o Homebrew:

    ```bash
    brew install ansible
    ```

3. **Clone o Repositório**

   ```bash
   git clone https://github.com/lbereta/ansible-automation.git
   cd ansible-automation
   ```

4. **Configure e Inicie o Servidor**
    Utilize o Ansible para configurar e iniciar o servidor Nginx:

    ```bash
    ansible-playbook nginx-setup.yml
    ```

    Esse comando irá garantir que o Docker esteja instalado e em execução, e iniciará o Container Nginx configurado.

5. **Verifique a Configuração**
    Abra o navegador e acesse http://localhost:8080 para ver a página HTML servida pelo Nginx.

## Parar e Remover o Container

1. Para parar e remover o Container Nginx, você pode usar:

    ```bash
    docker compose down
    ```
