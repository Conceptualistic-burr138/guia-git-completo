# Atualizando o repositório: pull, fetch, merge e rebase

## `git pull`

O `git pull` normalmente faz duas coisas:

1. `git fetch`
2. `git merge`

Ou seja, ele baixa alterações do remoto e já tenta integrar no seu código local.

### Pull padrão

```bash
git pull
```

### Pull de branch específica

```bash
git pull origin main
```

## `git fetch`

Busca alterações do remoto, mas sem aplicar automaticamente.

```bash
git fetch
```

Buscar de um remoto específico:

```bash
git fetch origin
```

Isso é útil para inspecionar antes de misturar alterações.

## `git merge`

Integra uma branch em outra.

Exemplo: estando na `main`, juntar a branch `feat/login`:

```bash
git switch main
git merge feat/login
```

## `git rebase`

Reaplica seus commits em cima de outra base.

Exemplo:

```bash
git switch feat/login
git rebase main
```

Isso pode deixar o histórico mais linear, mas exige mais cuidado.

## Quando usar cada um?

- `pull`: para atualizar de forma rápida
- `fetch`: para baixar e analisar antes
- `merge`: para juntar históricos preservando a estrutura
- `rebase`: para manter histórico linear

## Atualizar sua branch com a `main`

Fluxo com merge:

```bash
git switch main
git pull origin main
git switch feat/minha-branch
git merge main
```

Fluxo com rebase:

```bash
git switch main
git pull origin main
git switch feat/minha-branch
git rebase main
```

## Resolver conflitos

Quando houver conflito:

1. abra os arquivos marcados
2. escolha o conteúdo correto
3. salve os arquivos
4. adicione ao staging
5. finalize a operação

Em merge:

```bash
git add .
git commit
```

Em rebase:

```bash
git add .
git rebase --continue
```

Para abortar um rebase:

```bash
git rebase --abort
```

Para abortar um merge em andamento:

```bash
git merge --abort
```
