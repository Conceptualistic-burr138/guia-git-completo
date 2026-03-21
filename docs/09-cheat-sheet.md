# Cheat sheet rápido de Git

## Inicialização

```bash
git init
git clone <url>
git config --global --list
```

## Status e histórico

```bash
git status
git log
git log --oneline
git diff
git diff --staged
```

## Staging e arquivos

```bash
git add arquivo.txt
git add .
git add -A
git reset arquivo.txt
git reset
git restore --staged arquivo.txt
git restore arquivo.txt
git rm arquivo.txt
git rm --cached arquivo.txt
```

## Branches

```bash
git branch
git branch -a
git branch -r
git branch -m novo-nome
git branch -M main
git switch main
git switch -c feat/minha-branch
git checkout -b feat/minha-branch
git branch -d nome-da-branch
git push origin --delete nome-da-branch
```

## Commits

```bash
git commit -m "feat: nova feature"
git commit -am "fix: corrige bug"
git commit --amend -m "nova mensagem"
```

## Remoto

```bash
git remote -v
git remote add origin <url>
git remote set-url origin <url>
git remote remove origin
```

## Envio e atualização

```bash
git push -u origin main
git push -u origin feat/minha-branch
git push
git pull
git pull origin main
git fetch
git merge main
git rebase main
```

## Desfazer

```bash
git reset --soft HEAD~1
git reset HEAD~1
git reset --hard HEAD~1
git rebase --abort
git merge --abort
```
