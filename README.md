# Estudos-SICP
Repositório direcionado aos estudos do Livro Structure &amp; Interpretation of Computer Programs

## Como Instalar o LISP em seu computador Windows
LISP possui diversas implementações. Focaremos nossos estudos de algoritmos usando o LISP-Scheme-Racket, uma sub-implementação de Scheme. Para fazer o download dos binários do Racket, acesse este link: [Racket-Lang](https://racket-lang.org/download/).

A instalação é bastante simples, ocorre através de um instalador do tipo .exe. Apenas clique next, next, next e finish.

É iniciar o racket através do próprio executável, o qual iniciará uma linha de comando com um REPL (Read-Eval-Print-Loop). Se preferir uma interface mais amigável, você pode rodar a IDE Dr.Racket e carregar a linguagem Scheme-Racket como padrão de implementação.

## Como Instalar o Scheme-Racket no Linux / WSL 
A instalação do Racket do Linux ou WSL é feita através do seguinte comando, de acordo com a versão desejada da linguagem:

> wget -P ~/diretorio/de/instalacao/ https://download.racket-lang.org/releases/8.11.1/installers/racket-8.11.1-x86_64-linux-cs.sh

Terminado o download, execute o script recém baixado:
> sudo sh racket-x.yy.z-x86_64-linux-cs.sh

Um menu será aberto, perguntando se o usuário deseja um instalação dessa distribuição em estilo Unix, atribuindo à cada binário um diretório específico no sistema; comumente, opta-se por não escolher esse caminho para instalar o Racket. A maneira mais conveniente é negar essa sugestão e manter todos os arquivos em um mesmo diretório, tornando possível a instalação de múltiplas versões e implementações do LISP e do Scheme.

Num segundo passo, é solicitado ao usuário um diretório no qual a versão do Racket será instalado, no meu caso, escolherei: "/usr/racket".

Para finalizar a instalação, exporte o diretório com os binários do Scheme-Racket para as variáveis de ambiente $PATH. Para isso, abra o arquivo de configuração **rc** que se adeque ao seu cenário, no meu caso, é o arquivo **".zshrc"**, referente ao zshell:

> nano ~/.zshrc

Ao final do arquivo, adicione a linha:

```shell
export PATH="$PATH:/usr/racket/bin/"
```

Para testar o funcionamento de qualquer binário racket, você pode, assim como na instalação pelo sistema operacional Windows, invocar o executável *racket* pela linha de comando; habilitando a CLI-REPL. Caso queira iniciar a IDE Dr. Racket, invoque o *drracket*.