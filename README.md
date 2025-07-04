//pila
using System;
using System.Collections.Generic;

public class EjemploLista
{
    public static void Main(string[] args)
    {
        // Crear una lista de enteros
        List<int> numeros = new List<int>();

        // Añadir elementos a la lista
        numeros.Add(10);
        numeros.Add(20);
        numeros.Add(30);

        Console.WriteLine("Elementos en la lista:");
        foreach (int numero in numeros)
        {
            Console.WriteLine(numero);
        }
    }
}

2.Buscar un elemento en un diccionario
using System;
using System.Collections.Generic;

public class EjemploDiccionario
{
    public static void Main(string[] args)
    {
        // Crear un diccionario de nombres y edades
        Dictionary<string, int> edades = new Dictionary<string, int>();

        // Añadir elementos al diccionario
        edades.Add("Alice", 30);
        edades.Add("Bob", 21);
        edades.Add("Charlie", 35);

        // Buscar la edad de Bob
        if (edades.TryGetValue("Bob", out int edadBob))
        {
            Console.WriteLine($"La edad de Bob es: {edadBob}");
        }
        else
        {
            Console.WriteLine("Bob no se encontró en el diccionario.");
        }

        // Intentar buscar a David (no existe)
        if (edades.TryGetValue("David", out int edadDavid))
        {
            Console.WriteLine($"La edad de David es: {edadDavid}");
        }
        else
        {
            Console.WriteLine("David no se encontró en el diccionario.");
        }
    }
}

3.Eliminar un elemento de una cola (Queue<T>)
using System;
using System.Collections.Generic;

public class EjemploCola
{
    public static void Main(string[] args)
    {
        // Crear una cola de cadenas
        Queue<string> pedidos = new Queue<string>();

        // Añadir elementos a la cola
        pedidos.Enqueue("Pizza");
        pedidos.Enqueue("Hamburguesa");
        pedidos.Enqueue("Ensalada");

        Console.WriteLine("Pedidos actuales:");
        foreach (string pedido in pedidos)
        {
            Console.WriteLine(pedido);
        }

        // Atender el primer pedido (eliminar de la cola)
        string primerPedido = pedidos.Dequeue();
        Console.WriteLine($"\nAtendiendo: {primerPedido}");

        Console.WriteLine("Pedidos restantes:");
        foreach (string pedido in pedidos)
        {
            Console.WriteLine(pedido);
        }
    }
}

4.Insertar un elemento en una pila (stack<T>)
using System;
using System.Collections.Generic;

public class EjemploPila
{
    public static void Main(string[] args)
    {
        // Crear una pila de enteros
        Stack<int> libros = new Stack<int>();

        // Añadir elementos a la pila (simulando apilar libros)
        libros.Push(101); // Libro 101
        libros.Push(102); // Libro 102
        libros.Push(103); // Libro 103

        Console.WriteLine("Libros en la pila (de arriba a abajo):");
        foreach (int libro in libros)
        {
            Console.WriteLine(libro);
        }

        // Sacar el último libro añadido (simulando desapilar)
        int ultimoLibro = libros.Pop();
        Console.WriteLine($"\nSe ha sacado el libro: {ultimoLibro}");

        Console.WriteLine("Libros restantes en la pila:");
        foreach (int libro in libros)
        {
            Console.WriteLine(libro);
        }
    }
}
5.Recorrer los elementos de un conjunto (hasheSet<T>)
using System;
using System.Collections.Generic;

public class EjemploHashSet
{
    public static void Main(string[] args)
    {
        // Crear un conjunto de cadenas
        HashSet<string> frutas = new HashSet<string>();

        // Añadir elementos al conjunto
        frutas.Add("Manzana");
        frutas.Add("Banana");
        frutas.Add("Naranja");
        frutas.Add("Manzana"); // Intentar añadir "Manzana" de nuevo, no se agregará

        Console.WriteLine("Frutas en el conjunto:");
        // Recorrer los elementos del conjunto
        foreach (string fruta in frutas)
        {
            Console.WriteLine(fruta);
        }

        // Verificar si una fruta existe
        if (frutas.Contains("Banana"))
        {
            Console.WriteLine("\nEl conjunto contiene Banana.");
        }

        if (frutas.Contains("Uva"))
        {
            Console.WriteLine("El conjunto contiene Uva.");
        }
        else
        {
            Console.WriteLine("El conjunto NO contiene Uva.");
        }
    }
}

