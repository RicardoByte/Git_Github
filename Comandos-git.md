## *Comandos de preparação do ambiente de trabalho git/gitHub

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

git restore . // descartar todas as mudanças não staged

```

### Commits e Alterações

```
git commit --ammend -m"mensagem do commit" // Faz a alteração de um commit ja feito

git log // Historico de commits já feitos (Autor/data/mensagem do commit)

git reflog // mostra uma versão mais detalhadas do historico de commits

git add . // faz com que todos arquivos não rastreados no repositorio local sejam reconhecidos

$ git config --global alias.<apelido> <nome do comando> // Faz com que você adcione apelidos aos comandos do git

_______________________________________

git reset <tipo de reset> <hash do commit> // Diferentes usos:

-soft faz com que o commit seja desfeito com todos os arquivos ja rastreados

--mixed faz com que o commit seja desfeito com todos os arquivos não rastreiados

--hard faz com que o commit selecionado seja o unico que sera considerado

git rest tambem pode ser usado para a remoção de um arquivo especifico em um diretorio:

git reset HEAD nomeDiretorio/nomeArquivo
________________________________________

git push: envia alterações para o repositório remoto.

git push -u origin main // Envia os conteúdos do branch main do repositório local para o repositório remoto chamado origin, e define o main remoto como referência padrão para futuros push e pull.

git pull // pega informações que foram mudadas diretamente pelo repositorio remoto e trazendo elas para o repositorio local

-----------------------------------------


```



### Trabalhando com Branches 

``
```
git checkout -b <nome da branch nova> // cria uma nova branch

git checkout <nome da branch desejada> // muda a branch pra que foi selecionada

git branch // mostra o historico de branches 

git branch -m novo-nome // renomeia nome da branch atual

git branch -v <nome da branch desejada> // mostra o historico de branches e o commit mais recente adicionado

git branch -d <nome da branch desejada> // Remove a branch desejada

git merge <nome da branch que sera mesclada> // faz a mesclagem de uma branch em outra (É necessario estar na branch que recebera a outra)


```


### Cuidados ao fazer commits/alterações e erros comuns/meus erros 

### 1º Erro: Verificar se esta na pasta/arquivo correta do repositorio

Dicas de Prevenção: comandos como: 

1 - pwd: faz com que seu caminho no terminal seja mostrado para a verificação.
2 - cd .git: Se iniciado corretamente o repositorio tera esta pasta escondida se não houver a pasta em questão não tem iniciação git.

