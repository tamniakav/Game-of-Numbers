# Game-of-Numbers
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Game_of_Numbers
{
    class Program
    {
        static void Main(string[] args)
        {
            int a = int.Parse(Console.ReadLine());
            int b = int.Parse(Console.ReadLine());
            int maxNum = int.Parse(Console.ReadLine());

            int m = 0;
            int n = 0;
            int count = 0;
            

            for (int i = a; i <= b; i++)
            {
                for (int j = a; j <= b; j++)
                {
                    int sum = i + j;
                    count++;
                    
                    if (sum == maxNum)
                    {
                        m = i;
                        n = j;
                    }
                }
            }
            if (m + n == maxNum)
            {
                Console.WriteLine($"Number found! {m} + {n} = {maxNum}");
            }
            else
            {
                Console.WriteLine($"{count} combinations - neither equals {maxNum}");
            }
        }
    }
}
