# Guia Completo de Git e GitHub

Um guia prático e direto para iniciantes e para quem quer ter um material de referência no dia a dia.

Este repositório reúne os principais comandos de **Git** para:

- iniciar um repositório local
- conectar com um repositório remoto
- trabalhar com branches
- adicionar, remover e restaurar arquivos
- criar commits
- enviar alterações para o GitHub
- atualizar o projeto com `pull`
- clonar repositórios
- usar fluxos mais profissionais no dia a dia

## Estrutura da documentação

- [Primeiros passos](docs/01-primeiros-passos.md)
- [Branches](docs/02-branches.md)
- [Arquivos e staging (`add`, `reset`, `restore`, `rm`)](docs/03-arquivos-e-staging.md)
- [Commits](docs/04-commits.md)
- [Repositório remoto e GitHub](docs/05-remoto-e-github.md)
- [Pull, fetch, merge e rebase](docs/06-atualizando-o-repositorio.md)
- [Fluxo profissional sugerido](docs/07-fluxo-profissional.md)
- [Erros comuns e como resolver](docs/08-erros-comuns.md)
- [Cheat sheet rápido](docs/09-cheat-sheet.md)

---

## 1) O que é Git?

O **Git** é um sistema de versionamento. Ele registra mudanças no código e permite:

- voltar para versões anteriores
- trabalhar em equipe sem sobrescrever código dos outros
- criar branches para novas funcionalidades
- sincronizar o projeto com plataformas como GitHub, GitLab e Bitbucket

## 2) O que é GitHub?

O **GitHub** é uma plataforma online para hospedar repositórios Git.

Em resumo:

- **Git** = ferramenta de versionamento local
- **GitHub** = serviço na nuvem para armazenar e compartilhar repositórios Git

---

## 3) Configuração inicial

Antes de começar, vale configurar seu nome e email no Git:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Para conferir:

```bash
git config --global --list
```

---

## 4) Cenários mais comuns

### Criar um repositório local do zero

```bash
mkdir meu-projeto
cd meu-projeto
git init
```

### Clonar um repositório existente

```bash
git clone https://github.com/usuario/repositorio.git
```

### Subir um projeto local para o GitHub

```bash
git init
git add .
git commit -m "feat: commit inicial"
git branch -M main
git remote add origin https://github.com/usuario/repositorio.git
git push -u origin main
```

### Criar uma branch e já entrar nela

```bash
git checkout -b minha-branch
```

ou, no formato mais novo:

```bash
git switch -c minha-branch
```

### Atualizar sua branch local com uma branch remota específica

```bash
git pull origin main
```

---

## 5) Sequência básica do dia a dia

Fluxo simples e muito usado:

```bash
git status
git add .
git commit -m "feat: adiciona tela de login"
git push
```

Se estiver começando uma funcionalidade nova:

```bash
git switch main
git pull origin main
git switch -c feat/tela-login
# faz as alterações
git add .
git commit -m "feat: cria tela de login"
git push -u origin feat/tela-login
```

---

## 6) Convenção de commits sugerida

Uma forma mais organizada de escrever commits:

- `feat:` nova funcionalidade
- `fix:` correção de bug
- `docs:` documentação
- `refactor:` refatoração sem alterar comportamento
- `test:` testes
- `chore:` tarefas de manutenção
- `style:` formatação

Exemplos:

```bash
git commit -m "feat: adiciona autenticação com JWT"
git commit -m "fix: corrige erro na validação do formulário"
git commit -m "docs: atualiza guia de instalação"
```

---

## 7) Comandos mais usados

```bash
git init
git clone <url>
git status
git add .
git commit -m "mensagem"
git branch
git checkout <branch>
git checkout -b <nova-branch>
git switch <branch>
git switch -c <nova-branch>
git branch -M main
git remote add origin <url>
git remote -v
git pull origin main
git push -u origin main
```

---

## 8) Licença de uso da documentação

Você pode adaptar este conteúdo para o seu repositório público e ajustar os exemplos para o fluxo da sua equipe.
