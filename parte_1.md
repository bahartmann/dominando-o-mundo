# Parte 1 - Preparando o ambiente

Para começarmos a programar, vamos primeiro preparar nosso computador com as ferramentas necessárias. Nessa parte de configuração inical, é normal levar um tempinho a mais com as instalações. Se em alguma parte do processo as coisas não ocorrerem como o tutorial sugere ou você ficar trancada em alguma parte, peça ajuda! =)

## Linha de comando
A primeira ferramenta que vamos conhecer é a **linha de comando**, muito utilizada enquanto estamos programando. Ela permite controlar o computador de uma forma mais direta: usando apenas comandos!
Você já tem um programa no seu computador para usar a linha de comando. Siga as instruções para abri-lo de acordo com seu sistema operacional:

#### Windows
Vá em Iniciar → Todos os Programas → Acessórios → Prompt de comando

#### Mac OS X
Applications → Utilities → Terminal

#### Linux
Procure pelo programa *Terminal*. Provavelmente você o encontrará indo para Applications → Accessories → Terminal

Está vendo uma janela onde você pode digitar algum texto? Ótimo! Estamos prontas para continuar =)

> **Dica** → Para saber mais sobre a linha de comando, siga esse tutorial super legal e informativo: http://tutorial.djangogirls.org/pt/intro_to_command_line/index.html


## Ruby

Para programar, usamos uma *linguagem de programação*, que é um idioma que permite que a gente dê comandos para o computador. A linguagem que usaremos é **Ruby**, uma linguagem criada para ser fácil de usar =)

Para instalar Ruby no seu computador, siga as instruções de acordo com seu sistema operacional:

#### Windows
Primeiro, você deve saber se seu computador roda em 32 ou 64 bits. Veja como descobrir isso nessa página: http://windows.microsoft.com/pt-br/windows/32-bit-and-64-bit-windows#1TC=windows-7

 - Se seu computador é 32 bits, clique aqui:
   http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.2.4.exe
 - Se seu computador é 64 bits, clique aqui:
   http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.2.4-x64.exe

Quando você clicar no link, um download vai começar. Abra o arquivo baixado e siga as instruções de instalação.

#### Mac OS X
Você já possui Ruby instalado no seu computador! Não precisa fazer nada nesse passo.

#### Linux
Na linha de comando que mencionamos no último tópico, digite o seguinte comando: `sudo apt-get install` e aperte *Enter*. Você deverá digitar sua senha (a mesma que você usa para ligar o computador) e apertar *Enter*.

Para verificar se o Ruby está mesmo instalado, digite o comando `ruby -v` na linha de comando e aperte Enter. Você deve ver uma mensagem informando a versão do Ruby que você instalou, algo do tipo: `ruby 1.9.3p551`. Agora podemos usar Ruby!

## Editor de texto

Para que possamos escrever o código dos nossos programas, é preciso ter um bom editor de texto! Nosso editor de texto vai ser o Atom. Veja como ter o Atom no seu computador de acordo com seu sistema operacional:

#### Windows
Clique no link https://github.com/atom/atom/releases/download/v1.6.0/atom-windows.zip. Após o download terminar, descompacte o arquivo baixado, execute o arquivo e siga as instruções de instalação.

#### Mac OS X
Clique no link https://github.com/atom/atom/releases/download/v1.6.0/atom-mac.zip. Após o download terminar, clique no arquivo baixado e siga as instruções de instalação.

#### Linux
Na linha de comando, rode cada um dos seguintes comandos:

- `sudo add-apt-repository ppa:webupd8team/atom` + *Enter*
- `sudo apt-get update` + *Enter*
- `sudo apt-get install atom` + *Enter*

Depois de cada comando você deverá inserir sua senha (a mesma que você usar para ligar o computador).

Para ver se está tudo certo, abra o programa Atom. Tente fazer um novo arquivo e digitar. Funcionou? Vá para o próximo passo!


