# <center> Visual Studio
# Iniciar Consola
1. crear proyecto
2. c# | Windows | Consola
3. **seleccionar** Aplicacion de consola .net network
4. siguiente
5. **renombrar** pruebaConsola
6. crear

## En el proyecto
### Inicio a C#
```c#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace pruebaConsola
{
    public class Program
    {
        static void Main(string[] args)
        {
            //declara variables
            string nom = "", ape = "";
            //variables numericas
            int num1 = 0, num2 = 0, res = 0;
            float n1 = 0, n2 = 0;
            double d1 = 0, d2 = 0;
            //boolean
            bool existe = false;

            //vector de 5 valores
            string[] nombres = new string[5];

            //lista
            List<double> valores = new List<double>();

            //condicionales
            num1 = 7;
            num2 = 6;
            if (num1 > num2) {
                //mensaje a la pantalla "consola"
                Console.WriteLine("numero 1 es mayor");
            }else if (num1 == num2){
                Console.WriteLine("son iguales");
            }else{
                Console.WriteLine("numero 1 es menor");
            }

            //switch
            switch (nom)
            {
                case "juan":
                    Console.WriteLine("su nombre es juan");
                    break;
                case "pedro":
                    Console.WriteLine("su nombre es pedro");
                    break;
                default:
                    Console.WriteLine("sin nombre");
                    break;
            }

            // - Ciclos
            //for
            for (int i = 0; i < 10; i++) {
                Console.WriteLine(i);
            }

            //while
            int cont = 0;
            while (cont < 6)
            {
                Console.WriteLine(cont);
                cont++;
            }

            //foreach
            foreach (string n in nombres)
            {
                Console.WriteLine(n);
            }

            //do while
            do
            {
                Console.WriteLine(cont);
            } while (cont < 5);
        }
    }
}
```

### metodos / funciones + ejercicio:
```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace pruebaConsola
{
    public class Program
    {
        static void Main(string[] args)
        {
            menu();
        }

        public static void menu()
        {
            string op = "";
            Console.WriteLine("### Menu de Opciones ###");
            Console.WriteLine("1. Binario a decimal");
            Console.WriteLine("2. Decimal a binario");
            Console.WriteLine("3. Octal a decimal");
            Console.WriteLine("4. Decimal a octal");
            Console.WriteLine("5. Salir");
            Console.WriteLine();
            Console.WriteLine("Ingrese una opcion valida (1-5)");
            //conversion String a entero
            op = Console.ReadLine();

            switch (op)
            {
                case "1":
                    binario_decimal();
                    break;
                case "2":
                    decimal_binario();
                    break;
                case "3":
                    octal_decimal();
                    break;
                case "4":
                    decimal_octal();
                    break;
                case "5":
                    salir();
                    break;
                default:
                    Console.WriteLine("Ingrese una opcion valida");
                    break;

            }
        }

        private static void salir()
        {
            Console.WriteLine("No' vemo' gile conchetumareeeeee");
        }

        private static void decimal_octal()
        {
            Console.Write("Ingrese un numero decimal: ");
            if (int.TryParse(Console.ReadLine(), out int numDecimal))
            {
                // Convert.ToString con base 8 convierte un entero a su representación octal en texto
                string octal = Convert.ToString(numDecimal, 8);
                Console.WriteLine($"El resultado en octal es: {octal}");
            }
            else
            {
                Console.WriteLine("Error: Debe ingresar un numero entero valido.");
            }
            reiniciar();
        }

        private static void octal_decimal()
        {
            Console.Write("Ingrese un numero octal (ej. 57): ");
            string octal = Console.ReadLine();

            try
            {
                // Convert.ToInt32 con base 8 convierte una cadena octal a un entero decimal
                int decimalResult = Convert.ToInt32(octal, 8);
                Console.WriteLine($"El resultado en decimal es: {decimalResult}");
            }
            catch (FormatException)
            {
                Console.WriteLine("Error: El valor ingresado no es un numero octal valido (digitos del 0 al 7).");
            }
            catch (OverflowException)
            {
                Console.WriteLine("Error: El numero es demasiado grande.");
            }
            reiniciar();
        }

        private static void decimal_binario()
        {
            Console.Write("Ingrese un numero decimal: ");
            if (int.TryParse(Console.ReadLine(), out int numDecimal))
            {
                // Convert.ToString con base 2 convierte un entero a su representación binaria en texto
                string binario = Convert.ToString(numDecimal, 2);
                Console.WriteLine($"El resultado en binario es: {binario}");
            }
            else
            {
                Console.WriteLine("Error: Debe ingresar un numero entero valido.");
            }
            reiniciar();
        }

        private static void binario_decimal()
        {
            Console.Write("Ingrese un numero binario (ej. 1011): ");
            string binario = Console.ReadLine();

            try
            {
                // Convert.ToInt32 permite convertir una cadena en base 2 a un entero decimal
                int decimalResult = Convert.ToInt32(binario, 2);
                Console.WriteLine($"El resultado en decimal es: {decimalResult}");
            }
            catch (FormatException)
            {
                Console.WriteLine("Error: El valor ingresado no es un numero binario valido (solo debe contener 0 y 1).");
            }
            catch (OverflowException)
            {
                Console.WriteLine("Error: El numero es demasiado grande para ser procesado.");
            }
            reiniciar();
        }

        private static void reiniciar()
        {
            Console.WriteLine();
            menu();
        }
    }
}

```

# Iniciar JFrame
1. crear proyecto
2. c# | Windows | Escritorio
3. **seleccionar** Aplicacion de windows Forms
4. siguiente
5. **renombrar** Form1
6. crear
## En el proyecto

esa vaina se borro nose que paso pero ibamos a hacer una calculadora cientifica, si esto sigue con este texto significa que nunca la hicimos por que no hacia falta, a la final solo era para demostrar que se podia trabajar con Jframe


# SQL management
1. new query
2. sql
```sql
create database prueba3315298
```
```sql
use prueba3315298
```
crear la base
```sql
create table usuario(
	usuarioId int identity primary key,
	userName varchar(20) not null unique,
	pass varchar(20) not null
);
create table encargado(
	encargadoId int identity primary key,
	documento varchar(15) not null unique,
	nombres varchar(50) not null,
	apellidos varchar(50) not null,
	correo varchar(60) not null unique
);
create table ambiente(
	ambienteId int identity primary key,
	codigo varchar(10) not null unique,
	nombre varchar(20) not null unique,
	encargadoId int not null,
	CONSTRAINT amb_enc FOREIGN KEY (encargadoId) REFERENCES encargado(encargadoId)
);
```
