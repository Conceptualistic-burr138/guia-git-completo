# Primeiros passos com Git

## O que você precisa ter instalado

- Git instalado na máquina
- uma conta no GitHub, se quiser subir o projeto para a nuvem

Para verificar se o Git está instalado:

```bash
git --version
```

## Configuração inicial

Configure seu nome e email uma vez:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Ver configurações:

```bash
git config --list
git config --global --list
```

## Criando um repositório local

```bash
mkdir meu-projeto
cd meu-projeto
git init
```

Isso cria um repositório Git na pasta atual.

## Iniciando já com `main`

Em alguns ambientes a branch inicial pode vir como `master`. Para padronizar como `main`:

```bash
git branch -M main
```

## Clonando um repositório existente

```bash
git clone https://github.com/usuario/repositorio.git
```

Clonar em uma pasta com nome personalizado:

```bash
git clone https://github.com/usuario/repositorio.git meu-projeto-local
```

Depois de clonar:

```bash
cd repositorio
```

## Conferindo o estado do repositório

```bash
git status
```

Esse é um dos comandos mais importantes. Ele mostra:

- branch atual
- arquivos alterados
- arquivos em staging
- se há commits para enviar

## Ver histórico de commits

```bash
git log
```

Forma resumida:

```bash
git log --oneline
```

Forma visual com branches:

```bash
git log --oneline --graph --decorate --all
```
