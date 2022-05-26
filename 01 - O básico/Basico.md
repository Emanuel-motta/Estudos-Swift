
# **O Básico** 

> Swift é uma nova linguagem de programaçao para desenvolvimento iOS. No entanto, muitas coisas sao familiares da Linguagem C e Objective-C.

Swift fornece suas próprias versoes de todos os tipos fundamentais: 

1. **Int:** Para inteiros;
2. **Double e Float:** Para valores de ponto flutuante;
3. **Bool:** Para valores booleanos;
4. **String:** Para valores textuais.

Também tem versoes poderosas dos tres tipos de coleçoes principais: **Array, Set e Dictionary**.

O uso de constantes no Swift é muito mais poderoso do que em C. Usadas em todo o Swift para tornar o código mais seguro e claro na intençao de quando for trabalhar com valores fixos.

**Swift é uma linguagem do *tipo seguro*, o que significa que ela te ajuda a ter clareza sobre os tipos de valores com os quais seu código pode trabalhar.**

&nbsp;
# **Constantes e Variáveis** 

> Constantes e variáveis associam um nome a um valor de um tipo específico. **O valor de uma constante NAO pode ser alterado depois de definido**, enquanto uma variável pode ser definida com um valor diferente no futuro.

&nbsp;
## **Declarando Constantes e Variáveis**

>Devem ser declaradas antes de serem usadas. Voce declara **Constantes** com a palavra ***let*** e **Variáveis** com a palavra ***var***. 

Exemplo:

~~~ Swift
let maximumNumberOfLoginAttempts = 10
var currentLoginAttempt = 0
~~~

Esse trecho de código pode ser lido como: 

"Declare uma nova constante chamada *maximumNumberOfLoginAttempts*, e de a ela um valor de *10*. Em seguida, declare uma nova variável chamada *currentLoginAttempt*, e de a ela um valor inicial de *0*."

Note que, o máximo de tentativas de login permitidas é declarado como constante, pois o valor nunca muda. Já o valor de tentativas de login atual é uma variável, pois o valor deve ser incrementado após cada tentativa com falha.

É possível declarar várias constantes e variáveis em uma única linha. Veja abaixo:

~~~ Swift
var x = 0.0, y = 0.0, z = 0.0
~~~

> **Observaçao**
>
> Se um valor armazenado em seu código nao mudar, sempre o declare como ***let*** (Constante). Use variáveis apenas para armazenar valores que serao alterados.
>

&nbsp;
## **Anotaçoes de Tipo** 

Voce pode fornecer *anotaçoes de tipo* ao declarar uma constante ou variável, podendo esclarecer o tipo de valores que elas podem armazenar. Escreva colocando dois pontos após o nome da constante ou variável, seguido por um espaço. 

Este exemplo fornece uma anotaçao de tipo para uma variavel chamada *welcomeMessage*, para indicar que ela pode armazenar *Strings* 

~~~ Swift
var welcomeMessage: String
~~~

Os dois pontos significam "... do tipo ...". Pense nisso como "o tipo de coisa" que pode ser armazenado.

A *welcomeMessage* variável agora pode ser definida para qualquer valor de string sem erro: 

~~~ Swift
welcomeMessage = "Hello"
~~~

Voce pode definir várias variáveis relacionadas do mesmo tipo em uma única linha: 

~~~ Swift
var red, green, blue: Double
~~~
> **Observaçao**
>
> É raro que voce precise escrever anotaçoes de tipo na prática. Ao voce fornecer uma valor inicial para uma constante ou uma variável no ponto de definiçao, o Swift quase sempre pode inferir o tipo a ser usado.
>

&nbsp;
## **Nomenclatura de constantes e variáveis**

Nomes de constantes e variáveis podem conter quase qualquer caractere, incluindo carcteres unicode:

~~~ Swift
let π = 3.14159
let 你好 = "你好世界"
let 🐶🐮 = "dogcow"
~~~

Os nomes nao podem conter caracteres de espaço em branco, símbolos matemáticos, setas, valores escalares Unicode de uso privado ou caracteres de desenho de linha de caixa.

Após a declaraçao de uma constante ou uma variável, voce nao pode declará-la novamente com o mesmo nome ou alterá-la para armazenar valores de um tipo diferente

> **Oservaçao**
>
> Se voce precisar dar a uma constante ou variável o mesmo nome de uma palavra-chave reservada do Swift, coloque a palavra-chave com acentos graves (´) ao usá-la como um nome. No Entanto, evite usar palavras-chave como nomes, a menos que voce nao tenha escolha.
>

Voce pode alterar o valor de uma variável existente para outro valor de um tipo compátivel.

~~~ Swift
    var friendlyWelcome = "Hello !!"
    friendlyWelcome = "Bonjour !!"
    // friendlyWelcome is now "Bonjour !"
~~~

Ao contrário de uma variável, o valor de uma constante nao pode ser alterado depois de definido.

 ~~~ Swift
let languageName = "Swift"
languageName = "Swift++"
// This is a compile-time error: languageName cannot be changed
~~~

&nbsp;
## **Imprimindo Constantes e Variáveis**

Voce pode imprimir o valor atual de uma constante ou variável com a funçao:

~~~ Swift
print(friendlyWelcome)
// Prints "Bonjour!"
~~~

A ***print(_:separator:terminator:)*** é uma funçao global que imprime um ou mais valores em uma saida apropriada. No Xcode, por exemplo, a funçao imprime sua saída no console. 

O Swift usa a ***interpolaçao de strings*** para incluir o nome de uma constante ou variável como um espaço reservado de uma string. Basta colocar o nome entre parenteses e escape com uma barra invertida antes do parentese: 

~~~ Swift
print ("The current value of friendlyWelcome is \(friendlyWelcome)")
// Prints "The current value of friendlyWelcome is Bonjour !"
~~~

&nbsp;
# **Comentários**

**Use comentários para incluir texto nao executável em seu código, como uma nota ou um lembrete.**

Comentários em Swift sao muito semelhantes aos comentarios em C. Comentários de linha única começam com duas barras (//):

~~~ Swift
// This is a comment.
~~~

Comentários de várias linhas começam com uma barra seguida de asterisco (/*) e terminam com um asterisco seguido de uma barra (*/):

~~~ Swift
 /* This is also a comment
 but is written over multiple lines. */
~~~

&nbsp;
# **Ponto e Vírgula**

Ao contrário de muitas outras linguagens, o Swift nao exige que voce escreva um ponto e virgula (;) após cada instruçao em seu código. No entanto, os pontos e vírgulas sao necessarios se voce quiser escrever varias instruçoes separadas:

~~~ Swift
let cat = "Miau"; Print(cat)
// Prints "Miau"
~~~

&nbsp;
# **Inteiros**

>Os ***inteiros*** sao numeros sem componentes fracionário, como ***42*** e ***-23***. Os inteiros sao com ***sinal*** (positivo, zero ou negativo) ou ***sem sinal*** (positivo ou zero). 

&nbsp;
## **Limites Inteiros**

Voce pode acessar os valores minimo e maximo de cada tipo inteiro com seus propriedades ***min*** e ***max***:

~~~Swift
let minValue = UInt8.min // minValue is equal to 0, and is of type UInt8 
let maxValue = UInt8.max // maxValue is equal to 255, and is of type UInt8
~~~

Os valores dessas propriedades sao do tipo numerico de tamanho apropriado e, portanto, podem ser usados em expressoes junto com outros valores do mesmo tipo.

&nbsp;
## **Int**

Na maioria dos casos, voce nao precisa escolher um tamanho específico de inteiro para seu código.
- Em uma plataforma de 32 bits, ***Int*** é do mesmo tamanho que ***Int32***.
- Em uma plataforma de 64 bits, ***Int*** é do mesmo tamanho que ***Int64***.

A menos que voce precise trabalhar com um tamanho específico de inteiro, sempre use ***Int*** para valores inteiros em seu código. Isso ajuda a consistencia e a interoperabilidade do código.

&nbsp;
## **UInt**

Swift também fornece um tipo inteiro sem sinal, ***UInt***, que tem o mesmo tamanho que o tamanho da palavra nativa da plataforma atual:

- Em uma plataforma de 32 bits, ***UInt*** é do mesmo tamanho que ***UInt32***.
- Em uma plataforma de 64 bits, ***UInt*** é do mesmo tamanho que ***UInt64***.

> **Observaçao**
>
> Use ***UInt*** somente quando precisar especificamente de um tipo inteiro sem sinal com o mesmo tamanho da palavra nativa da plataforma. Se este nao for o caso, opte sempre pelo uso do ***Int***, um uso consistente de ***Int*** para valores inteiros ajuda a interoperabilidade do código, evita a necessidade de conversao. 
>

&nbsp;
# **Números de ponto flutuante**

> Número de ***ponto flutuante*** sao numeros com um componente fracionario, como ***3.14159***, ***0.1*** e ***-273.15***.

Os tipos de ponto flutuante pode representar um intervalo de valores muito maior que os do tipo inteiros e podem armazenar números maiores ou menores do que podem ser armazenados em um arquivo ***Int***. **Swift forneve dois tipos de númetos de ponto flutuantes assinados:**

- ***Double*** representa um númeto de ponto flutuante de 64 bits.
- ***Float*** representa um númeto de ponto flutuante de 32 bits.

> **Observaçao**
>
> ***Double*** tem uma precisao de pelo menos 15 dígitos decimais, enquanto a precisao de ***Float*** pode ser 6 dígitos decimais. O tipo de ponto flutuante apropriado a ser usado depende da natureza e do intervalo de valores com os quais voce precisa trabalhar em seu código. Em situaçoes onde qualquer tipo seria apropriado, ***Double*** é preferível.
>

&nbsp;
# **Segurança de tipo e Inferencia de tipo**

Como dito anteriormente, Swift é uma linguagem de *tipo seguro*. O que significa que voce tem que ser claro sobre os tipos de valores no qual voce utiliza em seu codigo, se uma parte requerer *String* voce nao pode passa-la como *Int*. 

Sao executadas *verificaçoes de tipo* ao compilar o código para sinalizar quaisquer tipo incompatível. Sendo assim, mais facil a detecçao e correçao de erros.

Essa *verificaçao de tipo* facilita o trabalho com diferentes tipos de valores. Sendo desnecessario a especificaçao do tipo de cada variável ou constante. O Swift por si só realiza a *inferencia de tipo* para assimilar o tipo apropriado para cada constante ou variável, examinando os valores fornecidos.

> Devido a *inferencia de tipo*, Swift requer poucas declaraçoes de tipo. 
>
> Constantes e variáveis sao explicitamente tipadas, mas muito do trabalho já é feito para voce.

A *inferencia de tipo* é útil quando se declara uma constante ou variável com um valor inicial. Isso ocorre quando é atribuido um valor *Literal* a constante ou variável 

> Um valor *literal* é um valor que aparece direto no código fonte.

Por exemplo: 

~~~Swift
let meaningOfLife = 42
// meaningOfLife is inferred to be of type Int
~~~

Da mesma forma se voce nao especificar um tipo para um literal de *Ponto Flutuante*, o Swift SEMPRE deduzirá como sendo um *Double* em vez de *Float* 

~~~Swift
let pi = 3.14159
// pi is inferred to be of type Double
~~~

Se voce combinar literais inteiros e de ponto flutuante em uma expressao essa regra se mantem, e o tipo inferido sera *Double*

~~~Swift
let anotherPi = 3 + 0.14159
// anotherPi is also inferred to be type Double
~~~

&nbsp;
# **Alias de Tipo**

> Os *aliases* de tipo definem um nome alernativo para um tipo existente. Voce define aliases de tipo com a palavra chave ***typealias***

~~~Swift
typealias AudioSample = UInt16
~~~

Depois de definir um alias de tipo, voce pode usar o alias em qualquer lugar em que possa usar o nome original

~~~Swift
var maxAmplitudeFound = AudioSample.min
// maxAmplitudeFound is now 0
~~~

Aqui, *AudioSample* é definico como um alias para *UInt16*. Por ser um alias, a chamada para *AudioSample.min* realmente chama *UInt16.min*, que fornece um valor inicial de 0 para a *maxAmplitudeFound* variável.

&nbsp;
# **Booleanos**

Swift tem um tipo Booleano básico, chamado ***Bool***. Os valores booleanos sao chamados de lógicos, porque eles só podem ser verdadeiros ou falsos. Swift fornece dois valores de constantes booleanas *true* e *false* :

~~~Swift
let orangesAreOrange = true
let turnipsAreDelicious = false
~~~

Os dois valores foram inferidos como *Bool* a partir do momento em que foram incializados como valores literais booleanos. 