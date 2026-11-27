# Mundo SENAI 2026 — Esteira RFID

Aplicação web para monitoramento de uma esteira de produtos com RFID,
desenvolvida como projeto integrador do curso técnico do SENAI Videira.

[![PHP](https://img.shields.io/badge/Backend-PHP-777BB4?logo=php&logoColor=white)](https://www.php.net/)
[![HTML5](https://img.shields.io/badge/Frontend-HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/Frontend-CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/Frontend-JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)
[![MySQL](https://img.shields.io/badge/Database-MySQL-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Docker](https://img.shields.io/badge/Ambiente-Docker-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![Licença](https://img.shields.io/badge/Licen%C3%A7a-MIT-green)](./LICENSE)

## Sumário

- [Sobre o projeto](#sobre-o-projeto)
- [Demonstração](#demonstração)
- [Funcionalidades](#funcionalidades)
- [Tecnologias](#tecnologias)
- [Arquitetura](#arquitetura)
- [Como executar](#como-executar)
- [Equipe](#equipe)
- [Roadmap](#roadmap)
- [Licença](#licença)

## Sobre o projeto

O projeto simula uma esteira de distribuição de produtos de uma empresa,
destinando caixas para diferentes regiões do Brasil. Cada caixa é identificada
por uma TAG RFID lida por sensores na esteira.

A versão final inclui a parte física: esteira, sensores RFID e braços robóticos.

## Demonstração

![Tela de login](./docs/img/login.png)
![Dashboard](./docs/img/dashboard.png)

## Funcionalidades

- Autenticação de usuário com controle de acesso.
- Conexão e persistência em banco MySQL.
- Exibição das TAGs RFID registradas.
- CRUD de TAGs e de caixas.
- Dashboard com indicadores da esteira.
- Integração com o hardware (sensores e braços robóticos).

## Tecnologias

| Camada | Tecnologia |
| --- | --- |
| Backend | PHP |
| Frontend | HTML5, CSS3, JavaScript |
| Banco de dados | MySQL |
| Dependências | Composer |
| Ambiente | Docker, Linux, Apache |
| Versionamento | Git e GitHub |

## Arquitetura

O projeto adapta o padrão MVC para **MVCS**, separando Models, Views,
Controllers e Services.

    .
    ├── App/
    │   ├── Controllers/
    │   ├── Core/
    │   ├── Models/
    │   ├── Routes/
    │   ├── Services/
    │   └── Views/
    ├── Public/
    │   └── Assets/
    ├── docs/
    │   └── img/
    ├── vendor/
    └── docker-compose.yml

## Como executar

**Pré-requisitos:** Docker e Docker Compose (ou PHP 8+, Composer, MySQL e Apache).

1. Clone o repositório:

        git clone https://github.com/senaivideira-apps/2026-2-mundo-senai-esteira-rfid.git
        cd 2026-2-mundo-senai-esteira-rfid

2. Instale as dependências:

        composer install

3. Crie o arquivo de configuração a partir do modelo:

        cp App/Core/env.example.php App/Core/env.php

4. Preencha as credenciais em `App/Core/env.php` (esse arquivo não é versionado):

        <?php

        return [
            "host" => "seu-host",
            "port" => "sua-porta",
            "db" => "sua-db",
            "user" => "seu-user",
            "password" => "sua-senha",
        ];

5. Suba o ambiente:

        docker compose up -d

6. Acesse em `http://localhost:8080`.

## Equipe

| Nome | Função |
| --- | --- |
| Nome do aluno | Desenvolvimento backend |
| Nome do aluno | Frontend e banco de dados |
| Prof. Seu Nome | Orientação |

## Roadmap

- [x] Conexão com banco de dados
- [x] Autenticação de usuário
- [x] Exibição e CRUD de TAGs
- [x] Painel de usuários e dashboard
- [x] CRUD de caixas
- [x] Integração com hardware

## Licença

Distribuído sob a licença MIT. Veja [LICENSE](./LICENSE).

Projeto desenvolvido para fins educacionais no SENAI Videira.
