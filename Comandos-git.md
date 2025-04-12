## Comandos de preparação do ambiente de trabalho git

### Git Config

```
git config --global init.username <nome> // Configura nome de usuario para o desejado

git config --global init.useremail <email> // Configura email do usuario para o desejado

git config --global init.defaltbranch <nome branch principal> // Configura nome da branch principal para novos repositorios

git branch -m <nome antigo da branch> <nome novo da branch> //  Configura nome da branch principal para o repositorio especificado
```

### Repositórios locais/remotos 

```
git init // faz com que o diretorio atual seja preparado para virar um repositorio local

git clone <url do repositorio em nuvem> // faz com que haja a clonagem de um repositorio em nuvem (Ex: GitHub)

git remote add origin <url do repositorio> // linka o repositorio local com um repositorio em nuvem para futuras modificações

git rm -rf .git // faz com que as configurações do git sejam pagadas do diretorio

git status // Mostra alterações que estão pendentes de ser feitas e a branch que elas pertencem

git restore // faz com que um arquivo desejado volte para uma versão anterior voltando todas alterações ja feitas 

```

## Commits e Alterações

```
git commit --ammend -m"mensagem do commit" // Faz a alteração de um commit ja feito

git log // Historioco de commits já feitos (Autor/data/mensagem do commit)

git reflog // mostra uma versão mais detalhadas do historico de commits

git add . // faz com que todos arquivos não rastreados no repositorio local sejam reconhecidos

_______________________________________

git reset <tipo de reset> <hash do commit> // Diferentes usos:

-soft faz com que o commit seja desfeito com todos os arquivos ja rastreados

--mixed faz com que o commit seja desfeito com todos os arquivos não rastreiados

--hard faz com que o commit selecionado seja o unico que sera considerado

git rest tambem pode ser usado para a remoção de um arquivo especifico em um diretorio:

git reset nomeDiretorio/nomeArquivo
_______________________________________