# Indução Matemática e Complexidade de Algoritmos

---

**1°  Prove por indução matemática que a soma dos cubos dos n primeiros números inteiros positivos, n ≥ 1, é igual ao quadrado da soma destes números.**

Variável de Indução:

Inteiros positivos, $n \geq 1$.

Caso Base: 

$n = 0  \rightarrow 0^3 = (0)^2$

Hipótese de Indução: 

A propriedade é válida para $n = k \rightarrow 1³ + 2³ + ... + k ³ = (1 + 2 + ... + k)²$

Passo indutivo, para $n = k + 1$:

$$
S_{k+1} = 1³ + 2³ + ... + k ^3 + (k + 1)³
$$

Note que o termo $1³ + 2³ + ... + k ^3$ é nossa Hipótese Indutiva. Logo, podemos substituir seu valor na expressão acima. Assim:

$$
S_{k + 1} = (1 + 2 + ... + k)² + (k+1)³
$$

Podemos perceber que o valor da Hipótese Indutiva representa uma Progressão Aritmética. Portando, podemos substituir seu valor pela fórmula de uma PA de 1 à k:

$$
S_k = (1 + 2 + ... + k)² = \Bigg (\frac {(1 + k)k} {2} \Bigg )\raisebox{1.25em}{$2$} = \Bigg (\frac {k + k²} {2} \Bigg )\raisebox{1.25em}{$2$}
$$

Assim:

$$
S_{k+1} = \Bigg ( \frac {k + k²} {2} \Bigg )\raisebox{1.25em}{$2$} + (k+1)³
\\
⠀
\\
⠀⠀⠀⠀⠀ = \frac {k² + 2 k³ + k⁴} {4} + \frac {4(k+1)³} {4}
\\
⠀
\\
⠀⠀⠀⠀⠀= \frac {k⁴ + 6k³ + 13k² + 12k + 4} {4}
\\
⠀
\\

⠀⠀⠀⠀⠀= \frac {(k² + 4k + 4)(k² + 2k + 1)} {4}
\\
⠀
\\
⠀⠀⠀⠀⠀= \Bigg (\frac {(1 + (k+1))(k+1)} {2} \Bigg )\raisebox{1.25em}{$2$}
$$

Perceba que chegamos numa fórmula de PA de $k+ 1$ elementos, portando:

$$
S_{k+1} = \Bigg (\frac {(1 + (k+1))(k+1)} {2} \Bigg )\raisebox{1.25em}{$2$} = (1 + 2 + ... + k + (k+1))²
$$

Assim, chegamos ao resultado esperado e, supondo que a propriedade do enunciado é válida para $k$, então será verdadeira para o próximo elemento $k + 1$.

**2° Seja T uma árvore binária cheia de altura h, h ≥ 0. Prove por indução matemática que T tem $n = 2^{h+1} - 1$ nós. Uma árvore binária é dita cheia quando todos os nós de um nível ou são folhas ou possuem exatamente dois filhos.**

Variável de Indução:

Altura da Árvore, $h$.

Caso Base:

Sabemos que numa árvore cheia o número de nós da respectiva altura, $h$, é dada por: $2^h$. Então, a soma dessa propriedade aplicada em cada nível até a altura $h$ será igual à  $2^{h + 1} -1$. 

Para $h = 0 \rightarrow n = 2^{0+1} -1 = 2^0 = 1$

Assim, a propriedade é válida para o Caso Base.

Hipótese de Indução:

Supomos que tal propriedade é válida para uma árvore de altura $h = k$, logo:

$$
2^0 + 2^1 + ... + 2^k = 2^{k+1} - 1
$$

Caso Geral:

Assim, vamos tentar provar a propriedade para uma altura $k+1$. Dessa forma, esperamos chegar no resultado $2^{k + 2} -1$:

$$
S_{k+1} = 2^0 + 2^1 + ... + 2^k + 2^{k+1}
$$

Aplicando a Hipótese de Indução:

$$
S_{k+1} = 2^{k+1} - 1 + 2^{k + 1}
\\
⠀
\\
S_{k+1}= 2(2^{k+1}) - 1 = 2^{k+2} - 1
$$

Logo, chegamos ao resultado esperado e a propriedade provou-se verdadeira.

**3° Dado um vetor de inteiros de n elementos, elabore um algoritmo para determinar quantos destes números são negativos.**

Variável de Indução:

Quantidade de elementos, $n$.

Caso Base:

Lista vazia, $n = 0 \rightarrow$ retorna $0$.

Hipótese de Indução:

Sabemos resolver o problema para $k = n - 1$ elementos.

Caso geral:

Reservamos o primeiro elemento, comparamos se o mesmo é negativo e aplicamos a Hipótese de Indução no restante da lista.

Pseudo-código:

```
algoritmo neg_lista(l): Inteiro
{-
Entrada: Lista com números inteiros.
Saída: Inteiro representando a quantidade de números negativos que existem na lista.
-}
	início
		Se L = nulo, então -- Caso Base
			retorne 0
		Senão -- Caso Geral
			retorne eh_neg(l.first) + neg_lista(l.prox)
	fim
	
função eh_neg(elem): Inteiro
{-
	Entrada: Inteiro a ser analizado.
	Saída: 0, se o número for positivo, e 1 se o número for negativo.
-}
	inicio
		Se elem < 0, então
			retorne 1
		Senão
			retorne 0
	fim
```

Código:

```python
def neg_lista(lista):
  if lista == []:
    return 0
  else:
    return eh_neg(lista[0]) + neg_lista(lista[1:])

def eh_neg(elem):
  if elem < 0:
    return 1
  else:
    return 0

l = [1,2,-5,-8,23,-9,0,3,1,-1,-5,-7]
print(neg_lista(l), end='\n\n')
```

4**°  Dada uma árvore binária de inteiros e dois limites de intervalo, inferior e superior, determine a soma dos elementos da árvore que estão neste intervalo de valores (intervalo fechado).**

Variável de Indução:

Número de nós da Árvore, $n$.

Caso Base:

Árvore vazia, $n = 0 \rightarrow$  retorne $0$.

Altura atual é maior que o intervalo desejado $\rightarrow$ retorne $0$.

Hipótese de Indução: 

Sei resolver para uma árvore com $1 \leq k < n$.

Caso geral:

Dividiremos a árvore em subárvores cada vez menores, aplicaremos uma função auxiliar no Nó raiz da Árvore atual para verificar se o mesmo encontra-se no intervalo desejado, se sim retornamos o mesmo, caso não, retornamos $0$. Assim, aplicamos a Hipótese Indutiva.

Pseudo-código:

```
algoritmo sum_tree(root, altura, limite_inf, limite_sup): Inteiro
{-
	Entrada: Árvore Binária, sua Altura inicial (geralmente 0) 
					 e o limite inferior e superior desejado.  
	Saída: Número inteiro representado a soma dos 
				 elementos da Árvore no intervalo desejado.
-}
	inicio
	  Se root = Vazio || altura > lim_sup, então -- Caso Base
	    retorne 0
	  
	  Senão -- Caso Geral
	    retorne sum_n(root.key, altura, limite_inf, limite_sup) + 
							sum_tree(root.left, altura + 1, limite_inf, limite_sup) + 
							sum_tree(root.right, altura + 1, limite_inf, limite_sup)
	fim

função sum_n(key, altura, lim_inf, lim_sup): Inteiro
{-
	Entrada: Valor do Nó que deseja-se analisar, Altura atual 
					 e os limites inferior e superior desejado.
	Saída: 0, se o valor não estiver no intervalo correto, 
				 caso contrário retorna-se o valor do nó.
-}
	inicio
	  Se altura >= lim_inf && altura <= lim_sup, então
	    retorne key
	  Senão
	    retorne 0
	fim
```

Código:

```python
from binarytree import BinaryTree

tree = BinaryTree()

"""
       10
    5      13
  3  6   12  14
"""

tree.add(10)
tree.add(5)
tree.add(13)
tree.add(3)
tree.add(6)
tree.add(12)
tree.add(14)

def sum_tree(root, altura, lim_inf, lim_sup):
  if root == None or altura > lim_sup:
    return 0
  
  else:
    return sum_n(root.key, altura, lim_inf, lim_sup) + sum_tree(root.left, altura + 1, lim_inf, lim_sup) + sum_tree(root.right, altura + 1, lim_inf, lim_sup)

def sum_n(key, altura, lim_inf, lim_sup):
  if altura >= lim_inf and altura <= lim_sup:
    return key
  else:
    return 0

print(sum_tree(tree.r, 0, 0, 0), end='\n\n')
```

5**° Dados dois vetores de inteiros ordenados em ordem crescente, gere um terceiro vetor com os dados dos vetores de entrada também ordenados em ordem crescente, mas sem elementos repetidos.**

Ideia para solução:

Vamos passar os dois vetores como argumentos .

Primeiramente vemos qual dos vetores tem o menor último número, assim podemos criar um laço de repetição com esse vetor. Pois, ao terminar o laço irá sobrar elementos no segundo vetor e basta concatená-lo com o resultado. 

No laço de repetição criamos duas variáveis de posição. Inciamos comparando os elementos das posições dos vetores desejadas e dependendo do resultado aumentamos a variável de posição do vetor que acabamos de pegar o elemento. Caso o elemento exista nos dois vetores aumentamos a variável de posição de ambos os vetores. Assim, percorremos todo o menor vetor definido no começo do programa, restando apenas concatenar o restante do maior vetor ao resultado.

Pseudocódigo

```
algoritmo ord_vetor(vetor_a, vetor_b, tam_a, tam_b): Vetor de Inteiros
{-
	Entrada: Dois vetores de inteiros e seus respectivos tamanhos.
	Saída: Vetor contendo os elementos dos dois vetores ordenados. 
-}
	inicio
	  Se vetor_a = Vazio, então
	    retorne vetor_b
	  Se vetor_b = Vazio, então
	    retorne vetor_a
	  Se vetor_a[tam_a] < vetor_b[tam_b], então
	    menor := vetor_a
			len_menor := tam_a
			maior := vetor_b
			len_maior := tam_b
	  Senão
	    menor := vetor_b
			len_menor := tam_b
			maior := vetor_a
			len_maior := tam_a
	  
	  vetor_c := []
	  pos1 := 1
		pos2 := 1
	  Enquanto pos1 <= len_menor, faça
	    Se menor[pos1] < maior[pos2], então
	      vetor_c.append(menor[pos1])
	      pos1 := pos1 + 1
	    Se menor[pos1] > maior[pos2], então
	      vetor_c.append(maior[pos2])
	      pos2 := pos2 + 1
	    Senão
	      vetor_c.append(menor[pos1])
	      pos1 := pos1 + 1
	      pos2 := pos2 + 1
	  
	  retorne vetor_c + maior[pos2:]
	fim
```

Análise de Complexidade

$$
\textstyle\sum_{i=1}^n . 2 + 6n + \textstyle\sum_{i=1}^m = 2(n+1) + 6n + m = 8n + m + 2
\\
⠀
\\
Complexidade: O(n + m)
\\
⠀
\\
Espaço⠀gasto: O(n + m)
$$

Código:

```python
a = [1,2,4,5,10]
b = [4,5,6,9,11]

def ord_vetor(vetor_a, vetor_b):
  
  if vetor_a == []:
    return vetor_b
  elif vetor_b == []:
    return vetor_a
  elif vetor_a[-1]  < vetor_b[-1]:
    menor, maior = vetor_a, vetor_b
  else:
    menor, maior = vetor_b, vetor_a
  
  vetor_c = []
  pos1, pos2 = 0, 0
  while pos1 < len(menor):
    if menor[pos1] < maior[pos2]:
      vetor_c.append(menor[pos1])
      pos1 += 1
    elif menor[pos1] > maior[pos2]:
      vetor_c.append(maior[pos2])
      pos2 += 1 
    else:
      vetor_c.append(menor[pos1])
      pos1 += 1
      pos2 += 1
  
  return vetor_c + maior[pos2:]

print(ord_vetor(a,b), end='\n\n')
```

6**° Dados dois vetores de inteiros A e B, gere um terceiro vetor representando o vetor interseção dos vetores originais, nas duas situações abaixo. A solução para cada situação deve ser distinta, ou seja, você não pode reutilizar parte da solução de um item em outro item. O vetor de interseção não pode ter elementos duplicados.**

**a. A e B estão ordenados, em ordem decrescente**

Ideia para solução:

Nessa questão, adotamos uma estratégia similar a feita na questão anterior. Porém, dessa vez selecionamos o vetor que possui o maior último número. Assim, criaremos um laço de repetição com esse vetor. 

No laço de repetição comparamos os elementos e iremos aumentar as variáveis de posição dependendo do resultado da comparação, e só adicionaremos ao resultado se os elementos forem iguais.

Pseudocódigo:

```
algoritmo ord_intersec(vetor_a, vetor_b, tam_a, tam_b): Vetor de Inteiros
{-
	Entrada: Vetores de Inteiros e seus respectivos tamanhos
	Saída: Interseção ordenadas dos vetores
-}
	início
	  Se vetor_a = Vazio || vetor_b = Vazio, então
	    retorne Vazio
	  Se vetor_a[tam_a]  > vetor_b[tam_b], então
	    maior := vetor_a
			len_maior := tam_a
			menor := vetor_b
			len_menor := tam_b
	  else:
	    maior := vetor_b
			len_maior := tam_b
			menor := vetor_a
			len_menor := tam_a
	  
	  vetor_c := []
	  pos1 = 1
		pos2 = 1
	  Enquanto pos1 < len_maior, faça
	    Se maior[pos1] > menor[pos2], então
	      pos1 := pos1 + 1
	    Se maior[pos1] < menor[pos2], então
	      pos2 := pos2 + 1
	    else:
	      vetor_c.append(maior[pos1])
	      pos1 := pos1 + 1
	      pos2 := pos2 + 1
	  
	  retorne vetor_c
	fim
```

Análise de Complexidade:

$$
\textstyle\sum_{i=1}^n . 2 + 5n = 2(n+1) + 5n = 7n+2

\\
⠀
\\
Complexidade: O(n)

\\
⠀
\\
Espaço⠀gasto: O(n)
$$

Código:

```python
def ord_intersec(vetor_a, vetor_b):  
  if vetor_a == [] or vetor_b == []:
    return []
  elif vetor_a[-1]  > vetor_b[-1]:
    maior, menor = vetor_a, vetor_b
  else:
    maior, menor = vetor_b, vetor_a
  
  vetor_c = []
  pos1, pos2 = 0, 0
  while pos1 < len(maior):
    if maior[pos1] > menor[pos2]:
      pos1 += 1
    elif maior[pos1] < menor[pos2]:
      pos2 += 1 
    else:
      vetor_c.append(maior[pos1])
      pos1 += 1
      pos2 += 1
  
  return vetor_c

v_a = [10,6,4,2,1]
v_b = [11,9,6,5,4]

print(ord_intersec(v_a, v_b), end='\n\n')
```

**b. A e B estão em ordem arbitrária.**

Ideia para solução:

Para resolver essa questão, iremos verificar qual é o menor vetor em tamanho e criaremos um laço “for” com tal vetor, e dentro desse laço criaremos outro “for” com o maior vetor. Assim, iremos comparar todos os elementos em busca dos iguais e retorná-los em uma lista.

Pseudocódigo:

```
algoritmo intersec(vetor_a, vetor_b): Vetor de Inteiros
{-
	Entrada: Dois vetores de Inteiros
	Saída: Vetor contendo a interseção dos vetores passados como argumento
-}
	início
	  Se vetor_a = Vazio || vetor_b = Vazio, então
	    retorne Vazio
	  Se len(vetor_a)  > len(vetor_b), então
	    maior = vetor_a
		  menor = vetor_b
	  Senão
	    maior = vetor_b
			menor = vetor_a
	  
	  vetor_c := []
	  Para cada i em menor, faça
	    Para cada j em maior, faça
	      Se i = j, então
	        vetor_c.append(i)
	
	  retorne vetor_c
	fim
```

Análise de Complexidade:

$$
\textstyle\sum_{i=1}^n . \textstyle\sum_{i=1}^m . 3 = 3(n + 1)(n + 1) = 3(n² + 2n + 1)

\\
⠀
\\
Complexidade: O(n²)

\\
⠀
\\
Espaço⠀gasto: O(n)
$$

Código:

```python
def intersec(vetor_a, vetor_b):
  if vetor_a == [] or vetor_b == []:
    return []
  elif len(vetor_a)  > len(vetor_b):
    maior, menor = vetor_a, vetor_b
  else:
    maior, menor = vetor_b, vetor_a
  
  vetor_c = []
  for i in menor:
    for j in maior:
      if i == j:
        vetor_c.append(i)

  return vetor_c

a = [5,7,1,2,9,10]
b = [10,6,7,23,1,2]

print(intersec(a,b), end='\n\n')
```

7**° Dada uma expressão contendo parênteses, literais e operadores aritméticos, elabore um algoritmo para determinar se a expressão está com os parênteses balanceados, ou seja, se para cada parêntese aberto há um parêntese fechando e se os pares de parênteses estão adequadamente aninhados. Você pode supor que a expressão será fornecida como uma string e que a reposta de seu algoritmo será um booleano, onde True significa que a expressão é correta e False, incorreta.**

```markdown
Ex: ((a + b) + (c * d)) é uma expressão correta 
 (( a + b) + 1 é uma expressão incorreta 
 ) (a + b)) + (c * d) é uma expressão incorreta
```

Ideia para solução:

Nessa questão, vamos limpar a entrada deixando apenas uma “String” contendo os Parênteses a serem analisados. Assim, passaremos essa nova “String” para um laço de repetição que irá executar até existir “()” na mesma. Iremos substituir os parenteses encontrados por “String” vazia. Por fim, basta comparar se no resultado sobrou algum parentese. Caso sim, então a expressão não está correta.

Pseudocódigo:

```
algoritmo exp_correta(exp): Boleano
{-
	Entrada: String contendo a expressão a ser analisada
	Saída: Boleano True se a expressão for válida, caso não seja válida então retorna Boleano False.
-}
	início
	  parenteses := []
	  total := 0
	  Para c em exp, faça
	    Se c = "(" || c = ")", então
	      parenteses.append(c)
	  
	  parenteses = ''.join(parenteses)
	  Enquanto houver "()" em parenteses, faça  
	    parenteses := parenteses.replace('()', '') 
	  
	  Se parenteses = '', então
	    retorne True
	  Senão
	    retorne False
	fim
```

Análise de Complexidade:

$$
(\textstyle\sum_{i=1}^n . 5) + n + (\textstyle\sum_{i=1}^n  \textstyle\sum_{i=1}^n) \textstyle\sum_{i=1}^n = 6n + n³ + 2n² + 6n
\\
⠀
\\
Complexidade: O(n³ + n²)

\\
⠀
\\
Espaço⠀gasto: O(2n)
$$

Código:

```python
def exp_correta(exp):
  parenteses = []
  for c in exp:
    if c == "(" or c == ")":
      parenteses.append(c)
  
  parenteses = ''.join(parenteses)
  while ("()" in parenteses):  
    parenteses = parenteses.replace('()', '') 
  
  if parenteses == '':
    return True
  else:
    return False
    
exp = "((a - c) + (b * d))"
print(exp_correta(exp))
```