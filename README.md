Exercício 1

using System;

namespace ConsoleApp1
{
class Program
{
static void Main(string[] args)
{
int num, result;



Console.WriteLine("Digite um número de 1 a 10:");
bool resultadoConversao = int.TryParse(Console.ReadLine(), out num);



if (!resultadoConversao)
{
Console.WriteLine("Você deve digitar apenas número inteiros!");
return;
}



if ((num >= 1) && (num <= 10))
{
if ((num % 2) == 0)
{
for (int i = 0; i <= 10; i++)
{
result = num * i;
Console.WriteLine(num + " X " + i + " = " + result);
}
}
else
{
for (int i = 10; (i <= 10) && (i >= 0); i--)
{
result = num * i;
Console.WriteLine(num + " X " + i + " = " + result);
}
}
}
else
{
Console.WriteLine("Eu mandei digitar um número entre 1 e 10!");
}
}
}
}

---------------------------------------------------------------------------------------------------------------------------------------------------------------
Exercício 2

using System;



namespace Projeto2
{
class Program
{
static void Main(string[] args)
{
string cor;



Console.WriteLine("Informe a cor do semáforo:");



cor = Console.ReadLine();



switch (cor)
{
case "verde":
Console.WriteLine("Pode seguir em frente!");
break;



case "vermelho":
Console.WriteLine("Parada obrigatória!");
break;



case "amarelo":
Console.WriteLine("Atenção motorista!");
break;



default:
Console.WriteLine("Semáforo com defeito! Corrigir o defeito!");
break;
}
}
}
}

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
Exercício 3

using System;

namespace exe3
{
    class Program
    {
        static void Main()
        {
            try
            {
                Console.WriteLine("digite um valor entre 350 e 8750");//digita o numero na tela
                string num = Console.ReadLine();//transforma o digita em string
                int numInt = int.Parse(num);
                int num4 = 0;

                if (numInt >= 350 && numInt <= 8750)
                {

                    char posição1 = num[0];
                    int covert1 = (int)char.GetNumericValue(posição1);
                    int num1 = covert1 % 2;

                    char posição2 = num[1];
                    int covert2 = (int)char.GetNumericValue(posição2);
                    int num2 = covert2 % 2;

                    char posição3 = num[2];
                    int covert3 = (int)char.GetNumericValue(posição3);
                    int num3 = covert3 % 2;

                    try
                    {

                        char posição4 = num[3];
                        int covert4 = (int)char.GetNumericValue(posição4);
                        num4 = covert4 % 2;

                        int result = num1 + num2 + num3 + num4;
                        Console.WriteLine("quantidade de impares:" + result);
                        Console.WriteLine("quantidade de pares:" + (4 - result));
                    }
                    catch
                    {
                        int result = num1 + num2 + num3;
                        Console.WriteLine("quantidade de impares:" + result);
                        Console.WriteLine("quantidade de pares:" + (3 - result));

                    }

                }
                else
                {
                    Console.WriteLine("adicione um tamanho de caractere valido entre 3 e 4");
                }
            }
            catch
            {
                Console.WriteLine("valor invalido");
            }
        }
    }
}








-------------------------------------------------------------------------------------------------------------------------------------------------------------
Exercício 4

using System;



namespace EX4
{
class Program
{
static void Main(string[] args)
{
double numEl, numVV, numVB, numVN, percNumVV, percNumVB, percNumVN;



Console.WriteLine("Digite o número total de eleitores:");
numEl = double.Parse(Console.ReadLine());



Console.WriteLine("Digite o número de votos brancos:");
numVB = double.Parse(Console.ReadLine());



Console.WriteLine("Digite o número de votos nulos:");
numVN = double.Parse(Console.ReadLine());



Console.WriteLine("Digite o número de votos válidos:");
numVV = double.Parse(Console.ReadLine());



percNumVV = (numVV / numEl) * 100;
percNumVB = (numVB / numEl) * 100;
percNumVN = (numVN / numEl) * 100;



Console.WriteLine(numVV + " com o percentual de " + percNumVV + " em relação ao total de eleitores " + numEl);
Console.WriteLine(numVB + " com o percentual de " + percNumVB + " em relação ao total de eleitores " + numEl);
Console.WriteLine(numVN + " com o percentual de " + percNumVN + " em relação ao total de eleitores " + numEl);
}
}
}
