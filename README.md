# git-commands

syntaxe de ajuda do commit: git --help nomeDoComandoDesejado

// inicializa um reposit�rio git na pasta atual do terminal
git init

// mostra os logs de commit de forma resumida
git log

// mostra logs de commits com o nome do arquivo alterado
git whatchanged

// mostra logs de commits de forma detalhada, mostrando o que foi alterado no arquivo em cada commit
git whatchanged -p

// seleciona arquivos para commitar
git add

// commita arquivos adicionados com uma mensagem
git commit -m ''

// envia arquivos commitados para meu reposit�rio
git push

// baixa a vers�o mais recente do meu reposit�rio
git pull 

// lista as branches presentes no repositório (caso tenha um nome em seguida, cria uma branch nova)
git branch

// entra em uma branch existente
git checkout nomeDaBranch

// Este comando vai restaurar o arquivo index.html ao seu estado original CASO ele não esteja no index ou staging area.
git checkout -- nodeDoArquivo.arq

// cria e entra em uma branch nova automaticamente
git checkout -b

// joga as atualizações de uma branch selecionada na branch atual
git merge nomeDaBranch

// unifica os commits da branch1 na branch2, evitando erros para dar push no repositório remoto
git rebase nomeDaBranch1 nomeDaBranch2

// reseta o estado de "add" de determinado arquivo
git reset HEAD nomeDoArquivo

// caso o arquivo ja tenha sido commitado, ele também pode voltar para o commit escolhido pegando o código presente no git log
git reset codigoDoCommitDesejado

// utilizado para deletar um commit especifico (mesmo que ele seja antigo)
git revert codigoDoCommitDesejado

// inicia o estado de stash, congelando alterações na memória do computador e poder ser acessada depois para enfim poder ser commitada
git stash

// lista todos stashs atuais na memória
git stash list


// retorna o stash mais recente da memória
git stash pop

// pode ser usado para retomar um stash especifico que está na memória (o nome do stash é adquirido através do list)
gis stash apply nomeDoStash


// apaga da memória o stash 
git stash drop

// git bisect é uma ferramenta de localização de commits que funciona de forma dinâmica. com o start ele é iniciado.
git bisect start

// após iniciado deve ser dito 2 parâmetros, selecionando 1 commit que voce tenha certeza que é ruim e qual commit é bom, com isso a ferramenta já pode ter ideia de onde pode ser localizado o commit em bom estado mais recente na aplicação
git bisect bad HEAD
git bisect good codigoDoCommitDesejado
// a partir disso você poderá dizer a ferramenta qual commit está bom e ruim até chegar a conclusão final dizendo bisect bad ou good

// o arquivo .gitconfig presente na raiz do usuário é onde pode ser alterado detalhes importantes, de cores a alias (atalhos) para otimizar o desenvolvimento
[alias]
	checkout = co

// utilizado para transferir apenas um commit especifico na branch master (diferente do rebase ou merge)
git cherry-pick

// git cola é uma forma de obter interface gráfica no git, facilitando alguns detalhes, segue link de download
http://git-cola.github.io/downloads.html

// em caso de uso de .gitignore, caso preciso atualizar os conteudos atualizado em seu repositório, será necessario limpar o cache com o seguinte código
git rm -r --cached .
