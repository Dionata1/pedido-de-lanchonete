# pedido-de-lanchonete
Este projeto é um programa simples em C# que simula o sistema de pedidos de bebidas em uma lanchonete. O
usuário pode escolher bebidas de um cardápio, adicionar ao pedido e no final ver o valor total da compra.
É um exercício prático para treinar a estrutura switch case e o uso de loops.
Funcionalidades
Exibe um menu de bebidas com preços.
Permite que o usuário escolha quantas bebidas quiser.
Calcula o valor total do pedido automaticamente.
Finaliza o pedido ao selecionar a opção “Sair/Finalizar".
Cardápio de Bebidas 1 - Coca-Cola (R$ 5,00) 2 - Suco de Laranja (R$ 6,00) 3 - Água (R$ 3,00) 4 - Café (R$ 4,00) 5-
Finalizar pedido
using System;

namespace sistema_de_lanchonete
{
    class Program
    {
        static void Main()
        {
            int opcao;
            double total = 0;

            do
            {
                Console.WriteLine("\n======== Cardápio de bebidas ========");
                Console.WriteLine("1. Coca-Cola - R$ 5,00");
                Console.WriteLine("2. Suco de laranja - R$ 6,00");
                Console.WriteLine("3. Água - R$ 3,00");
                Console.WriteLine("4. Café - R$ 4,00");
                Console.WriteLine("5. Finalizar pedido");
                Console.WriteLine("====================================");

                Console.Write("Escolha uma opção: ");
                opcao = int.Parse(Console.ReadLine());

                switch (opcao)
                {
                    case 1:
                        total += 5.00;
                        Console.WriteLine("Coca-Cola adicionada ao pedido.");
                        break;

                    case 2:
                        total += 6.00;
                        Console.WriteLine("Suco de laranja adicionado ao pedido.");
                        break;

                    case 3:
                        total += 3.00;
                        Console.WriteLine("Água adicionada ao pedido.");
                        break;

                    case 4:
                        total += 4.00;
                        Console.WriteLine("Café adicionado ao pedido.");
                        break;

                    case 5:
                        Console.WriteLine($"Pedido finalizado. Total a pagar: R$ {total:F2}");
                        break;

                    default:
                        Console.WriteLine("Opção inválida. Tente novamente.");
                        break;
                }

                if (opcao != 5)
                {
                    Console.WriteLine($"Total atual: R$ {total:F2}");
                }

            } while (opcao != 5);

            Console.WriteLine("Obrigado por comprar conosco!");
        }
    }
}
