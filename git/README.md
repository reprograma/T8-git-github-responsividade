# Git

O git é uma ferramenta da linha de coamndo para controle de versão de arquivos. 
É bastante usado por times de desenvolvedores para facilitar o trabalho 
paralelo de vários desenvolvedores no mesmo projeto, auxiliar no encontro 
de bugs e regressões, manter documentação do histórico do projeto, entre outros.

> [site do git](https://git-scm.com/)

### Comandos

Todas as funcionalidades do git podem ser acessadas pela linha de comando de
um computador que tenha o git instalado. Para ver uma lista dos comando principais
do git, digite `git` ou `git --help` na sua linha de comando e aperte o Enter.

##### Nota sobre comandos

Uma ferramenta da linha de comando é um software que não tem interface gráfica.
Todas as suas funcionalidades devem ser acessadas através de comandos específicos
a serem executados diretamente pela linha de comando de um computador.

Veja alguns comando nativos e importantes de sistemas que seguem a especificação 
[UNIX](https://pt.wikipedia.org/wiki/Unix):

- `ls` - *list* lista todos os arquivos e pastas dentro da pasta atual
- `cd <caminho relativo de outro diretório>` - *change directory* muda o
estado atual da linha de comando para outro diretório
- `man <comando>` - *manual* se existir, renderiza a página de manual de 
algum outro comando

##### Anatomia de um comando

- **comando**: o primeiro termo de qualquer comando é o nome do programa
que você deseja executar. Exemplo:

```bash
whoami
```

O programa `whoami`, retorna o nome do atual usuário logado no computador.

- **opções**: opções servem como modificadores de um comando. Elas podem
começar com um ou mais `-`. Exemplo:

```bash
ls -a
```

O programa `ls`, lista todos os arquivos e pastas dentro da pasta atual.
Quando seguido da opção `-a` ele lista também os arquivos e pastas cujos
nomes começam com um `.`.

- **argumentos**: muitas vezes, os comando precisam receber argumentos para
saberem como ou em que devem agir.

```bash
ping google.com
```

O programa `ping` faz um teste de conexão entre o computador local e um
computador remoto. Para poder fazer esse teste, ele precisa receber como
argumento o endereço do computador remoto que precisa testar.

> Este programa roda infinitamente, e enquanto está rodando não permite
ao usuário usar a linha de comando. Para pausar a execução deste e de outros
programas na linha de comando, basta teclar `ctrl + c`.

> Opções podem receber argumentos também, basta que o argumento venha
imediatamente depois da opção. Exemplo:

```bash
curl google.com --output google.html
```

O programa `curl` pode ser usado para transferir dados de ou para um 
servidor. Neste exemplo, usamos o `curl` para acessar o site **google.com**
e usamos a opção `--output` para salvar os dados recebidos dentro de um 
arquivo que chamamos de `google.html`.

##### Os comandos do git

- `git init`: inicializa um novo repositório do git dentro da pasta atual.

- `git config`: modifica o arquivo de configurações do git (`.gitconfig`).
Entre outras coisas o arquivo de confirações do git, contém informações 
como o nome e o email do atual usuário. Exemplo:

```bash
git config user.name "Beatriz Rizental"
git config user.email "beatriz.rizental@gmail.com"
```

- `git remote`: gerencia os links com repositórios remotos dentro do
repositório atual. Exemplo:

```bash
git remote -v
```

Lista os links com repositórios remotos dentro do repositório atual.

```bash
git remote add origin https://github.com/git/git.git
```

Adiciona um novo link para o repositório remoto, apontando para o endereço
`https://github.com/git/git.git` e com o nome de `origin`

- `git status`: mostra o estado dos arquivos e pastas dentro do atual 
repositório.

- `git add <caminho>`: adiciona a área de staging do git todos os arquivos
cujo ao caminho corresponda a `<caminho>`.

- `git commit`: cria um novo commit, com todos os arquivos que estejam
na área de staging do git. Este comando, irá abrir o [vim](https://www.vim.org/),
um editor de texto da linha de comando, para que você possa adicionar uma
mensagem descritiva a ele.

- `git log`: mostra o histórico de commits do atual repositório.

- `git push <remoto> <branch>`: envia commits divergentes para um repositório remoto.

- `git pull <remoto> <branch>`: pega commits divergentes de um repositório remoto.