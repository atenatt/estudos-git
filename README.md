## Guia de Configuração e Uso do Git

Este documento serve como um guia rápido para configurar e utilizar o Git em seus projetos.

## Configuração do Git

### Configurar o Git

Para configurar seu nome de usuário e email globalmente:

```bash
git config --global user.name "Victor Pedro"
git config --global user.email "victor.boas@fatec.sp.gov.br"
```

### Verificar as Configurações Globais

Para verificar as configurações globais atuais:

```bash
git config --global list
```

## Inicialização do Repositório

### Inicializar o Git

Para inicializar um repositório Git no diretório atual:

```bash
git init
```

### Clonar um Repositório

Para clonar um repositório existente:

```bash
git clone https://github.com/user/arquivo.git
```

## Adicionar Arquivos ao Stage

### Adicionar todos os arquivos do diretório corrente

Para adicionar todos os arquivos não ignorados no diretório atual e em seus subdiretórios ao staging area:

```bash
git add .
```

### Adicionar um arquivo específico

Para adicionar um único arquivo ao staging area:

```bash
git add arquivo.txt
```

### Adicionar todos os arquivos com uma extensão específica

Para adicionar todos os arquivos com a extensão `.html` no diretório atual e em seus subdiretórios ao staging area:

```bash
git add *.html
```

## Verificar o Status dos Arquivos

Para verificar o status dos arquivos no diretório de trabalho, incluindo quais arquivos estão modificados, novos ou marcados para remoção, utilize o comando:

```bash
git status
```

## Remover um Arquivo do Staging Area

Para remover um arquivo do staging area antes de commitá-lo, utilize o comando:

```bash
git reset arquivo.txt
```

## Restaurar um Arquivo

Para restaurar um arquivo para a última versão commitada, utilize o comando:

```bash
git restore arquivo.txt
```

## Verificar as Diferenças entre os Arquivos

Para visualizar as diferenças entre o arquivo no staging area e o arquivo no disco de trabalho, utilize o comando:

```bash
git diff
```

Para visualizar as diferenças de um arquivo específico, utilize:

```bash
git diff arquivo.txt
```

## Confirmar uma Alteração

### Criar um Commit

Para criar um commit e registrar as alterações no staging area no repositório local, utilize o comando:

```bash
git commit -m "Mensagem do commit"
```

Opcionalmente, você pode incluir uma mensagem mais descritiva para o commit:

```bash
git commit -m "Descrição detalhada das alterações realizadas"
```

### Adicionar um Arquivo e Commitar Juntos

Para adicionar um novo arquivo ao staging area e commitá-lo junto com as alterações existentes, utilize o comando:

```bash
git add arquivo.txt
git commit -m "Mensagem do commit"
```

### Modificar a Mensagem do Último Commit

Para modificar a mensagem do último commit, utilize o comando:

```bash
git commit --amend -m "Nova mensagem do commit"
```

## Verificar as Diferenças entre o Último Commit e o Código Atual

Para visualizar as diferenças entre o último commit e o código atual no staging area, utilize o comando:

```bash
git diff --staged
```

## Visualizar os Logs dos Commits

### Visualizar Todos os Logs

Para visualizar o histórico de todos os commits no repositório, utilize o comando:

```bash
git log
```

### Visualizar os Últimos 3 Logs

Para visualizar os 3 últimos commits no repositório, utilize o comando:

```bash
git log -3
```

### Visualizar Todos os Logs em Uma Linha

Para visualizar todos os commits em uma única linha, utilize o comando:

```bash
git log --oneline
```

### Visualizar Logs com Organização das Branches

Para visualizar os commits com organização das branches, utilize o comando:

```bash
git log --oneline -graph
```

### Filtrar Logs por Autor

Para visualizar apenas os commits de um autor específico, utilize o comando:

```bash
git log --author="Victor Pedro"
```

Substitua `"Victor Pedro"` pelo nome do autor desejado.

### Filtrar Logs por Data

Para visualizar os commits que foram feitos em uma data específica ou em um intervalo de datas, utilize o comando:

```bash
git log --since="2023-12-31" --until="2024-01-01"
```

Substitua as datas entre aspas pelas datas desejada

# Mostrar a branch
    git branch
# Criar uma branch
    git branch nome-da-branch
# Excluir branch
    git branch -D nome-da-branch
# Criar uma branch e ir para ela
    git checkout -b nome-da-branch

# Ver o log de uma branch
    git log main

# Ver a diferença de duas branchs
    git diff main nome-da-branch

## Gerenciando Branches no Git

Este guia apresenta os comandos básicos para gerenciar branches no Git, permitindo que você trabalhe em diferentes versões do seu projeto de forma organizada e eficiente.

### Visualizar as Branches Existentes

Para listar todas as branches, tanto locais quanto remotas, no seu repositório, utilize o comando:

```bash
git branch
```

### Criar uma Nova Branch

Para criar uma nova branch a partir da branch atual e posicionar-se nela, utilize o comando:

```bash
git checkout -b nome-da-branch
```

Substitua `nome-da-branch` pelo nome desejado para a sua nova branch.

### Excluir uma Branch

Para excluir uma branch local, utilize o comando:

```bash
git branch -D nome-da-branch
```

**Observação:** Este comando exclui a branch permanentemente. Utilize-o com cautela!

### Verificar o Log de uma Branch

Para visualizar o histórico de commits de uma branch específica, utilize o comando:

```bash
git log nome-da-branch
```

Substitua `nome-da-branch` pelo nome da branch que deseja consultar o log.

### Comparar Diferenças entre Branches

Para comparar as diferenças entre duas branches, utilize o comando:

```bash
git diff branch-base nome-da-branch
```

Substitua `branch-base` pela branch que você deseja usar como referência e `nome-da-branch` pela branch que deseja comparar.

### Exemplos Práticos

* **Criar uma branch para corrigir um bug:**

```bash
git checkout -b corrigir-bug
```

* **Comparar as diferenças entre a branch `master` e a branch `corrigir-bug`:**

```bash
git diff master corrigir-bug
```

* **Excluir a branch `corrigir-bug` após mesclar as alterações:**

```bash
git checkout master
git merge corrigir-bug
git branch -D corrigir-bug
```
Claro! Aqui está a seção revisada com comentários mais claros e informativos:

---

## Utilizando o GitHub

### Criar um Repositório Remoto
Para adicionar um repositório remoto ao seu repositório local, use:
```sh
git remote add origin git@github.com:usuario/repositorio.git
```
*Adiciona um repositório remoto chamado `origin` com a URL especificada.*

### Ver o Nome da Branch Atual
Para verificar o nome da branch que você está utilizando:
```sh
git branch --show-current
```
*Exibe o nome da branch atual em que você está trabalhando.*

### Enviar Suas Mudanças para o Repositório Remoto
Para enviar suas alterações locais para o repositório remoto:
```sh
git push -u origin main
```
*Envia as mudanças para a branch `main` do repositório remoto `origin` e configura a branch local para rastrear a branch remota.*

### Receber as Mudanças do Repositório GitHub
Para atualizar seu repositório local com as mudanças do repositório remoto:
```sh
git pull origin main
```
*Baixa e aplica as mudanças da branch `main` do repositório remoto `origin` para o seu repositório local.*

### Ver Configurações do Repositório Remoto
Para visualizar as configurações do repositório remoto:
```sh
git remote show origin
```
*Exibe detalhes sobre o repositório remoto `origin`, incluindo as URLs de fetch e push, e o estado das branches rastreadas.*

---

Esses comentários devem tornar as instruções mais claras e úteis. Se precisar de mais alguma coisa, me avise!