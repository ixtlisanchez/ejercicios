Ejercicios de programación 
Sánchez González Ixtli Xochitl 

Calcular el área de un círculo.

import java.util.Scanner;
public class AreaCirculo1 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Por favor Ingrese el radio del círculo: ");
        double radio = scanner.nextDouble();

        double area = Math.PI * Math.pow(radio, 2);

        System.out.println("El área del círculo que ingreso es: " + area);
    }
}


Verificar si un número es par o impar.

import java.util.Scanner;
public class ParOImpar {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese un número: ");
        int numero = scanner.nextInt();

        if (numero % 2 == 0) {
            System.out.println(numero + " es un número par.");
        } else {
            System.out.println(numero + " es un número impar.");
        }
    }
}


Encontrar el mínimo de tres números.

import java.util.Scanner;
public class MinimoDeTresNumeros {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese el primer número: ");
        int num1 = scanner.nextInt();
        System.out.print("Ingrese el segundo número: ");
        int num2 = scanner.nextInt();
        System.out.print("Ingrese el tercer número: ");
        int num3 = scanner.nextInt();

        int minimo = Math.min(Math.min(num1, num2), num3);

        System.out.println("El mínimo de los tres números es: " + minimo);
    }
}

Calcular la suma de los dígitos de un número.

import java.util.Scanner;
public class SumaDigitos {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese un número: ");
        int numero = scanner.nextInt();

        int suma = 0;
        while (numero > 0) {
            suma += numero % 10;
            numero /= 10;
        }

        System.out.println("La suma de los dígitos es: " + suma);
    }
}


Generar una secuencia de Fibonacci.

import java.util.Scanner;
public class Fibonacci {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese la longitud de la secuencia Fibonacci: ");
        int n = scanner.nextInt();

        int a = 0, b = 1;

        System.out.println("Secuencia Fibonacci:");
        for (int i = 0; i < n; i++) {
            System.out.print(a + " ");
            int temp = a;
            a = b;
            b = temp + b;
        }
    }
}


Verificar si un número es positivo, negativo o cero.

import java.util.Scanner;
public class PositivoNegativoCero {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese un número: ");
        double numero = scanner.nextDouble();

        if (numero > 0) {
            System.out.println("El número es positivo.");
        } else if (numero < 0) {
            System.out.println("El número es negativo.");
        } else {
            System.out.println("El número es cero.");
        }
    }
}

Calcular el promedio de un arreglo de números.

public class PromedioArreglo {
    public static void main(String[] args) {
        int[] numeros = {10, 20, 30, 40, 50};
        int suma = 0;

        for (int numero : numeros) {
            suma += numero;
        }

        double promedio = (double) suma / numeros.length;
        System.out.println("El promedio es: " + promedio);
    }
}

Encontrar el máximo común divisor de dos números.

import java.util.Scanner;
public class MaximoComunDivisor {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese el primer número: ");
        int num1 = scanner.nextInt();
        System.out.print("Ingrese el segundo número: ");
        int num2 = scanner.nextInt();

        int mcd = gcd(num1, num2);

        System.out.println("El máximo común divisor es: " + mcd);
    }

    // Método para calcular el máximo común divisor utilizando el algoritmo de Euclides
    public static int gcd(int a, int b) {
        if (b == 0) {
            return a;
        } else {
            return gcd(b, a % b);
        }
    }
}

Calcular el número de dígitos en un número entero.

import java.util.Scanner;

public class NumeroDeDigitos {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese un número entero: ");
        int numero = scanner.nextInt();

        int numDigitos = String.valueOf(numero).length();

        System.out.println("El número de dígitos es: " + numDigitos);
    }
}

Verificar si un año es bisiesto o no.

import java.util.Scanner;

public class AnoBisiesto {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese un año: ");
        int ano = scanner.nextInt();

        boolean esBisiesto = (ano % 4 == 0 && ano % 100 != 0) || (ano % 400 == 0);

        if (esBisiesto) {
            System.out.println(ano + " es un año bisiesto.");
        } else {
            System.out.println(ano + " no es un año bisiesto.");
        }
    }
}
