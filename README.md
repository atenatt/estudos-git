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

## Integração de Branches e Tags no Git: Um Guia Simplificado

### Introdução

Este guia apresenta os comandos essenciais para integrar branches e gerenciar tags no Git, permitindo que você trabalhe de forma organizada e eficiente em seus projetos.

### Integração de Branches na Main

**1. Mudar para a Branch Principal:**

```bash
git checkout main
```

**2. Mesclar a Branch:**

```bash
git merge nome-da-branch
```

**Observações:**

* Este comando integra as alterações da sua branch na `main`, criando um novo commit que registra a fusão.
* Se houver conflitos de merge, resolva-os manualmente antes de continuar.
* Utilize `git merge --abort` para cancelar a fusão em caso de problemas.
* Utilize `git merge --continue` para retomar a fusão após a resolução de conflitos.

**Exemplo:**

```bash
git checkout main
git merge feature/nova-funcionalidade

# Se houver conflitos, resolva-os manualmente

git add .
git commit -m "Mesclando feature/nova-funcionalidade na main"
```

### Rebasando Branches

O rebasamento reescreve o histórico de commits da sua branch, aplicando suas alterações em cima da `main` de forma linear. Utilize o comando:

```bash
git rebase main
```

**Observações:**

* O rebasamento pode ser útil para manter um histórico de commits mais limpo e linear, especialmente ao trabalhar em conjunto com outros colaboradores.
* Tenha cuidado ao utilizar o rebasamento, pois ele pode reescrever a história de commits já publicados em outros repositórios.

**Exemplo:**

```bash
git rebase main

# Se houver conflitos, resolva-os manualmente

git push origin HEAD:main
```

### Tags Leves e Anotadas

#### Tags Leves

* Marcadores simples para um commit específico.
* **Criar:** `git tag nome-da-tag`
* **Listar:** `git tag`
* **Remover:** `git tag -d nome-da-tag`

**Exemplo:**

```bash
git tag v1.0.0
```

#### Tags Anotadas

* Armazenam mais informações (mensagem, data, assinatura).
* **Criar:** `git tag -s nome-da-tag -m "Descrição da tag"`
* **Visualizar:** `git tag -v nome-da-tag`

**Exemplo:**

```bash
git tag -s v1.0.0 -m "Primeira versão estável do projeto"
```

### Publicando e Removendo Tags

**Publicar:** `git push origin nome-da-tag`

**Remover:** `git push origin --delete nome-da-tag`

**Observações:**

* Somente tags anotadas podem ser publicadas no repositório remoto.
* Tags leves são armazenadas localmente e não são compartilhadas automaticamente.

**Exemplo:**

```bash
git push origin v1.0.0

# Para remover a tag remota:

git push origin --delete v1.0.0
```

### Recomendações

* Utilize branches para separar diferentes versões do seu projeto.
* Utilize tags para marcar releases importantes ou pontos específicos no histórico.
* Dê nomes descritivos para branches e tags.
* Utilize `git branch` para visualizar branches.
* Utilize `git tag` para gerenciar tags.
* Publique tags para compartilhar com colaboradores.
* Remova tags desatualizadas.

## Desfazendo Mudanças, Corrigindo Commits e Gerenciando Branches no Git

Este guia complementa o guia anterior, apresentando comandos essenciais para desfazer alterações locais, corrigir commits e gerenciar branches de forma eficiente no Git.

### Desfazendo Mudanças Locais

**1. Desfazendo Mudanças em Arquivos Específicos:**

* Para desfazer as alterações não comitadas em um único arquivo, utilize:

```bash
git checkout -- nome-do-arquivo
```

* Substitua `nome-do-arquivo` pelo nome do arquivo que deseja reverter.

**2. Desfazendo Mudanças no Stage:**

* Para desfazer as alterações que já foram staggeadas, mas ainda não comitadas, utilize o comando:

```bash
git reset --hard HEAD
```

**Observação:** Este comando descartará todas as alterações no stage, tenha cuidado ao usá-lo.

**3. Removendo um Commit Local Recente:**

* Para remover o commit mais recente do seu histórico local, utilize o comando:

```bash
git reset --hard HEAD~1
```

**Observação:** Este comando removerá o commit do seu histórico local, mas não o removerá do repositório remoto se já tiver sido enviado.

### Corrigindo Commits

**1. Corrigindo a Última Mensagem de Commit:**

* Para editar a mensagem do último commit, utilize o comando:

```bash
git commit --amend
```

* Você poderá alterar a mensagem do commit e salvar as alterações.

**2. Revertendo um Commit Anterior:**

* Para reverter um commit específico, utilize o comando:

```bash
git revert HASH-DO-COMMIT
```

* Substitua `HASH-DO-COMMIT` pelo hash do commit que deseja reverter.

**Observação:** Este comando cria um novo commit para reverter as alterações do commit original.

### Gerenciando Branches

**1. Mudando de Branch sem Commitar:**

* Para mudar para outra branch sem salvar as alterações atuais, utilize o comando:

```bash
git stash
```

* Este comando armazenará as alterações não comitadas em um "stash" e mudará para a branch desejada.

**2. Retornando para as Alterações Armazenadas:**

* Para recuperar as alterações armazenadas no stash e aplicá-las na branch atual, utilize o comando:

```bash
git stash pop
```

**Observação:** Este comando aplicará as alterações do stash na branch atual e removerá o stash.

### Forçando um Push

**1. Forçando um Push para o Repositório Remoto:**

* Em situações excepcionais, você pode forçar um push para o repositório remoto, sobrescrevendo as alterações existentes na branch. Utilize o comando com cautela:

```bash
git push origin main --force
```

**Observações:**

* Utilize este comando apenas quando for absolutamente necessário e tenha certeza das consequências.
* Forçar um push pode causar problemas de versionamento e conflitos com outros colaboradores.

### Recomendações

* Utilize o comando `git status` para verificar o estado do seu repositório e identificar quais alterações estão em andamento, staggeadas ou comitadas.
* Faça commits frequentes para salvar seu trabalho e facilitar o rollback caso necessário.
* Utilize branches para separar diferentes versões do seu projeto e trabalhar em funcionalidades independentes.
* Utilize o comando `git log` para visualizar o histórico de commits e identificar o hash do commit que deseja reverter.
* Tenha cuidado ao utilizar comandos que alteram o histórico de commits, como `git reset` e `git revert`.


