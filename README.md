**<h1> Git & GitHub (DIO) </h1>**
Durante o Bootcamp da <a href="https://web.dio.me/tracks" taget = "_blank">Digital Innovation One</a> foram ministradas aulas sobre o funcionamento do Git e do GutHub e proposto um desafio: Criar seu repositório no GitHub e subir arquivos para o mesmo levando em conta as aulas de "Introdução ao Git e ao GitHub" ministradas pelo professor Otávio Reis.

##

**<h2>Introdução ao Git</h2>**

GIT é um sistema de versionamento de código destribuído. Foi criado por Linus Torvalds, em 2005;
Não Possui uma interface Gráfica (CLI), podendo interagir somente por linha de comando;
  
`Comandos para usuários do Windows:`
  
  <ul>
<li> cd(navegar entre as pastas) </li>
<li> dir (listar; se situar dentro do sistema computacional) </li>
<li> mkdir(criar pasta) </li>
<li> del / rmdir(remover arquivos \ remover respositório) </li>
<li> cls (limpar a tela) </li>
</ul>

`Comandos Para Usuários do Linux:`

<ul>
<li> cd(navegar entre as pastas) </li>
<li> ls (listar; se situar dentro do sistema computacional) </li>
<li> mkdir(criar pasta) </li>
<li> rm -rf (remover arquivos \ remover respositório) </li>
<li> clear (limpar a tela) </li>
  </ul>
  

## Tópicos fundamentais para entender o funcionamento do Git

- SHA1

Algorítmo de Encriptação. O Algoritmo pega o arquivo e o embaralha de maneira específica. Essa encriptação gera um conjunto de caracteres de 40 dígitos.

##

-  <h2>Objetos fundamentais</h2>

1. BLOBS

Onde os arquivos ficam guardados. 

Estrutura do blob: Tipo do objeto + tamanho do objeto + \0 + conteúdo do arquivo.

2. TREES

Armazena blobs. 

Estrutura: Tipo do objeto + tamanho do objeto + \0 + blob + sha1 + nome do arquivo.

Diferentemento da blob, a árvore guarda o nome do arquivo e podem apontar tanto para blobs ou para outras árvores.

3. COMMITS

É possivel escrever uma mensagem nesse objeto que estará explicando os arquivos da pasta.

Estrutura: Tipo do objeto + tamanho do objeto + árvore + parente (ou seja, último commit realizado) + autor + mensagem + timestamp (arquivo de tempo)

 ## Porque o Git é um sistema ditribuído e seguro?
 
 - Chave SSH

Estabelece uma conexão segura e encriptada entre duas máquinas. 

Conexão estabelecida com duas chaves, sendo uma pública e outra privada.

- Gerar Chave no Git Bash:

passo 1: ssh-keygen -t ed25519 -C email@gmail.com
passo 2: selecionar pasta que deseja salvar e a senha
passo 3: localizar na pasta -> cd /c/Users/...
passo 4: cat id_ed25519.pub

- Gerar Chave no GitHub:

Settings > SSH and GPC keys > New SSH key > colar a chave que o git bash retornou após o último passo.

- GitBash (De Novo)

`passo 1:`

input:  eval $(ssh-agent -s)

output: Agent pid 999

`passo 2:`

input: ssh-add id_ed25519

output: Enter passphrase for id_ed25519:

input: senha definida anteriormente

output: id_ed25519 (email@gmail.com)

- Clonar projeto

No github: copiar SSH do projeto


##

<h3>Alguns Comandos no Git</h3>

- Clonar Projeto:

No gitbash: `git clone git@github.com:Oliveira/foodfy.git`
ou seja, git clone + SSH do projeto

- Iniciar GIT

`git init` (inicializa um repositório)
`git add` (passa o arquivo de untracked para tracked - staged) 
`git commit` <br>

Ummodified - arquivo que não sofreu modificação
Modified - arquivo que foi modificado
Staged - esperando para ser manipulado

 - Resolvendo conflitos

`git add.` 
`git commit -a`
`git pull origin main`
`git push origin main`

## Links úteis

<a href="https://git-scm.com/downloads" target="_blank">Instalação do Git</a>

<a href="https://github.com/" target="_blank">GitHub</a>

<a href="https://web.dio.me/track/html-web-developer?tab=path" target="_blank"> Bootcamp HTML Developer DIO</a>
