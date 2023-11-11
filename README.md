# Tipagem de Dados

**Exemplo do C#:**

![Untitled](Tipagem%20de%20Dados%20e3c88a26dca941ad9984d55027e1e1c8/Untitled.png)

**Exemplo do JavaScript:**

![Untitled](Tipagem%20de%20Dados%20e3c88a26dca941ad9984d55027e1e1c8/Untitled%201.png)


--------------------------------------------------------------------------------------------------


# Tipos Primitivos

![Untitled](Tipos%20Primitivos%20498185869537404681abb67e204ea10a/Untitled.png)

valor padrão de cada um, caso nenhum valor seja declarado

![Untitled](Tipos%20Primitivos%20498185869537404681abb67e204ea10a/Untitled%201.png)


--------------------------------------------------------------------------------------------------


# Compiladores e Gereciamento

![Untitled](Compiladores%20e%20Gereciamento%20dfedd1a149a247b5938f039e0f607ddb/Untitled.png)

![Untitled](Compiladores%20e%20Gereciamento%20dfedd1a149a247b5938f039e0f607ddb/Untitled%201.png)

 a Microsoft criou a linguagem intermediaria para que todos as linguagens de programação tenha somente um compilador ao invés de vários.

conforme na imagem:

![Untitled](Compiladores%20e%20Gereciamento%20dfedd1a149a247b5938f039e0f607ddb/Untitled%202.png)

O **.NET Standard** consegue fazer a ligação de todos os frameworks juntos para serem trabalhos de forma simultânea 

![Untitled](Compiladores%20e%20Gereciamento%20dfedd1a149a247b5938f039e0f607ddb/Untitled%203.png)


--------------------------------------------------------------------------------------------------


# Versionamento

**Versionamento** seria a versão do programa que você utiliza ou que esta em desenvolvimento.

Definições:

- Podemos utilizar anotações com
- Alpha=> 0.0.1-al
- Beta=>-0.02-bl
- Release Candidate => 1.0.0-rcl
- Final=>1.0.0
- Normalmente alpha e beta tem versões menores que 1.0.0


--------------------------------------------------------------------------------------------------



# Constantes

![Untitled](Constantes%20cf1e4db8efae43d6a79c0b8060de1994/Untitled.png)

Exemplo de constante:

![Untitled](Constantes%20cf1e4db8efae43d6a79c0b8060de1994/Untitled%201.png)

Padrão:

![Untitled](Constantes%20cf1e4db8efae43d6a79c0b8060de1994/Untitled%202.png)


--------------------------------------------------------------------------------------------------


# Nullabe types

![Untitled](Nullabe%20types%204d5c3c254f974b9b96b6029cdeb73bf4/Untitled.png)

![Untitled](Nullabe%20types%204d5c3c254f974b9b96b6029cdeb73bf4/Untitled%201.png)

a interrogação que transforma em null, e a IDE aceita quando colocar a interrogação

![Untitled](Nullabe%20types%204d5c3c254f974b9b96b6029cdeb73bf4/Untitled%202.png)

GetValueOeDefault = ele pega o valor padrao igual no exemplo a baixo, caso seja null ele vai mostrar zero.

HasValue = ele retorna em boolean true ou false, para saber se é ou não null

value = ele lança um exception caso não tenha valor (tipo um erro)

![Untitled](Nullabe%20types%204d5c3c254f974b9b96b6029cdeb73bf4/Untitled%203.png)

Resultado deste codigo acima: 

0
10
False
True
X is null
10

![Untitled](Nullabe%20types%204d5c3c254f974b9b96b6029cdeb73bf4/Untitled%204.png)

as duas interrogações é se caso o x for null ai ele pega o valor do lado direito que seria 0.0

```csharp
using System;
using System.Xml;

namespace Course {
    class Program {
        static void Main(string[] args) {

            double? x = null;
            double? y = 10;

            double a = x ?? 5;
            double b = y ?? 5;

            Console.WriteLine(a);
            Console.WriteLine(b);
        }
    }
}
```

RESULTADO: 

5
10


--------------------------------------------------------------------------------------------------


# Conversão

esses são os tipos primitivos aceitos para cada um deles, na conversão.

![Untitled](Conversão%20b6c0b88ca3014682b4f77255c4433077/Untitled.png)

![Untitled](Conversão%20b6c0b88ca3014682b4f77255c4433077/Untitled%201.png)

ele so deixa realizar a conversao implicita, quando o byte do tipo primitivo ´´e maior que o solicitado, ex: double ´´e 8 bytes e float sendo 4 bytes, cabe perfeitamente no double.

```csharp
//metodo de conversao implicita
float x = 4.5f;
        double y = x;

```

agora mesmo se o desenvolvedor quiser colocar um tipo primitivo grande e incluir no pequeno ele consegue atraves do casting.

```csharp
//metodo de casting
double a;
float b;
a = 5.1;
b = (float)a;
Console.WriteLine(b);
```


--------------------------------------------------------------------------------------------------



# Matematica e Math

![Untitled](Matematica%20e%20Math%2062bf5fb4ff524945bdf7475dcfc55088/Untitled.png)

```csharp
código tradicional: a=a+2;
código de atribuição: a+=2;
```

```csharp
int x = O; // Atribuição
x += 5; // x = x + 5;
x -= 1; // x = x - 1;
x x= 10; // x = x * 10;
x /= 2; // x = x / 2;
```

![Untitled](Matematica%20e%20Math%2062bf5fb4ff524945bdf7475dcfc55088/Untitled%201.png)


--------------------------------------------------------------------------------------------------


# Swtich Case, While e Do While

**Usando switch case:**

```csharp
int valor = 1;
switch (valor)
{
	case 1: Console.WriteLine("1"); break;
	case 2: Console.WriteLine("2"); break;
	case 3: Console.WriteLine("3"); break;
	default: Console.WriteLine("4"); break; // Se não for 1,2 ou 3
}
```

![Untitled](Swtich%20Case,%20While%20e%20Do%20While%206b9a33ca065f42f2813bc7a328227dd9/Untitled.png)

do while ex:

![Untitled](Swtich%20Case,%20While%20e%20Do%20While%206b9a33ca065f42f2813bc7a328227dd9/Untitled%201.png)

![Untitled](Swtich%20Case,%20While%20e%20Do%20While%206b9a33ca065f42f2813bc7a328227dd9/Untitled%202.png)



--------------------------------------------------------------------------------------------------



# Moedas

quando mexer com moedas a melhor forma de trabalhar com dinheiro em bancos ou outras instituicoes seria usar o tipo decimal conforme o exemplo abaixo, ele tem a melhor precisao, ele e um pouco mais lento que o double, mas as empresas pode perder milhoes caso o desenvolvedor troque para double, pois a precisao dele e muito menor que o decimal.

```csharp
using System;

namespace Strings {
    internal class Program {
        static void Main(string[] args) {

            decimal valor = 10.256516516516m;

            Console.WriteLine(valor);

        }
      
    }
}
```

# FORMATADORES DE MOEDAS

```csharp
/*
                                FORMATADORES DE MOEDAS 
      
      decimal valor = 10.25m;

            Console.WriteLine(valor.ToString(
                "C",CultureInfo.CreateSpecificCulture("pt-BR")));  aqui podemos especificar para ele qual a formatacao ideal para cada cultura, com a letra "C" pedimos para que ele mostre o valor em dinheiro
                                                                   RESULTADO => R$ 10,25

            Console.WriteLine(valor.ToString(
                "F", CultureInfo.CreateSpecificCulture("pt-BR")));  com a letra "F" pedimos para que ele mostre o valor em mais exato possivel RESULTADO => 10,25

            Console.WriteLine(valor.ToString(
                "P", CultureInfo.CreateSpecificCulture("pt-BR")));  mostra o resultado com porcentagem RESULTADO => 1.025,00%

                        MATH DE NUMERO 

    decimal valor = 10536.25m;
            Console.WriteLine(
                 Math.Round(valor)  ele arredonda o resultado RESULTADO => 10536
                 Math.Ceiling(valor)  ele arredonda para mais   RESULTADO => 10537
                Math.Floor(valor) ele arredonda para menos   RESULTADO => 10536
                );
    */
```


--------------------------------------------------------------------------------------------------



# Exceptions

```csharp
using System;
using System.Globalization;

namespace Editor_de_texto {
    internal class Program {
        static void Main(string[] args) {

            var arr = new int[3];

            try { // tente rodar o for, se caso der algo de errado ele passa para o catch

                //for (var index = 0; index < 10; index++) {

                //    Console.WriteLine(arr[index]); //  gerou este erro System.IndexOutOfRangeException, pois estamos pedindo para ele percorrer 11 arrays, sendo que ele tem somente 4 arrays
                //}
                Cadastrar("");
            } catch (IndexOutOfRangeException ex) { // fora de index gera esse erro 
                Console.WriteLine(ex.InnerException);
                Console.WriteLine(ex.Message);
                Console.WriteLine("não encontrei o indice na lista");

            } catch (ArgumentNullException ex) {  // aqui ele verifica se o parametro esta nulo, caso seja true ele mostra a mensagem de erro abaixo ()
                Console.WriteLine(ex.InnerException); // exibi tambem uma mensagem de erro e visualize informacoes detalhadas sobre a raiz do problema
                Console.WriteLine(ex.Message); // exibi a mensagem de erro na tela 
                Console.WriteLine("falha ao cadastrar texto");
            } catch (MinhaException ex) {  
                Console.WriteLine(ex.InnerException); 
                Console.WriteLine(ex.Message);
                Console.WriteLine(ex.QuantoAconteceu);
                Console.WriteLine("exceção customizada");
            } catch (Exception ex) {  // imprima esssa informacao caso algo der errado (sempre tem essa ordem de try em primeiro e depois o catch) se gerar um erro desconhecido ou generico roda essa codição
                Console.WriteLine(ex.InnerException); // exibi tambem uma mensagem de erro e visualize informacoes detalhadas sobre a raiz do problema
                Console.WriteLine(ex.Message); // exibi a mensagem de erro na tela 
                Console.WriteLine("Ops algo deu errado!!");
            }
        }
        static void Cadastrar(String texto) {
             if (string.IsNullOrEmpty(texto))//  se caso a string for nula ou vazia vai gerar erro
                throw new MinhaException(DateTime.Now);
        }

        public class MinhaException : Exception { // foi feito uma classe em herança

            public MinhaException(DateTime date) {  // foi realizado aqui o metodo construtor

                QuantoAconteceu = date;  // é atribuido o valor do date para a propriedade "QuandoAconteceu"
            }
            public DateTime QuantoAconteceu { get; set; } /*isso é uma propriedade de um objeto, que utiliza a classe DateTime para trabalhar com datas e horários.*/
        }
    
    }
}
```



--------------------------------------------------------------------------------------------------



# foreach

![Untitled](foreach%207799abe6d2b54154a0729243f2a98cad/Untitled.png)

Comparação resolvendo com for e depois com o foreach.


--------------------------------------------------------------------------------------------------


# Matrizes

```csharp
namespace Course {
    class Program {
        static void Main(string[] args) {

            double[,] mat = new double[9, 9];
            Console.WriteLine(mat.Length); // quantos elementos a matrix tem no total
            Console.WriteLine(mat.Rank); // quantidade total de linhas
            Console.WriteLine(mat.GetLength(0)); // quantidade de linhas
            Console.WriteLine(mat.GetLength(1));
        }
    }
}
```

para inicia uma matriz ex:

```csharp
int n = int.parse(console.readLine())

int [,] mat = new int [n,n]
```


--------------------------------------------------------------------------------------------------


# Expressão ternaria

![Untitled](Expressão%20ternaria%20e93e7ace12b44bb49ca73b085c363103/Untitled.png)

![Untitled](Expressão%20ternaria%20e93e7ace12b44bb49ca73b085c363103/Untitled%201.png)

