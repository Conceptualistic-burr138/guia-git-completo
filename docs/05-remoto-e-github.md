# Repositório remoto e GitHub

## Ver repositórios remotos configurados

```bash
git remote -v
```

## Adicionar um remoto

Normalmente o remoto principal recebe o nome `origin`:

```bash
git remote add origin https://github.com/usuario/repositorio.git
```

## Alterar a URL do remoto

```bash
git remote set-url origin https://github.com/usuario/novo-repositorio.git
```

## Remover um remoto

```bash
git remote remove origin
```

## Adicionar mais de um remoto

Exemplo:

```bash
git remote add origin https://github.com/usuario/repositorio.git
git remote add upstream https://github.com/empresa/repositorio-base.git
```

Verificar:

```bash
git remote -v
```

## Subir branch principal para o GitHub

```bash
git push -u origin main
```

## Subir branch nova

```bash
git push -u origin feat/minha-branch
```

## Enviar alterações depois que o upstream já foi definido

```bash
git push
```

## Baixar alterações do remoto

```bash
git pull
```

## Baixar de uma branch específica

```bash
git pull origin main
```

## Buscar alterações sem aplicar

```bash
git fetch
```

## Fluxo completo para subir um projeto local para a nuvem

```bash
git init
git add .
git commit -m "feat: commit inicial"
git branch -M main
git remote add origin https://github.com/usuario/repositorio.git
git push -u origin main
```

## Clonar e começar a trabalhar

```bash
git clone https://github.com/usuario/repositorio.git
cd repositorio
git status
```

## Trabalhando com `upstream` em fork

Quando você faz um fork:

- `origin` geralmente aponta para o seu fork
- `upstream` aponta para o repositório original

Adicionar `upstream`:

```bash
git remote add upstream https://github.com/autor/repositorio-original.git
```

Buscar atualizações do projeto original:

```bash
git fetch upstream
git switch main
git merge upstream/main
```
