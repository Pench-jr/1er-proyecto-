package bloque3;
import java.util.Scanner;
public class Proyec_final {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        Scanner teclado=new Scanner(System.in);
        double edad = 0, peso = 0;
        double kg = 0, altu = 0;
        byte num = 0;
        
        System.out.println("***************************");
        System.out.println("* EN QUE TE PUEDO AYUDAR? *");
        System.out.println("***************************\n");
        System.out.println("1) Puedes entrar al club?\n\n2)Puedes donar sangre\n\n3)Como estas de peso?\n\n4)Convercion de unidades\n\n5)Calculadora de areas\n");
        System.out.print("Elije una opcion -> ");
        num = (byte) teclado.nextInt();
        
        switch(num)
        {
        
        
        
        
        
        case 1:
        	edad = 0;
        	System.out.println("Cual es tu edad?");
        	edad = teclado.nextInt();
        	if (edad >= 18)
        		System.out.println("Puedes entrar al Club");
        break;
        
        
        
        
        
        case 2:
        	 System.out.println("ingresa tu edad");
        	 edad = teclado.nextDouble();
        	 System.out.println("ingresa tu peso en kg");
        	 peso = teclado.nextInt();
        	 if (edad>=18) if (edad<65) if (peso>50)
        	 {
        		 System.out.println("Eres apto para donar sangre");
        	 }
        	 else 
        	 {
        		 System.out.println("No eres apto para donar sangre");
        	 }
        break;
        
        
        
        
        
        case 3:
        	double imc = 0;
        	String clasificacion = null;
        	System.out.println("cual es tu peso en kg?");
        	kg = teclado.nextDouble();
        	System.out.println("Cual es tu altura en metros?");
        	altu = teclado.nextDouble();
        	imc = kg/(altu*altu);
        	if (imc<18.5)
        	{
        		clasificacion ="peso bajo";
        	}
        	else if (imc>=18.5 && imc<=24.9)
        	{
        		clasificacion ="peso normal";
        	}
        	else if (imc>=25 && imc<=29.9)
        	{
        		clasificacion ="sobrepeso";
        	}
        	else if (imc>30)
        	{
        		clasificacion ="obesidad";
        	}
        	System.out.println("clasificacion: "+clasificacion);
        break;
        
        
        
        
        
        case 4:
              int opcion1 = -1;

              while (opcion1 != 0) {
              System.out.println("\n--- CONVERSOR DE UNIDADES ---");
        	  System.out.println("1) Celsius a Fahrenheit");
        	  System.out.println("2) Kilómetros a Millas");
        	  System.out.println("3) Kilogramos a Libras");
        	  System.out.println("0) Salir");
        	  System.out.print("Elija una opción: ");
        	  opcion1 = teclado.nextInt();

        	  switch (opcion1) {
              case 1:
        	  System.out.print("Ingrese grados Celsius: ");
        	  double celsius = teclado.nextDouble();
        	  double fahrenheit = (celsius * 9/5) + 32;
        	  System.out.println(celsius + " *C  -> "+ fahrenheit+" F");
        	  break;
        	                
        	  case 2:
        	  System.out.print("Ingrese kilómetros: ");
        	  double kilometros = teclado.nextDouble();
        	  double millas = kilometros * 0.621371;
        	  System.out.println(kilometros+" km  ->  " +millas+" mi");
        	  break;
        	                
        	  case 3:
        	  System.out.print("Ingrese kilogramos: ");
        	  double kilogramos = teclado.nextDouble();
        	  double libras = kilogramos * 2.20462;
        	  System.out.println(kilogramos+" kg  ->  "+ libras+" lb");
        	  break;
        	                
        	  case 0:
        	  System.out.println("Conversor finalizado.");
        	  break;
        	                
        	  default:
        	  System.out.println("Opción inválida.");
        	 }
        	 }	
        break;
        
        
        
        
        
        case 5:
        	int opcion;
            double area;

            do {
                System.out.println("Calculadora de Áreas de Figuras Geométricas");
                System.out.println("1. Círculo");
                System.out.println("2. Triángulo");
                System.out.println("3. Cuadrado");
                System.out.println("4. Rectángulo");
                System.out.println("5. Salir");
                System.out.print("Elige una opción: \n");
                opcion = teclado.nextInt();

            switch (opcion) 
            {
            case 1: // Círculo
                System.out.print("Introduce el radio del círculo: ");
                double radio = teclado.nextDouble();
                area = 3.1416 * radio * radio;
                System.out.println("El área del círculo es: " + area);
                System.out.println();
            break;

            case 2: // Triángulo
                 System.out.print("Introduce la base del triángulo: ");
                 double base = teclado.nextDouble();
                 System.out.print("Introduce la altura del triángulo: ");
                 double altura = teclado.nextDouble();
                 area = (base * altura) / 2;
                 System.out.println("El área del triángulo es: " + area);
                 System.out.println();
            break;

            case 3: // Cuadrado
                 System.out.print("Introduce el lado del cuadrado: ");
                 double lado = teclado.nextDouble();
                 area = lado * lado;
                 System.out.println("El área del cuadrado es: " + area);
                 System.out.println();
            break;

            case 4: // Rectángulo
                 System.out.print("Introduce la base del rectángulo: ");
                 double baseRectangulo = teclado.nextDouble();
                 System.out.print("Introduce la altura del rectángulo: ");
                 double alturaRectangulo = teclado.nextDouble();
                 area = baseRectangulo * alturaRectangulo;
                 System.out.println("El área del rectángulo es: " + area);
                 System.out.println();
           break;

           case 5:
                System.out.println("Saliste de la calculadora de áreas.");
           break;

           default:
           System.out.println("Opción inválida, por favor elige una opción correcta.");
           }

               } while (opcion != 5);
        break;
        }
        
}
}
