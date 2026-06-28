# Tarea2GenesisJavierFlujoDeControlGrupo8
Tarea 2 Primera Unidad sobre el Flujo De Control Algoritmos Computacionales
using System;
class Main
{
    static void Program(string[] args)
    {
        Console.WriteLine("Calculo del Impuesto Sobre la Renta (ISR)");
        Console.WriteLine("-----------------------------------------");

        Console.Write("Ingrese el sueldo anual del empleado: ");
        double sueldo = Convert.ToDouble(Console.ReadLine());

        double isr = 0;

        if (sueldo <= 416220)
        {
            isr = 0;
        }
        else if (sueldo <= 624329)
        {
            isr = (sueldo - 416220) * 0.15;
        }
        else if (sueldo <= 867123)
        {
            isr = 31216 + (sueldo - 623329) * 0.20;
        }
        else
        {
            isr = 79776 + (sueldo - 867123) * 0.25;
        }
        Console.WriteLine("Sueldo: RD$" + sueldo.ToString("N2"));
        if (isr == 0) 
        {
            Console.WriteLine("ISR: N/A");
        } 
        else
        {
          Console.WriteLine(" ISR: RD$" + isr.ToString("N2"));
        }
    }
}
