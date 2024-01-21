# Cadastro Falso com Angular

## Etapas Do Projeto

- Configuração geral

> Sistema operacional
```bash
codespace@codespaces-20d430 
--------------------------- 
OS: Ubuntu 20.04.6 LTS x86_64 
Host: Virtual Machine 7.0 
Kernel: 6.2.0-1018-azure 
Uptime: 30 mins 
Packages: 650 (dpkg) 
Shell: bash 5.0.17 
Terminal: vscode 
CPU: AMD EPYC 7763 (2) @ 3.243GHz
Memory: 2287MiB / 7929MiB 
```

> Criação de diretorios

```bash
$ mkdir server && cd server
```

>> Instalação *json-server* com npm

```bash
$ npm i json-server
```

>>> Criação do arquivo db com json

```json
{
    "cadastros":[
        {
            "id": 1,
            "caracteristica":"material",
            "tipo": 1
        },
        {
            "id": 2,
            "caracteristica":"objeto",
            "tipo": 2
        }
    ]
}
```

>>>> Configurar o arquivo package e inicializar o arquivo json

```bash
$ npm run start
```

> Instalação do Framework [Angular](https://angular.io/cli)

```bash
$ 
``` 

>> Versão do Angular

```bash
Angular CLI: 17.1.0
Node: 20.11.0
Package Manager: npm 10.2.4
OS: linux x64
```

> Inicialização do aplicativo

```bash
$ npm init
```

- Escolha padrão para inicialização do aplicativo.
- Instalação de dependências
  - bun add elysia @elysiajs/cookie prisma @prisma/client dotenv pg jsonwebtoken@8.5.1
- Instalação correspondentes
  - bun add -d @types/jsonwebtoken
- As dependências que foram instaladas:
  - Elysia: Elysia é uma estrutura web para Bun que simplifica o trabalho com Bun, semelhante ao que Express faz para Node.js.
  - Prisma: Prisma é um mapeador objeto-relacional (ORM) para JavaScript e TypeScript.
  - Dotenv: Dotenv é um pacote NPM que carrega variáveis ​​ambientais de um arquivo .env em process.env.
  - PG: PG é o driver nativo do PostgreSQL.
  - jsonwebtoken@8.5.1: Um pacote que implementa o padrão JWT (versão 8.5.1).
- Configurando o banco de dados
  - bunx prisma init --datasource-provider postgresql
- Criando modelos Prisma
  - Migração das model com prisma
    - bunx prisma migrate dev --name init
- Criação de serviços e controladores
  - mkdir controllers && mkdir services
- Implementando Lógica dos Serviços
- Implementando Lógica das Controllers
- Configurando seu servidor Bun-Elysia
- comando para iniciar app.
  - bun --watch index.ts