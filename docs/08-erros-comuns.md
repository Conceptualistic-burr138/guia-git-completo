# Erros comuns e como resolver

## `fatal: not a git repository`

Você executou um comando Git fora de uma pasta versionada.

Resolva entrando na pasta correta ou iniciando o repositório:

```bash
git init
```

## `remote origin already exists`

O remoto `origin` já foi criado.

Veja os remotos:

```bash
git remote -v
```

Troque a URL:

```bash
git remote set-url origin NOVA_URL
```

Ou remova e adicione de novo:

```bash
git remote remove origin
git remote add origin NOVA_URL
```

## `src refspec main does not match any`

Normalmente acontece quando ainda não existe commit ou a branch tem outro nome.

Faça pelo menos um commit:

```bash
git add .
git commit -m "feat: commit inicial"
```

Depois confira a branch:

```bash
git branch
```

Se necessário:

```bash
git branch -M main
```

## `failed to push some refs`

O remoto tem alterações que você ainda não trouxe.

Tente:

```bash
git pull origin main --rebase
```

Depois:

```bash
git push origin main
```

## Conflitos de merge

O mesmo trecho foi alterado em dois lugares.

Passos:

1. abrir os arquivos com conflito
2. editar manualmente
3. salvar
4. `git add .`
5. concluir merge ou rebase

## Commit na branch errada

Se ainda não enviou:

```bash
git reset --soft HEAD~1
git switch -c nome-da-branch-correta
git commit -m "feat: commit movido para branch correta"
```

## Subi arquivo sensível sem querer

Se ainda não enviou:

```bash
git rm --cached .env
```

Adicione ao `.gitignore` e faça novo commit.

Se já enviou ao remoto, o ideal é:

- remover o arquivo do histórico
- trocar credenciais vazadas imediatamente

## Apaguei arquivo por engano

Se a alteração ainda não foi commitada:

```bash
git restore nome-do-arquivo
```

Se quer recuperar de um commit anterior:

```bash
git checkout HASH_DO_COMMIT -- nome-do-arquivo
```
