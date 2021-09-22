# Comandos Básicos do Git 🤓

- **git config**

Um dos comandos git mais usados ​​é o `git config` que é usado para definir valores de configuração específicos do usuário como e-mail, algoritmo preferido para diff, nome de usuário, formato de arquivo, etc. Por exemplo, o seguinte comando pode ser usado para definir o email:

> `git config --global user.email foo@bar.com`

- **git init**

Este comando é usado para criar um novo repositório GIT. Uso:

> `git init`

- **git add**

O comando `git add` pode ser usado para adicionar arquivos novos ou modificados (*unstracked* ou *modified*) ao índice (*staged*). Por exemplo, o seguinte comando irá adicionar um arquivo chamado *temp.txt* presente no diretório local para o índice:

> `git add temp.txt`

Ou para adicionar todos os arquivos ao índice:

> `git add .`

ou

> `git add *`


- **git clone**

O comando `git clone` é usado clonar (copiar) um repositório remoto (no Github) para um repositório local, use:

> `git clone https://github.com/nome_usuario/nome-repositorio`

- **git commit**

O comando `git commit` é usado para confirmar as alterações na HEAD. Tenha em atenção que quaisquer alterações efetuadas ainda não irão para o repositório remoto. Uso:

> `git commit –m “coloque sua mensagem aqui”`

- **git status**

O comando `git status` exibe uma lista de arquivos alterados juntamente com os arquivos que ainda não foram adicionados ou confirmados. Uso:

> `git status`

- **git push**

É outro dos comandos git básicos mais usados. Envia as alterações feitas no seu diretório local para o ramo principal do repositório remoto associado ao diretório de trabalho. Por exemplo:

> `git push origin main`

- **git checkout**

O comando `git checkout` pode ser usado para criar *branches* ou alternar entre elas. Por exemplo, o seguinte cria uma nova *branch* e muda para ela:

> `command git checkout -b <branch-name>`

Para simplesmente mudar de uma *branch* para outra, use:

> `git checkout <branch-name>`

- **git remote**

O comando `git remote` permite que um usuário se conecte a um repositório remoto. O comando a seguir lista os repositórios remotos atualmente configurados:

> `git remote –v`

Esse comando permite que o usuário se conecte a um servidor remoto:

> `git remote add origin <93.188.160.58>`

- **git branch**

O comando `git branch` pode ser usado para listar, criar ou excluir *branches*. Para listar todos as *branches* presentes no repositório, use:

> `git branch`

Para excluir uma *branch*:

> `git branch –d <branch-name>`

- **git pull**

O comando `git pull` é usado para buscar e baixar conteúdo de repositórios remotos e fazer a atualização imediata ao repositório local para que os conteúdos sejam iguais. Uso:

> `git pull <remote>`

- **git merge**

O comando `git merge` incorpora as alterações dos commits da *branch* remota (desde o momento em que os seus históricos divergirem da *branch* atual) para dentro da *branch* atual. Uso:

> `git merge <branch-name>`

- **git diff**

O comando `git diff` é usado para listar os conflitos entre os arquivos. Para visualizar conflitos com o arquivo base, use:

> `git diff --base <file-name>`

O seguinte comando é usado para exibir os conflitos entre *branches* *about-to-be-merged* antes de mesclá-los:

> `git diff <source-branch> <target-branch>`

Para simplesmente listar todos os conflitos atuais, use:

> `git diff`

- **git tag**

A marcação é usada para marcar compromissos específicos com alças simples. Um exemplo pode ser:

> `git tag 1.1.0 <insert-commitID-here>`

- **git log**

Executar o comando `git log` exibe o registro de *log* do *commit*, juntamente com os detalhes pertinentes. Um exemplo de saída pode ser:

> commit 15f4b6c44b3c8344caasdac9e4be13246e21sadw
> Author: Alex Hunter <alexh@gmail.com>
> Date:   Mon Oct 1 12:56:29 2016 -0600

Para exibir o *log* de maneira resumida, use:

> `git log --oneline`

- **git reset**

O comando `git reset` é usado para redefinir o índice e o diretório de trabalho para o estado do último *commit*. Uso:

> `git reset --hard HEAD`

- **git rm**
O comando `git rm` pode ser usado para remover arquivos do índice e do diretório de trabalho. Uso:

> `git rm filename.txt`

- **git stash**

Provavelmente um dos menos conhecidos comandos git básicos é `git stash` que ajuda a salvar as mudanças que não devem ser *commitados* imediatamente, mas em uma base temporária. Uso:

> `git stash`

- **git show**

Para visualizar informações sobre qualquer objeto git, use o comando git show. Por exemplo:

> `git show`

- **git fetch**

O comando **git fetch** permite que um usuário obtenha todos os objetos do repositório remoto que atualmente não residem no diretório de trabalho local. Exemplo de uso:

> `git fetch origin`

- **git ls-tree**

Para exibir um objeto `tree` juntamente com o nome e o modo de cada item e o valor SHA-1 do blob, use o comando `git ls-tree`. Por exemplo:

> `git ls-tree HEAD`

- **git cat-file**

Usando o valor SHA-1, exiba o tipo de um objeto usando o comando `git cat-file`. Por exemplo:

> `git cat-file –p d670460b4b4aece5915caf5c68d12f560a9fe3e4`

- **git grep**

O comando `git grep` permite que um usuário procure, através das *trees*, frases e/ou palavras. Por exemplo, para pesquisar *www.hostinger.com* em todos os arquivos, use:

> `git grep "www.hostinger.com"`

- **gitk**

O comando `gitk` é a interface gráfica do Git para um repositório local que pode ser invocado digitando e executando:

> `gitk`

- **git instaweb**

Com o comando `git instaweb`, um servidor *web* pode ser executado em interface com o repositório local. Um navegador da Web também é automaticamente direcionado para ele. Por exemplo:

> `git instaweb –httpd=webrick`

- **git gc**

Para otimizar o repositório através da coleta de lixo, que irá limpar arquivos desnecessários e otimizá-los, use:

> `git gc`

-- **git archive**

O comando `git archive` permite que um usuário crie um arquivo **zip** ou **tar** contendo os componentes de uma única *tree* de repositório. Por exemplo:

> `git archive --format=tar main`

- **git prune**

Através do comando `git prune`, os objetos não acessíveis são excluídos. Uso:

> `git prune`

- **git fsck**
Para executar uma verificação de integridade do sistema de arquivos git, use o comando `git fsck`. Todos os objetos corrompidos são identificados:

> `git fsck`

- **git rebase**

Geralmente, o comando `git rebase` é usado para editar mensagens anteriores do *commit*, combinar vários *commits* em um, excluir ou reverter *commits* que não são mais necessários. Por exemplo:

> `git rebase master`

ou

> `git rebase --interactive other_branch_name`

### Conclusão

Alguns dos comandos git básicos são usados com mais frequência. Outros exigem um nível mais avançado de usuário para não corrermos o risco de perder nosso código. Em caso de dúvidas, consulte a [documentação GIT](https://git-scm.com/doc) disponível nesse link.

#### Autor: mtaranto

