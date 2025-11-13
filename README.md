using System;

class Program
{
    static void Main()
    {
        
        string[] vetor = new string[10]
        {
            "Ana", "Bruno", "Carlos", "Daniela", "Eduardo",
            "Fernanda", "Gabriel", "Helena", "Igor", "Juliana"
        };

 
        Console.Write("Digite o nome ou número que deseja buscar: ");
        string busca = Console.ReadLine();

      
        int posicao = -1;

        
        for (int i = 0; i < vetor.Length; i++)
        {
            if (vetor[i].Equals(busca, StringComparison.OrdinalIgnoreCase))
            {
                posicao = i;
                break; 
            }
        }

      
        if (posicao != -1)
        {
            Console.WriteLine($"Elemento '{busca}' encontrado na posição {posicao} do vetor.");
        }
        else
        {
            Console.WriteLine("Não encontrado.");
        }

        Console.ReadKey();
    }
}
