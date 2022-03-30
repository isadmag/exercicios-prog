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
