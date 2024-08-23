# avaliacao-jp
Avaliação referente a Git e Github

ls -al ~/.ssh - Verificará se existe uma chave ssh.

ssh-keygen -t ed25519 -C "your_email@example.com" - Adicionará uma nova chave.

eval "$(ssh-agent -s)" - Iniciará o agente ssh.

ssh-add ~/.ssh/id_ed25519 - Vinculará a chave ssh ao agente.

clip < ~/.ssh/id_ed25519.pub - copiará a chave SSH para adicionar ao seu Github. Ideal aqui é descrever a qual local essa chave se refere para possivel remoção.


git init - Serve para criar(inicializar) um novo repositório/repositório vazio em um diretorio existente.

git status - Mostrará o status da bracnh(repositório) atual informando se tem arquivos para serem comitados ou que estejam pendentes de alteração.

git add <filename ou . > - Responsável por incluir, alterar ou até mesmo remover um conteúdo que esteja no indice.

git rm --cached <file> - Remove do indice os arquivos que ainda não foram comitados. Vale ressaltar que o arquivo não será removido do diretorio e sim da "fila" de pronto para comitar.

git branch - Este comando irá listar as branchs já exitentes. Para listar apenas as branchs remotas poderá ser usado o comando git branch -r, já para listar as remotas e as locais deverá ser usado o git branch -a

git checkout <branchname> - Servirá para navegar entre as branchs, por exemplo, com esse comando você sairá da "main/master" e irá para a branch selecionada.

git checkout -b <branchname> - Criará uma nova branch e já irá nos redirecionar para ela.

git commit -m "<description>" - Comando responsável por "salvar" as alterações do índice mediante a descrição doque foi alterado. 

git merge <branch> - Mesclará a branch atual com a branch informada, por exemplo, eu realizarei as alterações numa branch de teste para correções de erro, após as alterações validadas posso aplicar este comando para unir essas correções para a branch principal.

git push - Enviará os commits realizados do repositório local para um que seja remoto.

git branch -D <branchname> - Removerá do repositório a branch, este comando não possui a possibilidade de reversão, ou seja, se excluir por engano precisará começar a branch novamente.

git fetch - Baixará os objetos e referencias do repositório remoto para o local, esse comando atualiza apenas as referencias locais e não necessita de reversão já que não ocorrerá o processo de merge entre eles.

git pull - Ao contrario do código anterior, este comando mesclará as mudanças do repositório remoto na branch local. Para reverter esse processo deverá ser usado o código git reset --hard<commit-hash>.

git clone <link do seu repositorio do guthub>- Como o nome sugere, esse comando clonará um repositório remoto para o repositório local. 