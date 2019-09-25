# Fight-simulator

using System;

namespace Fantazy_fighting
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Skriv namn till fighter nr 1");
            Console.Write(": ");
            string fn1 = Console.ReadLine();
            Console.WriteLine("Skriv namn till fighter nr 2");
            Console.Write(": ");
            string fn2 = Console.ReadLine();

            string[] teq = new string[24] {" slog "," sparkade "," Högg "," spottade på "," petade på "," sköt ", " använde tankekraft på ", " kissade på ", " motorsågade ", " skrek fan till ",
                " pissade på ", " ollade ", " sågade ", " la en ost på ", " körde in en tandpetare i "," högg med en yxa "," hämtade mobbade ungen så han kunde stirra på "," spydde på ",
                " fimpade en cigg på "," sköt med en hagel bössa på "," slog med ett baseboll trä "," gjorde något skumt som inte borde nämnas på "," slickade på "," karate choppade " };
            string[] del = new string[11] {" pung ", " Höger fot", " vänster fot ", " höger ben ", " vänster ben ", " magen ", " huvudet ", " höger arm ", " vänster arm ", " höger hand ", " vänster hand " };

            int h1 = 100;
            int h2 = 100;

            string sid = "--------------------------------------------------------------------------";
            Random random = new Random();
            int f = random.Next(1, 11);
            int d = random.Next(1, 11);
            int s = random.Next(1,35);

            bool loop = true;

            while (loop==true) {
                startText();

                Console.WriteLine("--------------------------------------------------------------------------");

                d = random.Next(1, 10);
                f = random.Next(1,10);
                s = random.Next(1,35);
                Console.WriteLine(fn1+teq[f]+fn2+"s"+del[d]);
                Console.WriteLine("Det gjorde: "+s+" Skada");
                h2 -= s;

                Console.WriteLine("--------------------------------------------------------------------------");

                d = random.Next(1, 10);
                f = random.Next(1, 10);
                s = random.Next(1, 35);
                Console.WriteLine(fn2 + teq[f] + fn1 + "s" + del[d]);
                Console.WriteLine("Det gjorde: " + s + " Skada");
                h1 -= s;
                Console.WriteLine("--------------------------------------------------------------------------");
                Console.WriteLine("--------------------------------------------------------------------------");
                Console.WriteLine(fn1 + "s liv= " + h1 + " | " + fn2 + "s liv= " + h2);

                if (h1<1)
                {
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("----------------------<||" + fn2 + " Vann!" + "||>-------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    loop = false;
                }
                else if (h2 < 1)
                {
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("----------------------<||" + fn1 + " Vann!"+ "||>-------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    Console.WriteLine("--------------------------------------------------------------------------");
                    loop = false;
                }

                Console.ReadLine();
            }
            
        }
        static void startText()
        {
            for (int i = 20; i> 0; i--) {
                Console.WriteLine("--------------------------------------------------------------------------");
            }
            Console.WriteLine("--------------------------------------------------------------------------");
            Console.WriteLine("------------ooooooooo--oo------oooo------oo-----oo--oooooooooooooo-------.");
            Console.WriteLine("------------ooooooooo--oo----oo----oo----oo-----oo--------oo--------------");
            Console.WriteLine("------------oo---------oo--oo--------oo--oo-----oo--------oo--------------");
            Console.WriteLine("------------ooooo------oo--oo------------ooooooooo--------oo--------------");
            Console.WriteLine("------------ooooo------oo--oo----oooooo--ooooooooo--------oo--------------");
            Console.WriteLine("------------oo---------oo--oo--------oo--oo-----oo--------oo--------------");
            Console.WriteLine("------------oo---------oo----oo----oo----oo-----oo--------oo--------------");
            Console.WriteLine("------------oo---------oo------oooo------oo-----oo--------oo--------------");
            Console.WriteLine("--------------------------------------------------------------------------");
        }
    }
}
