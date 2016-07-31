Discente: Victor Deluca Almirante Gomes


Algumas das soluções incluem códigos de programas em linguagens de programação diversas. Para executar esses códigos, siga as
instruções a seguir:
- Acesse o site: https://ideone.com/
- Logo abaixo da caixa onde está escrito "enter input (stdin)", no canto inferior esquerdo, há um pequeno botão onde você pode
selecionar a linguagem de programação que desejar. Escolha a opção "Haskell".
- Copie e cole o código na grande caixa de texto onde você pode ler "enter your source code or insert template or sample or
your template". Caso o usuário precise digitar algum input, a solução incluirá um exemplo de input. Digite-o na caixa, abaixo
da mensagem "enter input (stdin)" e selecione a opção "Run", no canto inferior direito. Tenha cuidado especial com os códigos
em Haskell, pois qualquer input a menos ou a mais poderá ocasionar um Runtime Error. Nem todos os programas necessitarão de um
input.



1) 
Programação funcional é um paradigma de programação especificamente orientado ao uso de funções (É importante não confundir
paradigma de programação com linguagem de programação), o que significa que o programador não dá 'comandos', mas chama 'funções'
que receberão 'argumentos' e darão um 'retorno' ao usuário. É possível programar funcionalmente em diversas linguagens (Programar
funcionalmente em C++, quem diria?), mas existem linguagens que foram criadas especificamente com esse paradigma em mente, e 
estas são chamadas linguagens funcionais. São exemplos o Haskell, Scala e F#.
Entre as vantagens estão a vasta capacidade de manutenção e reutilização de código proveniente das funções. Paralelização e 
concorrência de código também são mais simples na programação funcional. As desvantagens envolvem performance inferior e dificuldade
de prever requisitos do programa, em comparação com outros paradigmas.





2) 
- Característica 1: Funções puras: Se uma função for chamada múltiplas vezes com os mesmos argumentos, ela sempre irá retornar o
mesmo valor.
--------------------------------------------------------------
Demonstração:
--------------------------------------------------------------
soma a b = a + b

main = do
	print(soma 1 5)
	print(soma 1 5)
	print ("Oi")
	print(soma 1 5)
--------------------------------------------------------------
Input: Inexistente
Output: 
6
6
"Oi"
6
--------------------------------------------------------------
Como podemos ver, a função foi chamada múltiplas vezes utilizando os números 1 e 5 como argumentos, e em todas elas o resultado
retornado foi o número 6.
--------------------------------------------------------------
- Característica 2: Funções de ordem maior: Funções podem retornar funções e receber funções como argumentos.
--------------------------------------------------------------
Demonstração:
--------------------------------------------------------------
soma a b = a + b
tenmult a b = (soma a b) * 10

main = do
	print(tenmult (soma 1 10) (soma 1 5))
--------------------------------------------------------------
Input: Inexistente
Output: 
60
--------------------------------------------------------------
Onde tenmult recebe como argumentos as funções "soma 1 10" e "soma 1 5" e retorna a soma de ambas as funções multiplicada por 10,
demonstrando que as funções podem receber outras funções como argumentos e retornar outras funções também.
--------------------------------------------------------------
- Característica 3: Estados imutáveis: Uma vez que o valor de uma variável for definido ele não pode ser modificado. O programa
não deve ter efeitos colaterais.
--------------------------------------------------------------
Demonstração:
--------------------------------------------------------------
p = sum[2,4,5,6]
p = 15

main = do
	print p
--------------------------------------------------------------
Input: Inexistente
Output:
Compilation error	time: 0 memory: 4652 signal:0
[1 of 1] Compiling Main             ( prog.hs, prog.o )

prog.hs:2:1:
    Multiple declarations of `p'
    Declared at: prog.hs:1:1
				 prog.hs:2:1
				
Compilation error	time: 0 memory: 4652 signal:0
[1 of 1] Compiling Main             ( prog.hs, prog.o )

prog.hs:2:1:
    Multiple declarations of `p'
    Declared at: prog.hs:1:1
                 prog.hs:2:1
--------------------------------------------------------------
Como podemos ver, o programa simplesmente não compila, alegando múltiplas declarações de 'p'. É possível contornar isso
utilizando a linha de código "let p = 15" no Main, por algum motivo, mas a princípio as variáveis são imutáveis.
--------------------------------------------------------------
- Característica 4: Composição de funções: A partir de duas funções é possível gerar uma nova função que executa as duas
de forma simultânea.
--------------------------------------------------------------
Demonstração:
--------------------------------------------------------------
soma a b = a + b
multi a b = a * b
elegantsum a b = ((soma a b)+(multi a b)+(soma a b))

main = do
	print (elegantsum 5 5)
--------------------------------------------------------------
Input: Inexistente
Output: 
45
--------------------------------------------------------------
Onde a função "elegantsum" executa as funções "soma" e "multi" ao mesmo tempo.
--------------------------------------------------------------





3)
- O Facebook utiliza programação funcional para as mais variadas funções, no entanto uma dessas funções é mencionada muito mais
 frequentemente do que as outras. Trata-se do Sigma, uma ferramenta de segurança do Facebook feita em Haskell que combate spam, 
 malware e outros tipos de mensagens nocivas (Que infelizmente não incluem conteúdo ofensivo), os deletando automaticamente caso
 sejam detectados.

- O Twitter utiliza amplamente a linguagem Scala, e o Github do Twitter possui um arquivo de texto relativamente extenso
 descrevendo detalhadamente o seu uso da linguagem, mas trazê-lo para este texto seria um exagero, para dizer o mínimo: Basta
 dizer que Scala é uma das linguagens de programação principais do site, utilizada em GRANDE parte de suas funcionalidades.

- A Netflix possui uma política interessante que permite aos seus desenvolvedores escolherem livremente a linguagem de programação
 que eles julgarem mais apropriada para seus projetos. Alguns desses desenvolvedores optaram pela linguagem Scala, e, embora alguns
 desses projetos tenham simplesmente desaparecido ou simplesmente não tenham recebido destaque suficiente para serem mencionados 
 constantemente, o projeto Atlas (Que consiste em um sistema de monitoramento em tempo real) continua em andamento e seu repositório
 no Github é constantemente atualizado.
 
 
 
4)
Orientação a objetos define um paradigma de programação que vê o programa como uma coleção de objetos interconectados. Esses objetos 
possuem "atributos" e "métodos", onde podemos definir atributos como características que o objeto possui e métodos como ações que o 
objeto é capaz de executar. Entre as vantagens trazidas com o seu uso estão a melhoria da interação entre analistas e especialistas,
a legibilidade do código e, de uma forma geral, a facilidade de compreender e visualizar o programa em prática, uma vez que a orientação
a objetos se aproxima mais da vida real do que os outros paradigmas.




5)
int year;
String make;
double speed;

São variáveis primitivas cujo escopo é a classe Car.

int y, String m, double beginningSpeed

São variáveis primitivas cujo escopo é o método Car().

int tmp = year;

É uma variável primitiva cujo escopo é o método getYear().

Roda r = new Roda(tmp);

É um objeto cujo escopo é o método getYear().

 
 
 
 6)
 - Ao executar o techo de código "*b++ = 0;", o valor de b (Que é um endereço de memória) aumenta, e o seu novo valor passa a não ser
 mais um endereço alocado dinamicamente, tornando o free(b) completamente inútil e gerando um Runtime Error (Que ocorre quando o programa
 acessa um endereço de memória inválido).
 
 
 
 
7)
a)
--------------------------------------------------------------------------------------------------------------
Haskell
--------------------------------------------------------------------------------------------------------------
main = do
	inputjar <- getLine
	let n1 = read inputjar::Double
	inputjar <- getLine
	let n2 = read inputjar::Double
	inputjar <- getLine
	let n3 = read inputjar::Double
	inputjar <- getLine
	let n4 = read inputjar::Double
	let media = (n1+n2+n3+n4)/4
	if media>=7 then do
		print("Aluno Aprovado")
		print(media)
	else do
		inputjar <- getLine
		let ex = read inputjar::Double
		let fin = (media+ex)/2
		if fin>=5 then do 
			print("Aluno Aprovado em Exame")
			print(fin)
		else do
			print("Aluno Reprovado")
			print(fin)
--------------------------------------------------------------------------------------------------------------
Exemplo de input:
7.0
5.0
1.0
3.0
9.0
Exemplo de output:
"Aluno Aprovado em Exame"
6.5


Exemplo de input:
7.0
5.0
1.0
3.0
1.0
Exemplo de output:
"Aluno Reprovado"
2.5
--------------------------------------------------------------------------------------------------------------
b)
--------------------------------------------------------------------------------------------------------------
Haskell
--------------------------------------------------------------------------------------------------------------
main = do
	inputjar <- getLine
	let n1 = read inputjar::Int
	if n1 `mod` 2 == 0 then print("Par")
	else print("Impar")
--------------------------------------------------------------------------------------------------------------
Exemplo de input:
4
Exemplo de output:
"Par"

Exemplo de input:
5
Exemplo de output:
"Impar"
--------------------------------------------------------------------------------------------------------------
 
 
 
c) 
--------------------------------------------------------------------------------------------------------------
Haskell
--------------------------------------------------------------------------------------------------------------
Nota: Embora o enunciado das próximas questões cobre apenas as funções, eu resolvi colocar uma aplicação delas no Main, para
a solução ficar mais completa.
--------------------------------------------------------------------------------------------------------------
srt::(Ord a)=>[a]->[a]
srt[]=[]
srt lista=srt1 lista(length lista)

srt1::(Ord a)=>[a]->Int->[a]
srt1 lista 0=lista
srt1 lista n=srt1(swp lista)(n-1)

swp::(Ord a)=>[a]->[a]
swp[x]=[x]
swp(x:y:zs)
	|x>y=y:swp(x:zs)
    |otherwise=x:swp(y:zs)

main = do 
	let k=[1,7,6,8,40,-45,3]
	let m=srt(k)
	print("Array normal")
	print(k)
	print("Array ordenada")
	print(m)
-----------------------------------------------------------------------------------------------------------------------
Input: Inexistente
Output:
"Array normal"
[1,7,6,8,40,-45,3]
"Array ordenada"
[-45,1,3,6,7,8,40]
-----------------------------------------------------------------------------------------------------------------------

	
	
d)
------------------------------------------------------------------------------------------------------------------------
Haskell
------------------------------------------------------------------------------------------------------------------------
maxi [x] = x  
maxi (x:xs)   
    | x > maxi xs = x  
    | otherwise = maxi xs
mini [x] = x
mini (x:xs)
	| x < mini xs = x
	| otherwise = mini xs

main = do 
	let k = [1,7,6,8,40,-45,3]
	let m = maxi k
	let n = mini k
	print("O maior dentre os numeros abaixo:")
	print(k)
	print("E o numero")
	print(m)
	print("E o menor e o numero")
	print(n)
-------------------------------------------------------------------------------------------------------------------------
Input: Inexistente
Output:
"O maior dentre os numeros abaixo:"
[1,7,6,8,40,-45,3]
"E o numero"
40
"E o menor e o numero"
-45
-------------------------------------------------------------------------------------------------------------------------
