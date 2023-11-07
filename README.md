# Git e Github - Branching Conflitos Pull Requests

## Referência
https://cursos.alura.com.br/course/git-github-branching-conflitos-pull-requests/task/57959

## Github Issues
Recurso para colaborar com projetos opensource no Github, onde se pode reportar falhas ou bugs, fazer sugestões, sugerir melhorias e etc. Pode se organizar qualquer coisa referente ao projeto utiliando issues.

## Git Poll Requests
Para uma gerenciamento de qualidade dos repositórios, onde os colaboradores do repositório, criam forks do projeto para poder trabalhar em issues ou colaboração e ao final da entrega, solicitam um Pull Request aos Administradores ou Gestores ou Mantenedores do Repositório da projeto.

    # Fluxo ex.:
    > Um colaborador do projeto (repositório), deseja colaborar em uma issue;
    > Este colaborador cria um Fork do projeto para sua conta no Github;
    > Este colaborador trabalha na solução;
    > Ao final da solução, faz os commits necessários e sobe para o Github;
    > No Github solicita o Pull Request;
    > Um dos administradores do projeto analisam o Pull request através das commits feitas;
    > Este administrador decide se esta ok ou não, estando ok ele aceita o Pull Reques;
    > Este adminstrador fecha a issue informando qual Pull Request trabalhou na solução.

## Consolidando commits
    # Para consolidar em apenas um os 3 ultimos commits
    > git rebase -i HEAD~3

    # Para consolidadar commits pelo ID
    > git rebase -i <idcommitfinal>~<idcommitinicial>

> Consolidar commits é uma boa prática, para eliminar commits que não precisam ser documentados e facilitar a avaliação de pull requests.

## Git Cherry-pick
Para trazer um commit para a branch que esta trabalhando, a atual.

    > git cherry-pick <id do commit que quer juntar a branch>

> Normalmente utilizado, quando precisamos corrigir um bug trabalhado e corrigido em outra branch diferente da master ou main.

## Git Bisect
Para localizar em que momento algo foi alterado entre os commits, ou seja, encontrar em qual commit um bug foi introduzido.

    Iniciar a busca
    > git bisect start
    > git bisect bad HEAD
    > git log --oneline
    > git bisect good <id do commit onde o cod estava bom>
    # Confira no código que está bom
    > git bisec good
    # Confira no código que está ruim
    > git bisect bad
    # Note no código que o git encontrou o commit do mal
    > git bisect reset
    # Confira quando foi alterado
    > git show <id do commit informado pelo git>
    # Para reverter para o commit correto
    > git revert <id commit correto>


## Git Blame
Para localizar "culpados" de alterações no código

    > git blame <arquivo>

> O Git Blame vai mostrar linha por linha do arquivo e quem a alterou.

> A melhor prática não é encontrar pessoas culpadas, mais sim o motivos culpados para trabalhar na melhoria. Ou então até entender que temos um intruso fazendo alterações indevidas.

## Git Show
Para mostrar todas alterações em um arquivo

    > git show <arquivo>

## Dicas e Truques

    # Para visualizar de forma grafica a linha de desenvolvimento
    > git log --graph

## Git Flow
Um método template para organizar as branches quando ser tralha em equipes, principalmente grandes equipes.

> https://www.alura.com.br/artigos/git-flow-o-que-e-como-quando-utilizar

## Boas Práticas
- É uma convensão que a Master tenha apenas os commits prontos para ir para produção;
- Não é interessante realizar trabalho e commit diretamente na Master;
- É uma boa prátiva termos uma branch de Desenvolvimento;
- Outra boa prática que cada funcionalidade seja trabalhada em uma branch separada;
- É comum ter "feature/" como prefixo do nome das branches de funcionalidades, assim como "hotfix/" nas de bugs;
- As branches de Release são criadas para testar e corrigir bugs.

## Git Branch

    # Remover Branch
    > git branch -d <nome da branch>

    # Remover Branch ignorando commits que não estão na atual
    > git branch -D <nome da branch>

## Git Gui
Ferramentas Cliente com interface gráficas para Git

    https://git-scm.com/downloads/guis

    Sugestão
    https://www.gitkraken.com/

## Git Hooks
Permite executar algum código quando um determinando evento acontece.

    > em .git
    > em hooks
    > Shell Scripts

## Além do Github
Abaixo outras ferramentas de repositório remoto online:

- https://bitbucket.org/
- https://gitlab.com/

## Material Complementar

> http://slides.com/daianealvesrj/software-livre-para-empreendedores

> https://help.github.com/en/articles/closing-issues-using-keywords


