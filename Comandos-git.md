
# Guia de Comandos Git/GitHub

## 📋 Configuração do Ambiente Git

### Configuração Inicial

```bash
# Configura nome de usuário globalmente
git config --global user.name "<nome>"

# Configura email do usuário globalmente
git config --global user.email "<email>"

# Configura nome da branch principal para novos repositórios
git config --global init.defaultBranch "<nome-da-branch-principal>"

# Renomeia branch atual
git branch -m <nome-antigo> <nome-novo>

# Criar alias para comandos
git config --global alias.<apelido> "<comando>"
```

## 🗂️ Repositórios Locais e Remotos

### Inicialização e Clonagem

```bash
# Inicializa repositório Git no diretório atual
git init

# Clona repositório remoto
git clone <url-do-repositorio>

# Conecta repositório local com remoto
git remote add origin <url-do-repositorio>

# Remove configurações Git do diretório
rm -rf .git
```

### Status e Restauração

```bash
# Mostra status das alterações pendentes
git status

# Restaura arquivo específico para versão anterior
git restore <nome-do-arquivo>

# Descarta todas as mudanças não staged
git restore .
```

## 💾 Commits e Alterações

### Adicionando e Commitando

```bash
# Adiciona todos os arquivos ao staging
git add .

# Adiciona arquivo específico
git add <nome-do-arquivo>

# Realiza commit com mensagem
git commit -m "mensagem do commit"

# Modifica o último commit
git commit --amend -m "nova mensagem"
```

### Histórico e Logs

```bash
# Mostra histórico de commits
git log

# Mostra histórico detalhado com referências
git reflog

# Mostra log em uma linha por commit
git log --oneline
```

### Reset e Reversão

```bash
# Reset soft - mantém arquivos staged
git reset --soft <hash-do-commit>

# Reset mixed (padrão) - remove do staging
git reset --mixed <hash-do-commit>

# Reset hard - descarta todas as mudanças
git reset --hard <hash-do-commit>

# Remove arquivo específico do staging
git reset HEAD <caminho/arquivo>
```

## 🌐 Sincronização com Repositório Remoto

### Push e Pull

```bash
# Envia alterações para repositório remoto
git push

# Primeira vez enviando branch para remoto
git push -u origin <nome-da-branch>

# Busca e integra mudanças do repositório remoto
git pull

# Busca mudanças sem integrar
git fetch
```

## 🌿 Trabalhando com Branches

### Criação e Navegação

```bash
# Cria nova branch
git branch <nome-da-branch>

# Cria e muda para nova branch
git checkout -b <nome-da-branch>

# Muda para branch existente
git checkout <nome-da-branch>

# Muda para branch (comando mais novo)
git switch <nome-da-branch>
```

### Gerenciamento de Branches

```bash
# Lista todas as branches
git branch

# Lista branches com último commit
git branch -v

# Renomeia branch atual
git branch -m <novo-nome>

# Deleta branch local
git branch -d <nome-da-branch>

# Força deleção de branch
git branch -D <nome-da-branch>
```

### Merge e Integração

```bash
# Faz merge de uma branch na atual
git merge <nome-da-branch-origem>

# Merge sem fast-forward (cria commit de merge)
git merge --no-ff <nome-da-branch>
```

## ⚠️ Cuidados e Boas Práticas

### Verificações Importantes

#### 1. Verificar Diretório Correto

```bash
# Mostra caminho atual
pwd

# Verifica se existe pasta .git (repositório inicializado)
ls -la | grep .git

# Ou navega para pasta .git
cd .git
```

#### 2. Antes de Fazer Commits

- ✅ Verificar se está na branch correta: `git branch`
- ✅ Conferir status das mudanças: `git status`
- ✅ Revisar arquivos que serão commitados: `git diff --staged`
- ✅ Usar mensagens de commit descritivas

#### 3. Erros Comuns a Evitar

- ❌ Fazer commit na branch errada
- ❌ Não verificar o diretório atual
- ❌ Fazer push sem pull (em trabalho colaborativo)
- ❌ Usar `git reset --hard` sem backup
- ❌ Commitar arquivos sensíveis (senhas, tokens)

### Comandos Úteis de Verificação

```bash
# Verifica configurações atuais
git config --list

# Verifica repositórios remotos
git remote -v

# Verifica diferenças não commitadas
git diff

# Verifica diferenças staged
git diff --staged
```

## 📁 Arquivo .gitignore

```gitignore
# Exemplos de arquivos/pastas a ignorar
node_modules/
.env
*.log
.DS_Store
dist/
build/
```

---

> **Dica:** Use `git help <comando>` para obter ajuda detalhada sobre qualquer comando Git.