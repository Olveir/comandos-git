# Comandos Git

Esse documento é uma lista dos comandos básicos de Git, contendo uma explicação breve da funcionalidade de cada um.

## Como criar um repositório localmente

1. `git init`

    Inicia um repositório localmente a partir de uma pasta. Esse comando é usado ao iniciar novos projetos localmente. 
    
    Para conseguir colocar os dados e arquivos locais em um repositório remoto, é necessario criar um local remoto no GitHub e conectar o repositório local ao remoto do GitHub.
<br><br>

2. `git remote add origin {url}`

    Esse comando é usado para conectar um repositório local com um repositório remoto. 
    
    É necessário que seja passado a url do repositório remoto.

## Como copiar um repositório remoto

1. ``git clone {url}``

    git clone: Clona (copia) um repositório remoto para uma pasta/diretório de seu computador. Ao clonar um repositório irá ser criada uma pasta localmente com o nome do seu repositório. Não é necessário iniciar o git nessa pasta, pois ele já vai estar ativado. 

    A clonagem necessita da url ou de uma chave SSH do repositório.

## Como lidar com alterações em um repositório

1. `git status`

    Exibe o estado atual do diretório de trabalho e da área de preparação. Mostra todos os arquivos que foram adicionados ou alterados e o estado atual da branch.
<br><br>

2. `git add`

    Adiciona arquivos novos ou alterados do diretório de trabalho para a área de preparação, onde todos arquivos que estiverem staged, na área de preparação, vão ser incluidos no próximo commit. 

    Esse comando possui diversos parâmetros que definem a pasta ou arquivo a serem colocados na Staging Area. Abaixo está algum deles:

        'git add .'  -> Adiciona todas as alterações do seu diretório de trabalho atual e subdiretórios.

        'git add main.py' -> Adiciona somente o arquivo citado. No caso se tivesse 10 arquivos diferentes, somente o arquivo "main.py" seria adicionado.

        'git add Desktop/' -> Adiciona todas as alterações de um diretório de trabalho específico.
<br>

3. `git commit`

    Salva todas os arquivos dentro da Staging Area e cria um ponto de salvamento do projeto. Contêm as mudanças exatas que foram salvas, metadados e uma mensagem.

    A mensagem do commit é importante para saber o quê estava nesse commit e o porquê do mesmo. 

        'git commit -m "Mensagem descritiva"'
<br>

4. `git push`

    Esse comando envia as alterações salvas do repositório local para o repositório remoto.

    Sintaxe comum:

        'git push <remote> <branch>'
        
    'remote' -> Nome do repositório remoto. Por padrão esse nome é "origin".
    
    'branch' -> Nome do "ramo" de desenvolvimento. A branch principal costuma ter o nome de "main" ou "master".

    Assim formando o comando:

        'git push origin main'
<br>

5. `git pull`

    "Puxa" todas as alterações feitas no repositório remoto para atualizar o repositório local.
    
    É usado em casos em que os arquivos do repositório remoto foi alterado e os mesmos arquivos localmente estão desatualizados.
<br><br>

6. `git branch`

    É uma linha do tempo paralela e independente que se ramifica a partir da linha principal (branch main). 

    É usada para que uma alteração não seja inserida diretamente na linha principal, permitindo a análise e correção da alteração, para que não afete o funcionamento estável do arquivo.

    O comando pode ser usado de diferente formas fornecendo diferentes funcionalidades, sendo elas:

        'git branch' -> Lista todas as branches existentes no repositório local.

        'git branch <nome-da-branch>' ->  Cria uma nova branch, do ponto exato da branch atual.
<br>

7. `git checkout`

    É usado para mudar de branches. 

    O comando básico permite que você altere entre as branches existentes no repositório local, sendo ele: 

        'git checkout <nome-da-branch>'

        'git checkout ajuste_pagamento'

    Assim, toda alteração realizada será registrada na linha do tempo da branch "ajuste_pagamento" sem alterar nenhuma outra branch.
    <br><br>
    Esse comando possui um atalho que permite que você crie uma branch e mude para ele imediatamente em um passo só.
    
        'git checkout -b ajuste_relatorios'
    
