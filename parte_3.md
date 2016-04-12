## Parte 3 - Mão na Massa!
Agora que já está tudo configurado e você já sabe alguma operações do Ruby (uhul!), vamos fazer algo na prática!

> **Dica** → Enquando você segue as instruções, tente escrever o código ao invés de copiar e colar. Isso vai ajudar a memorizar os comandos mais facilmente.

#### Rodando um programa Ruby

1. Na linha de comando, digite o seguinte:
`atom meus_programas/primeiro_programa.rb`. O Atom deve abrir com um arquivo em branco.

2. Escreva o seguinte texto no arquivo:
  ``` ruby
  # encoding: utf-8
  puts "Bem-vinda!"
  ```
  A primeira linha é para permitir acentos e caracteres especiais no nosso programa. A segunda linha é um comando que deve imprimir a mensagem *Bem-vinda!*.
3. Salve o arquivo.

4. Volte para a linha de comando e rode `ruby meus_programas/primeiro_programa.rb`. Está vendo a mensagem que você digitou? Você rodou seu primeiro programa! =)

#### Interagindo com a usuária

1. No Atom, adicione as seguintes linhas no seu programa:

	```ruby
	puts "Qual é seu nome?"
	nome = gets.chomp
	```

2. Salve o arquivo.

3. Rode o programa novamente (digitando `ruby meus_programas/primeiro_programa.rb` na linha de comando) e veja o que acontece. A linha de comando está esperando um *input* da usuária. Teste você mesma! Digite seu nome e aperte *Enter*.

4. Agora vamos usar o nome que a usuária nos deu! No seu programa, adicione o seguinte:
	``` ruby
	puts "Olá, #{nome}!"
	```
	Com isso, estamos usando a palavra que armazenamos na **variável** *nome*.

5. Salve seu programa e volte para a linha de comando para rodar ele. Veja o que acontece quando você executa o programa e digite um nome. Legal, né? Vamos continuar!

#### Criando uma calculadora de tempo

Você quer saber quantos dias faltam para o seu próximo aniversário? Ou quantos dias faltam para acabar o ano? Podemos fazer nosso programa calcular isso! Veja
como:

1. Adicione o seguinte na segunda linha do seu programa:
	``` ruby
	require 'date'
	```
	Isso vai permitir que nós usemos os recursos de datas do Ruby.

2. Adicione as linhas abaixo no seu programa:
	``` ruby
	puts "Qual é o nome do evento que deseja saber se está perto?"
	nome_evento = gets.chomp
	puts "Que dia vai acontecer o evento #{nome_evento}?"
	data = gets.chomp
	```
	Agora estamos armazenando o nome do evento e em que dia esse evento vai acontecer. Note que já avisamos qual é o formato de data esperado para nossos usuários, assim fica mais fácil de evitar erros.

	Nesse ponto, seu arquivo deve estar assim:

	``` ruby
	# encoding: utf-8
	require 'date'

	puts "Bem-vinda!"

	puts "Qual é seu nome?"
	nome = gets.chomp
	puts "Olá, #{nome}!"

	puts "Qual é o nome do evento que deseja saber se está perto?"
	nome_evento = gets.chomp
	puts "Que dia vai acontecer o evento #{nome_evento}?"
	data_evento = gets.chomp
	```
	> **Dica** → As linhas em branco não fazem diferença para o funcionamento do programa, mas elas ajudam muito na organização do código. Fica bem mais fácil de ler.

3. Vamos calcular o tempo restante! Adicione mais essas linhas no final do arquivo:
	``` ruby
	data = Date.strptime(data_evento, '%d/%m/%Y')
	dias_restantes = (data - Date.today).to_i
	puts "Faltam #{dias_restantes} dias para #{nome_evento}!"
	```
	A primeira linha cria uma variável com o texto que a usuária nos deu transformado em algo que o computador entende como data. A segunda linha calcula a diferença entre o dia de hoje e o dia do evento. O `.to_i` transforma essa diferença em um número inteiro. Você consegue deduzir o que a terceira linha faz?

4. Salve o programa e rode. Quando o programa pedir, digite a data do seu
próximo aniversário, por exemplo. Rode de novo com outras datas.

Hora do próximo passo!

#### Utilizando condicionais

Observe que se quem estiver utilizando nosso programa colocar uma data distante, o número de dias não é o ideal para calcular o tempo. Para melhorar isso, podemos mostrar esse tempo em meses ao invés de usar dias. Veja como:

1. Substitua a linha `puts "Faltam #{dias_restantes.to_i} dias para #{nome_evento}!"` pelo seguinte código:

	``` ruby
	if dias_restantes < 31
	  puts "Faltam #{dias_restantes} dias para #{nome_evento}!"
	end
	```
	O comando `if` vai impor uma condição para o código ser rodado. No nosso caso, o programa vai verificar se a quantidade de dias é menor que 30 e, somente se for, vai imprimir a mensagem.
	
2. Salve e rode o programa. Para testar, digite uma data que acontecerá em menos de um mês. Rode novamente com uma data superior a 30 dias.

3. Para rodar um comando quando um valor não satisfaz a condição, vamos usar o `else`. Troque o código adicionado no passo 1 pelo seguinte:

	``` ruby
	if dias_restantes < 31
	  puts "Faltam #{dias_restantes} dias para #{nome_evento}!"
	else
	  meses_restantes = dias_restantes/30
	  puts "Faltam #{meses_restantes} dias para #{nome_evento}!"
	end
	```
	Agora sim! Quando a quantidade de dias restantes não for menor que 31, vamos dar a informação em meses.
4. Salve e rode o programa várias vezes, com datas diferentes.

Uhuuuul! Você terminou seu primeiro programa!