# Repositório do Desafio de Projeto sobre Git/GitHub da DIO

Repositório criado para o desafio do projeto

## Repositórios

Repositórios no Git ajuda você a acompanhar os progressos e mudanças feitas no projeto e também a reverte-las se não for satisfatório.

## Repositórios Bare

**O que é um repositório ?**
Um repositório padrão tem uma pasta .git, que é a espinha dorsal do repositório onde todos os arquivos importantes para rastrear as alterações nas pastas são armazenados.
A estrutura de arquivos do repositório padrão deve ser algo assim:


    -- Default_Repo* 

    |-- .git* 

    |          |-- hooks* 

    |          |-- info* 

    |          |-- logs* 

    |          |-- objects* 

    |          |-- refs* 

    |          |-- COMMIT_EDITMSG 

    |          |-- config 

    |          |-- description 

    |          |-- HEAD 

    |          |-- index 

    |-- example.txt 


*: Folders 

Como você pode ver, a pasta .git contém todos os arquivos necessários para rastrear a pasta do projeto. O repositório padrão é sempre usado para repositórios locais.

## O que é um repositório Bare?
Um repositório Bare é semelhante ao Repositório padrão, mas nenhum compromisso pode ser feito em um repositório Bare. As mudanças feitas nos projetos não podem ser acompanhadas por um repositório Remoto, pois não tem uma árvore de trabalho. Uma árvore de trabalho é um diretório no qual todos os arquivos/subarquivos do projeto residem. O repositório Bare é essencialmente uma pasta ''**.git**'' com uma pasta específica onde todos os arquivos do projeto residem.
Praticamente falando tudo no repositório além de .git é uma parte da árvore de trabalho. Para criar um repositório Bare, navegue até o diretório escolhido em Git Bash e digite:

 
>mkdir FileName (Crie o diretório)

>cd FileName  (entre no diretório)

>git init --bare   (Inicie o Repositório Bare)

Criando repositório Bare...

A estrutura de arquivos do repositório Bare deve ser assim:


    -- BareRepositorio* 

              |-- hooks* 

              |-- info* 

              |-- logs* 

              |-- objects* 

              |-- refs* 

              |-- COMMIT_EDITMSG 

              |-- config 

              |-- description 

              |-- HEAD 

              |-- index 


*: Folders 

***Nota***: Esta é exatamente a mesma estrutura de arquivo da pasta .git no repositório padrão.

***Usando um repositório Bare***
Um repositório Bare está ligado a um repositório local, portanto, os arquivos em .git de repositório local devem coincidir com os arquivos no repositório Bare. Primeiro, crie um repositório Bare e em seguida, crie uma pasta de repositório local e clone o repositório Bare.

 
>cd C:/Users/example/repositories **(Entrando no repositório "repositories")**

>git clone C:/Users/example/BareRepositorio . **(Copie o caminho para o diretórioBare e use o git clone no repositório ""repositories"")**

Cloning into 'BareRepositorio'...

warning: You appear to have cloned an empty repository. 

done. 

___Configure o usuário___
>git config --global user.name "exemplo nome"

>git config --global user.email "exemplo@email"

Não se preocupe com o aviso. O repositório clonado terá o mesmo nome do Repositório Bare, navegará até essa pasta e adicionará arquivos de projeto e realizará alterações. Em seguida, empurre as aalterações para o repositório Bare:

>git add * (Jogue todas as alterações para o Repositório Local, **''Stage''**)

>git commit -m “First commit”  (Salve no Git criando a nova instacia e torne o repositório **''Unmodified''**)

[master (root-commit) ffdf43f] First Commit 

 1 file changed, 1 insertion(+) 

 create mode 100644 example.txt 


>git push c:/users/example/BareRepositorio  (Envie para o Repositório Bare as mudanças feitas no Projeto)

Enumerating objects: 3, done. 

Counting objects: 100% (3/3), done. 

Delta compression using up to 4 threads 

Compressing objects: 100% (2/2), done. 

Writing objects: 100% (3/3), 293 bytes | 97.00 KiB/s, done. 

Total 3 (delta 0), reused 0 (delta 0) 

To c:/users/example /BareRepo.git  

 * [new branch]      master -> master 

E assim, seu repositório local foi ligado ao Repositório Bare. 

Acredito que a grande vantagem desse tipo de Repositório seja o fato de preservamos melhor o projeto original, (sem poluilo), de correr riscos de alterações imprevistas e um melhor fluxo de trabalho onde diversas pessoas estão trabalhando em diferentes partes do projeto e as atualizações podem ser trabalhadas através da implementação de Tags. Sendo assim possível uma melhor visualização do desenvolvimento das mudanças feitas no projeto. 


Espero ter ajudado um pouco em seu conhecimento. Obrigado por chegar até aqui, espero que tenhamos uma próxima vez. Obrigado
 

## Links Úteis
[Sintese Basica Markdow](https://www.markdownguide.org/basic-syntax/)

[Trabalhando com Bare](https://www.geeksforgeeks.org/working-with-git-repositories/)
