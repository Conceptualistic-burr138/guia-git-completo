# Arquivos, staging e área de preparação

## Entendendo o fluxo

No Git, geralmente os arquivos passam por estas etapas:

1. alterado no diretório de trabalho
2. adicionado ao staging com `git add`
3. salvo em commit com `git commit`

## Ver o estado dos arquivos

```bash
git status
```

## Adicionar um arquivo específico

```bash
git add arquivo.txt
```

## Adicionar vários arquivos

```bash
git add arquivo1.txt arquivo2.txt
```

## Adicionar tudo

```bash
git add .
```

## Adicionar tudo no repositório inteiro

```bash
git add -A
```

## Remover um arquivo do staging, sem apagar da pasta

```bash
git reset arquivo.txt
```

ou:

```bash
git restore --staged arquivo.txt
```

## Remover todos os arquivos do staging

```bash
git reset
```

ou:

```bash
git restore --staged .
```

## Descartar mudanças locais de um arquivo

```bash
git restore arquivo.txt
```

## Descartar todas as mudanças locais ainda não commitadas

```bash
git restore .
```

## Remover arquivo do projeto e registrar no Git

```bash
git rm arquivo.txt
```

## Remover diretório recursivamente

```bash
git rm -r pasta/
```

## Remover do Git mas manter o arquivo local

Útil quando você quer parar de versionar um arquivo, mas sem apagar da máquina.

```bash
git rm --cached arquivo.txt
```

Exemplo comum com `.env`:

```bash
git rm --cached .env
```

Depois, adicione no `.gitignore`.

## Ver diferenças antes de commitar

```bash
git diff
```

Ver diferenças só do que já está em staging:

```bash
git diff --staged
```

## Ignorar arquivos com `.gitignore`

Exemplo:

```gitignore
bin/
obj/
node_modules/
.env
*.log
```

Isso evita subir arquivos desnecessários ou sensíveis.
