---
summary: Comece criando e executando uma nova aplicação AdonisJS
---

AdonisJs é um framework Node.js e, portanto, requer o Node.js instalado no seu computador. Para ser mais preciso, exigimos `Node.js> = 14.15.4`, junto com `npm> = 6.0.0`.

Você pode checar a versão do Node.js e npm rodando os comandos a seguir:

```sh
# checar a versão do node.js
node -v

# checar a versão do npm
npm -v
```
Se você não tem o Node.js instalado, então você pode [baixar o binário](https://nodejs.org/en/download/) para seu sistema operacional a partir do website oficial.

Se você é confortável com a linha de comando, recomendamos usar [nvm](https://github.com/nvm-sh/nvm) ou [volta](https://volta.sh/) para instalar e rodar múltiplas versões do Node.js em seu computador.

## Criando um novo projeto

Você pode criar um novo projeto usando [npm init](https://docs.npmjs.com/cli/v7/commands/npm-init) ou [yarn create](https://classic.yarnpkg.com/en/docs/cli/create/). Ambas ferramentas baixarão o pacote inicial do AdonisJS e dá início ao processo de instalação

```sh
npm init adonis-ts-app@latest hello-world

# Usando yarn
yarn create adonis-ts-app hello-world
```
O processo de instalação solicita as seguintes escolhas.

#### Estrutura do projeto
Você pode escolher uma entre as seguintes estruturas de projeto:

- `web` é a estrutura de projeto ideal para criar as clássicas aplicações renderizadas no servidor. Configuramos o suporte à sessões e instalamos o AdonisJS template engine.
- `api` é a estrutura de projeto ideal para criar um servidor de API.
- `slim` á a estrutura de projeto que cria a menor aplicação AdonisJS possível e não instala nenhum pacote adicional, exceto o núcleo do framework.

---

#### Nome do projeto
O nome do projeto. Definimos o valor dessa solicitação dentro do arquivo `package.json`.

---

#### Configurar eslint/prettier
Opcionalmente, você pode configurar Eslint e prettier. Ambos pacotes são configurados com as definições utilizadas pelo time principal do AdonisJS

---

#### Configurar webpack encore
Opcionalmente, você pode configurar [webpack encore](./http/assets-manager.md) para empacotar e servir as dependências de frontend.

Note que o AdonisJS é um framework backend e não se preocupa com ferramentas de build de frontend. Portanto, a configuração do webpack é opcional

## Iniciar o servidor de desenvolvimento
Após criar a aplicação, você pode iniciar o servidor de desenvolvimento rodando o comando a seguir:

```sh
node ace serve --watch
```

- O comando `serve` inicia o servidor HTTP e realiza compilação em memória de TypeScript para JavaScript
- A flag `--watch` tem a finalidade de observar modificações no sistema de arquivos e reiniciar automaticamente.

## Compilando para produção
Você deve sempre implantar o JavaScript compilado no seu servidor de produção. Você pode criar o build de produção rodando o comando a seguir:

```sh
node ace build --production
```

A saída compilada é gravada na pasta `build`. Você pode fazer `cd` nesta pasta e iniciar o servidor executando o arquivo `serve.js` diretamente. Saiba mais sobre o [processo de build do TypeScript](./fundamentals/typescript-build-process.md)


```sh
cd build
node server.js
```
