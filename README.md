# func
using System;

class Program
{
    // Function to print the Fibonacci sequence
    static void PrintFibonacci(int count)
    {
        int num1 = 0, num2 = 1, nextNum;

        Console.WriteLine("Fibonacci Sequence:");
        for (int i = 1; i <= count; i++)
        {
            Console.Write(num1 + " ");
            nextNum = num1 + num2;
            num1 = num2;
            num2 = nextNum;
        }
        Console.WriteLine();
    }

    static void Main()
    {
        Console.Write("Enter the number of terms in the Fibonacci sequence: ");
        int count = int.Parse(Console.ReadLine());

        if (count > 0)
        {
            PrintFibonacci(count);
        }
        else
        {
            Console.WriteLine("Please enter a positive integer.");
        }
    }
}
