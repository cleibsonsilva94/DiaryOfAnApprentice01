# O QUE É O GIT?

O Git é um sistema de controle de versão distribuído usado principalmente para o desenvolvimento de software. 
Ele permite que várias pessoas trabalhem em um mesmo projeto, mantendo um histórico completo de todas as alterações 
feitas no código-fonte. Com o Git, os desenvolvedores podem colaborar de forma eficiente, rastrear mudanças, reverter 
para versões anteriores, ramificar o código para desenvolver recursos separadamente e mesclar o trabalho de diferentes colaboradores.
 Ele é amplamente utilizado na indústria de software devido à sua eficácia na gestão do desenvolvimento de projetos em equipe. Abaixo
 trago alguns dos principais comandos dessa ferramenta simplesmente fascinante.

## PRINCIPAIS COMANDOS - Comentados :)

## CONFIGURAÇÃO E INICIALIZAÇÃO

git init # Inicializa um novo repositório Git local
git clone [url] # Clona um repositório remoto para o diretório local

## BÁSICO DE TRABALHO COM REPOSITÓRIOS

git add [file] # Adiciona alterações de um arquivo específico ao stage
git add . # Adiciona todas as alterações ao stage
git add -A # Adiciona todas as alterações, incluindo deletados, ao stage
git commit -m "[message]" # Cria um novo commit com as alterações no stage e uma mensagem de commit
git commit -am "[message]" # Adiciona e comita todas as alterações, permitindo adicionar uma mensagem de commit
git status # Exibe o status atual do repositório
git diff # Mostra as diferenças entre o diretório de trabalho e o stage
git diff --staged # Mostra as diferenças entre o stage e o último commit
git rm [file] # Remove um arquivo do repositório e do stage
git mv [old_file] [new_file] # Move ou renomeia um arquivo e adiciona a mudança ao stage

## TRABALHANDO COM BRANCHES

git branch # Lista todas as branches locais
git branch [branch_name] # Cria uma nova branch
git branch -d [branch_name] # Deleta uma branch
git branch -D [branch_name] # Força a deleção de uma branch
git checkout [branch_name] # Muda para uma branch específica
git checkout -b [branch_name] # Cria e muda para uma nova branch
git merge [branch_name] # Mescla uma branch específica na branch atual
git rebase [branch_name] # Rebase da branch atual a partir de outra
git cherry-pick [commit_hash] # Adiciona um commit específico de outra branch à branch atual
git stash # Salva alterações temporariamente
git stash list # Lista todos os stashes salvos
git stash apply # Aplica as alterações do último stash
git stash pop # Aplica e remove as alterações do último stash
git stash drop # Remove o último stash
git stash clear # Limpa todos os stashes salvos
git stash show [stash@{n}] # Mostra as mudanças de um stash específico

## SINCRONIZAÇÃO COM REPOSITÓRIOS REMOTOS

git remote -v # Lista todos os repositórios remotos configurados
git remote add [name] [url] # Adiciona um novo repositório remoto
git remote rename [old_name] [new_name] # Renomeia um repositório remoto
git remote remove [name] # Remove um repositório remoto
git fetch # Busca alterações do repositório remoto, mas não as mescla
git pull [remote] [branch] # Puxa e mescla as alterações do repositório remoto para a branch local
git push [remote] [branch] # Envia commits locais para o repositório remoto

## VISUALIZAÇÃO DE HISTÓRICO E DIFERENÇAS

git log # Exibe o histórico de commits
git log --oneline # Exibe o histórico de commits em uma linha
git log --graph # Exibe o histórico de commits em forma de grafo
git log --graph --decorate --all --oneline # Exibe o histórico de commits detalhado
git log --since=[date] # Exibe o histórico de commits desde uma data específica
git log --author=[author] # Exibe o histórico de commits de um autor específico
git log --grep=[pattern] # Exibe o histórico de commits com uma mensagem correspondente ao padrão
git log -p # Exibe o histórico de commits com as diferenças
git show [commit_hash] # Exibe informações detalhadas sobre um commit específico
git blame [file] # Mostra quem modificou cada linha de um arquivo e em qual commit

## DESFAZENDO ALTERAÇÕES

git checkout -- [file] # Descarta alterações não salvas em um arquivo específico
git reset [file] # Remove um arquivo do stage e do diretório de trabalho
git reset HEAD [file] # Remove um arquivo do stage, mantendo as alterações no diretório de trabalho
git reset --soft [commit] # Desfaz commits, mantendo as alterações no stage
git reset --hard [commit] # Desfaz commits e descarta todas as alterações
git clean -n # Mostra os arquivos não rastreados que seriam removidos
git clean -f # Remove arquivos não rastreados
git clean -fd # Remove arquivos não rastreados e diretórios vazios

SUBMÓDULOS
git submodule add [url] # Adiciona um submódulo ao projeto
git submodule update --init # Inicializa e atualiza os submódulos
git submodule update --recursive # Atualiza os submódulos e também os submódulos aninhados
git submodule foreach [command] # Executa um comando em cada submódulo
git submodule sync # Sincroniza os submódulos com as URLs de referência no repositório superiores

# TRABALHANDO COM TAGS
git tag # Lista todas as tags
git tag [tag_name] # Cria uma nova tag
git tag -a [tag_name] -m "[message]" # Cria uma nova tag anotada com uma mensagem
git tag -d [tag_name] # Deleta uma tag localmente
git push [remote] --tags # Envia todas as tags locais para o repositório remoto
git push [remote] :refs/tags/[tag_name] # Deleta uma tag do repositório remoto

# REFLOG
git reflog # Exibe o histórico de referências de HEAD

# BISECT
git bisect start # Inicia uma busca binária
git bisect good [commit] # Marca um commit como "bom"
git bisect bad [commit] # Marca um commit como "ruim"
git bisect reset # Reinicia o processo de bisect

# ALIASES
git config --global alias.[alias_name] [command] # Cria um alias para um comando git

# CONFIGURAÇÕES
git config --global user.name "[name]" # Configura o nome do usuário
git config --global user.email "[email]" # Configura o email do usuário
git config --global core.editor "[editor]" # Configura o editor padrão
git config --global merge.tool "[tool]" # Configura a ferramenta de merge padrão

## EXTRAS

git archive [branch_name] --format=zip --output=[file_name].zip # Cria um arquivo zip de um determinado branch
git blame [file] # Mostra quem modificou cada linha de um arquivo e em qual commit
git blame -L [start],[end] [file] # Mostra quem modificou as linhas específicas de um arquivo
git shortlog # Exibe um resumo de contribuições por autor
git shortlog -s # Exibe um resumo de contribuições por autor (sem detalhes)
git shortlog -sn # Exibe um resumo de contribuições por autor (ordenado por número de commits)
git clean -fdx # Remove arquivos não rastreados, incluindo diretórios vazios
git log --graph --decorate --pretty=oneline --abbrev-commit # Exibe o histórico de commits em formato gráfico simplificado
git checkout [commit_hash] # Muda para um commit específico
git show HEAD # Exibe informações detalhadas sobre o commit mais recente (HEAD)
git diff HEAD^ # Exibe as diferenças entre o commit mais recente e o anterior
git diff HEAD^ HEAD # Exibe as diferenças entre os dois commits mais recentes
git reset --soft HEAD^ # Desfaz o último commit mantendo as alterações no stage
git reset --hard HEAD^ # Desfaz o último commit e descarta as alterações

## UMA SUGESTÃO ;)

O Git é de longe a melhor ferramenta de versionamento que existe. 
No começo, sugiro que você anote os principais comandos. Mas quais, 
diante de tantos que existem? Os que você perceber que são mais atualizados 
na sua empresa ou os que permitirão que você consiga editar códigos, salvá-los 
temporariamente e submetê-los a um avaliador.

Anote esses comandos em um lugar onde você consiga acessá-los facilmente 
(eu anotava no Slack) e com o tempo você vai decorar boa parte deles e digo
mais, desenvolverá um grande amor e fascínio pelo recurso mais que perfeito: Git :)
