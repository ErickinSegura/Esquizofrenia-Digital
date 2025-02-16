---
Nombre: Erick Segura Sánchez.
Matrícula: A01613821.
---
Links: [[Planeación de Sistemas de Software]]
Fecha: Miércoles 12/Febrero/2025

## Instalación del Contenedor de Docker

![[Pasted image 20250212214041.png]]

La instalación de este contenedor fue de manera muy sencilla gracias al Dockerfile que ya contaba con todas las configuraciones necesarias para su correcto funcionamiento, la unica modificación que fue necesaria hacer fue en la selección de arquitectura ya que por defecto viene la arquitectura AARCH. Además con los archivos bat todo mucho más sencillo de realizar

<div class="page-break" style="page-break-before: always;"></div>

## Calculadora en Java

![[Pasted image 20250212214412.png]]
<div class="page-break" style="page-break-before: always;"></div>

Para la realización de la calculadora igualmente fue muy sencillo, mi unica variación a lo explicado en la clase fue usar nano como editor en vez de vim, ya que estoy más acostumbrado a este, el código para mi calculadora sencilla fue el siguiente:


```java
import java.util.Scanner;

public class Calculadora {

	public static void main(String[] args) {
	
		Scanner scanner = new Scanner(System.in);
		
		System.out.println("Selecciona una operacion:");
		
		System.out.println("1. Sumar");
		
		System.out.println("2. Restar");
		
		System.out.println("3. Multiplicar");
		
		System.out.println("4. Dividir");
		
		int opcion = scanner.nextInt();
		
		System.out.print("Ingresa el primer numero: ");
		
		double num1 = scanner.nextDouble();
		
		System.out.print("Ingresa el segundo numero: ");
		
		double num2 = scanner.nextDouble();
		
		double resultado = 0;
		
		switch (opcion) {
		
			case 1:
			
				resultado = num1 + num2;
				
				System.out.println("El resultado de la suma es: " + resultado);
				
				break;
			
			case 2:
			
				resultado = num1 - num2;
				
				System.out.println("El resultado de la resta es: " + resultado);
				
				break;
			
			case 3:
			
				resultado = num1 * num2;
				
				System.out.println("El resultado de la multiplicacion es: " + resultado);
				
				break;
			
			case 4:
			
				if (num2 != 0) {
				
				resultado = num1 / num2;
				
				System.out.println("El resultado de la division es: " + resultado);
				
				} else {
				
				System.out.println("Error: No se puede dividir por cero.");
				
				}
				
				break;
			
			default:
			
				System.out.println("Opcion no valida.");
			
			}
	
	scanner.close();
	
	}

}
```
