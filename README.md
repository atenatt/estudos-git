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

Substitua as datas entre aspas pelas datas desej