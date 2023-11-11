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