# Commits

## O que é um commit?

Um commit é um registro salvo de alterações no histórico do projeto.

## Criar um commit

```bash
git commit -m "mensagem do commit"
```

Exemplo:

```bash
git commit -m "feat: adiciona endpoint de usuários"
```

## Commitando tudo que já está versionado

```bash
git commit -am "fix: corrige bug na validação"
```

Atenção: isso **não adiciona arquivos novos**. Só funciona para arquivos que o Git já conhece.

## Alterar a mensagem do último commit

Se ainda não enviou para o remoto:

```bash
git commit --amend -m "nova mensagem"
```

## Adicionar arquivos esquecidos ao último commit

```bash
git add arquivo-esquecido.txt
git commit --amend
```

## Ver histórico resumido

```bash
git log --oneline
```

## Ver último commit

```bash
git show
```

## Boas práticas para mensagens

Prefira mensagens claras e objetivas:

- diga o que foi feito
- use verbo no presente
- evite mensagens genéricas como `update` ou `ajustes`

### Exemplos ruins

```bash
git commit -m "update"
git commit -m "mudanças"
```

### Exemplos melhores

```bash
git commit -m "feat: adiciona filtro por status na listagem"
git commit -m "fix: corrige erro ao salvar endereço"
git commit -m "docs: documenta variáveis de ambiente"
```

## Padrão de commits sugerido

- `feat:` nova funcionalidade
- `fix:` correção
- `docs:` documentação
- `refactor:` reorganização de código
- `test:` testes
- `chore:` manutenção
- `style:` formatação
- `perf:` melhoria de performance

## Desfazer o último commit

Mantendo alterações nos arquivos:

```bash
git reset --soft HEAD~1
```

Voltando alterações para o working directory:

```bash
git reset HEAD~1
```

Apagando commit e alterações locais:

```bash
git reset --hard HEAD~1
```

Use `--hard` com cuidado.
