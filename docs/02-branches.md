# Branches no Git

## O que é uma branch?

Uma branch é uma linha de trabalho separada. Ela permite desenvolver uma funcionalidade sem bagunçar a branch principal.

## Ver branch atual

```bash
git branch
```

A branch atual aparece com `*`.

## Listar branches locais

```bash
git branch
```

## Listar branches remotas

```bash
git branch -r
```

## Listar todas as branches

```bash
git branch -a
```

## Criar uma nova branch

```bash
git branch nome-da-branch
```

Exemplo:

```bash
git branch feat/login
```

## Mudar para outra branch

Forma moderna:

```bash
git switch nome-da-branch
```

Forma antiga, ainda muito usada:

```bash
git checkout nome-da-branch
```

## Criar e já entrar na branch

Forma moderna:

```bash
git switch -c nome-da-branch
```

Forma antiga:

```bash
git checkout -b nome-da-branch
```

## Renomear branch atual

```bash
git branch -m novo-nome
```

## Renomear uma branch específica

```bash
git branch -m nome-antigo novo-nome
```

## Mudar o nome da branch principal para `main`

```bash
git branch -M main
```

## Excluir branch local

```bash
git branch -d nome-da-branch
```

Forçando exclusão:

```bash
git branch -D nome-da-branch
```

## Excluir branch remota

```bash
git push origin --delete nome-da-branch
```

## Enviar uma branch nova para o remoto

```bash
git push -u origin nome-da-branch
```

O `-u` define a branch remota como upstream. Depois disso, normalmente basta usar `git push` e `git pull`.

## Ver em qual branch você está

```bash
git branch --show-current
```

## Criar branch a partir de outra branch atualizada

Exemplo recomendado:

```bash
git switch main
git pull origin main
git switch -c feat/nova-funcionalidade
```
