# Fluxo profissional sugerido

## Exemplo de fluxo organizado para time

### 1. Atualize a branch principal

```bash
git switch main
git pull origin main
```

### 2. Crie uma branch de trabalho

```bash
git switch -c feat/cadastro-usuario
```

### 3. Faça alterações e acompanhe o estado

```bash
git status
git diff
```

### 4. Adicione apenas o que faz sentido

```bash
git add .
```

ou arquivos específicos:

```bash
git add src/Controllers/UsuarioController.cs
git add src/Services/UsuarioService.cs
```

### 5. Faça commits pequenos e claros

```bash
git commit -m "feat: adiciona cadastro de usuário"
```

### 6. Envie a branch para o remoto

```bash
git push -u origin feat/cadastro-usuario
```

### 7. Abra um Pull Request no GitHub

Depois disso, o ideal é revisar no GitHub antes de mesclar na `main`.

## Padrão de nomes para branches

Sugestões:

- `feat/nome-da-feature`
- `fix/nome-do-bug`
- `hotfix/correcao-urgente`
- `docs/atualizacao-readme`
- `refactor/melhora-servico`

Exemplos:

```bash
feat/login-social
fix/erro-token-expirado
docs/guia-git
refactor/camada-repositorio
```

## Antes de enviar código

Checklist útil:

- rode testes
- revise arquivos modificados com `git diff --staged`
- confira se não está subindo segredo ou `.env`
- confirme a branch atual
- escreva um commit decente

## Comandos úteis para revisão

```bash
git status
git diff
git diff --staged
git log --oneline --graph --decorate --all
```

## Mantendo sua branch atualizada

```bash
git switch main
git pull origin main
git switch feat/cadastro-usuario
git merge main
```

ou:

```bash
git rebase main
```

## Publicando uma correção urgente

```bash
git switch main
git pull origin main
git switch -c hotfix/corrige-timeout
git add .
git commit -m "fix: corrige timeout na autenticação"
git push -u origin hotfix/corrige-timeout
```
