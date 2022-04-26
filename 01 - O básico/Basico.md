
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
## Declarando Constantes e Variáveis

>Devem ser declaradas antes de serem usadas. Voce declara **Constantes** com a palavra ***let*** e **Variáveis** com a palavra ***var***. 

Exemplo:

    let maximumNumberOfLoginAttempts = 10
    var currentLoginAttempt = 0

Esse trecho de código pode ser lido como: 

"Declare uma nova constante chamada *maximumNumberOfLoginAttempts*, e de a ela um valor de *10*. Em seguida, declare uma nova variável chamada *currentLoginAttempt*, e de a ela um valor inicial de *0*."

Note que, o máximo de tentativas de login permitidas é declarado como constante, pois o valor nunca muda. Já o valor de tentativas de login atual é uma variável, pois o valor deve ser incrementado após cada tentativa com falha.

É possível declarar várias constantes e variáveis em uma única linha. Veja abaixo:

    var x = 0.0, y = 0.0, z = 0.0
    
> **Observaçao**
>
> Se um valor armazenado em seu código nao mudar, sempre o declare como ***let*** (Constante). Use variáveis apenas para armazenar valores que serao alterados.
>

&nbsp;
## Anotaçoes de Tipo 

Voce pode fornecer *anotaçoes de tipo* ao declarar uma constante ou variável, podendo esclarecer o tipo de valores que elas podem armazenar. Escreva colocando dois pontos após o nome da constante ou variável, seguido por um espaço. 

Este exemplo fornece uma anotaçao de tipo para uma variavel chamada *welcomeMessage*, para indicar que ela pode armazenar *Strings* 

    var welcomeMessage: String

Os dois pontos significam "... do tipo ...". Pense nisso como "o tipo de coisa" que pode ser armazenado.

A *welcomeMessage* variável agora pode ser definida para qualquer valor de string sem erro: 

    welcomeMessage = "Hello"

Voce pode definir várias variáveis relacionadas do mesmo tipo em uma única linha: 

    var red, green, blue: Double

> **Observaçao**
>
> É raro que voce precise escrever anotaçoes de tipo na prática. Ao voce fornecer uma valor inicial para uma constante ou uma variável no ponto de definiçao, o Swift quase sempre pode inferir o tipo a ser usado.
>

