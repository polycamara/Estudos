# Estudos


# Construindo um Sistema para um Estacionamento com C#

Desafio de construir um sistema para um estacionamento DIO.

## Código

    int resposta = 1;
    List<string> placas = new List<string>();

        Console.WriteLine("Seja bem-vindo ao sistema de estacionamento!");

        Console.WriteLine("Digite o preço inicial: ");
        double preçoInicial = Convert.ToDouble(Console.ReadLine());

        Console.WriteLine("Agora digite o preço por hora: ");
        double preçoHora = Convert.ToDouble(Console.ReadLine());

    while (resposta != 4)
    {
        Console.WriteLine("Digite a sua opção: \n 1 - Cadastrar veículo \n 2 - Remover veículo \n 3 - Listar veículos \n 4 - Encerrar");
        resposta = Convert.ToInt32(Console.ReadLine());

    if (resposta == 1)
    {
        Console.WriteLine("Digite a placa do veículo para estacionar: ");
        string placa = Console.ReadLine();
        placas.Add(placa);
    }
    else if (resposta == 2)
    {
        Console.WriteLine("Digite a placa do veículo para retirar: ");
        string placaRemover = Console.ReadLine();

        placas.Remove(placaRemover);

        Console.WriteLine("Quantas horas o veículo permaneceu no estacionamento?");
        double horasEstacionado = Convert.ToDouble(Console.ReadLine());

        Console.WriteLine($"O valor do estacionamento ficou: {preçoInicial + (preçoHora * horasEstacionado)} reais");

    }
    else if (resposta == 3)
    {
        Console.WriteLine("\nLista de veículos estacionados:");
        foreach (string placacarro in placas)
        {
            Console.WriteLine(placacarro);
        }
        Console.WriteLine();
    }
    else if (resposta == 4)
        {
        Console.WriteLine("Agradecemos sua visita!");
        }
    }
