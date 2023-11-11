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