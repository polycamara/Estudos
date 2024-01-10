sing System;

namespace DesafioPOO.Models
{
    public class Iphone : Smartphone
    {
        // Construtor
        public Iphone(string numero) : base(numero)
        {
            // Implemente conforme o diagrama
        }

        // Sobrescreve o método InstalarAplicativo da classe pai Smartphone
        public override void InstalarAplicativo(string nomeApp)
        {
            Console.WriteLine($"Instalando {nomeApp} na loja da Apple...");
        }
    }
}

namespace DesafioPOO.Models
{
    public class Nokia : Smartphone
    {
        // Construtor
        public Nokia(string numero) : base(numero)
        {
            // Implemente conforme o diagrama
        }

        // Sobrescreve o método InstalarAplicativo da classe pai Smartphone
        public override void InstalarAplicativo(string nomeApp)
        {
            Console.WriteLine($"Instalando {nomeApp} na loja da Nokia...");
        }
    }
}

namespace DesafioPOO.Models
{
    public abstract class Smartphone
    {
        public string Numero { get; set; }
        // Propriedades conforme o diagrama

        public Smartphone(string numero)
        {
            Numero = numero;
            // Implemente conforme o diagrama
        }

        public void Ligar()
        {
            Console.WriteLine("Ligando...");
        }

        public void ReceberLigacao()
        {
            Console.WriteLine("Recebendo ligação...");
        }

        public abstract void InstalarAplicativo(string nomeApp);
    }
}
