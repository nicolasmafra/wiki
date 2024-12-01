# Exponencial

## Motivação

A exponencial parece conectar áreas totalmente diferentes da matemática, como mapeamento de multiplicação para adição, equações diferenciais, números complexos e rotações. Ao mesmo tempo, existem diversas formas de caracterizar a exponencial. Então, encontremos a definição mais elementar e cheguemos às demais caracterizações como consequência.

Referência: [caracterizações da exponencial](https://en.wikipedia.org/wiki/Characterizations_of_the_exponential_function#Characterizations)

## Uma operação aritmética

A multiplicação é uma operação binária que repete a adição, por isso tem a propriedade distributiva:

$$
a.(x+y)=(a.x)+(a.y)
$$

De maneira análoga, a exponenciação (ou potenciação) repete a multiplicação. Portanto ela também tem uma propriedade análoga:

$$
a^{(x+y)} = (a^x).(a^y)
$$

## Uma função

Se a base da potência for fixada, passamos a ter uma função (operação unária) em vez de uma operação binária:

$$
f(x) = a^x
$$

Analisemos os possíveis valores para a base: se for negativa, a função não é bem definida para parâmetros não inteiros; se for 0 ou 1, a função se torna constante; se for maior que 1 é crescente; se for entre 0 e 1 é decrescente.

Note também que a função decrescente é o espelhamento horizontal da função crescente, que pode ser obtida invertendo a base, pela relação:

$$
a^{-x} = (1/a)^x
$$

Ou seja, podemos concentrar nossos esforços apenas na função crescente ao definir que a base seja maior que 1.

## Equação funcional

A função de exponenciação poderia ser definida também como sendo **qualquer** função estritamente crescente que satisfaça a propriedade já citada:

$$
f(x+y)=f(x)f(y)
$$

Que implica em:

$$
f(0) = 1
\\ f(1) = a
$$

Onde "a" é base da exponenciação, sendo qualquer valor maior que 1.

## Exponencial Natural

Dada uma função que satisfaz a equação funcional e tomando sua derivada, obtemos:

$$
f'(x)=\lim_{\Delta \to 0} \frac{f(x+\Delta)-f(x)}{\Delta}
=\lim_{\Delta \to 0} \frac{f(x)f(\Delta)-f(x)}{\Delta}
=f(x)\lim_{\Delta \to 0} \frac{f(\Delta)-1}{\Delta}
$$

E calculando esse novo limite:

$$
\lim_{\Delta \to 0} \frac{f(\Delta)-1}{\Delta}
=\lim_{\Delta \to 0} \frac{f(0+\Delta)-f(0)}{\Delta}
=f'(0)
$$

Ou seja, a derivada é proporcional à própria função, com constante de proporcionalidade igual à derivada no ponto zero.

Como a base da exponenciação é qualquer valor maior que 1, essa constante pode ser qualquer valor positivo, então podemos escolher que seja 1. Agora definamos uma exponencial _natural_ a partir das seguintes condições:

$$
\exp(x+y) = \exp(x)\exp(y)
\\ \exp'(0) = 1
$$

Que implica também na definição de uma base natural:

$$
exp(1) = e
$$

Portanto, outra forma de escrever a exponencial natural seria:

$$
\exp(x) = e^x
$$

## Equação diferencial

Agora que esse fator é 1, é verdade que:

$$
\exp'(x)=\exp(x)
$$

Assim, uma outra definição para a exponencial natural seria pelas seguintes condições:

$$
f'(x) = f(x)
\\ f'(0) = 1
$$

### Série de Taylor

Se derivar a exponencial uma vez resulta nela mesma, então derivar n vezes também. E sabendo a enésima derivada, é possível extrair a série de Taylor da exponencial natural ao redor do ponto zero (série de Maclaurin):

$$
\exp(x) = \lim_{n \to \infty} \sum_{k=0}^n \frac{x^k}{k!}
$$

Desse modo, podemos calcular a base natural:

$$
e = \exp(1) = \lim_{n \to \infty} \sum_{k=0}^n \frac{1}{k!}
$$

### Limite do produto

[Referência](https://en.wikipedia.org/wiki/Characterizations_of_the_exponential_function#Characterization_1_%E2%87%94_characterization_4).

Sabendo que podemos aproximar uma função recursivamente pelo método de Euler:

$$
f(x) = f(n\Delta t)
\\ f(t+\Delta t) \approx f(t)+f'(t)\Delta t
$$

Então aplicando na exponencial e resolvendo a recursão:

$$
\exp(t+\Delta t) \approx \exp(t)+\exp'(t)\Delta t = exp(t)(1+\Delta t)
\\ \exp(x) \approx (1+\Delta t)^n
$$

Assim, temos mais uma forma de definir a exponencial:

$$
\exp(x) = \lim_{n\to\infty}\left(1+\frac{x}{n}\right)^n
$$

E, consequentemente, mais uma forma de definir a base natural:

$$
e = \exp(1) = \lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n
$$
