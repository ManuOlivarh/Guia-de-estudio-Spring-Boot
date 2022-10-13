# Guia de estudio Spring Boot


## Introducción

Esta guía de estudio esta orientada a estudiantes y desarrolladores de Spring, que quieran aprender o estudiar la teoria y los conceptos principales de esta tecnología, todos estos conceptos fueron recopilados de distintas páginas y traducidos al español para que sea de mejor comprensión para los estudiantes de habla hispana. :)


## ¿Qué es Java Spring Boot?
Java Spring Framework (Spring Framework) es un marco popular, de código abierto y de nivel empresarial para crear aplicaciones independientes de nivel de producción que se ejecutan en la máquina virtual de Java (JVM).

Java Spring Boot (Spring Boot) es una herramienta que hace que el desarrollo de aplicaciones web y microservicios con Spring Framework sea más rápido y fácil a través de tres capacidades principales:

- Autoconfiguración
- Un enfoque obstinado de la configuración
- La capacidad de crear aplicaciones independientes

Estas características funcionan juntas para brindarle una herramienta que le permite configurar una aplicación basada en Spring con una configuración y configuración mínimas.

[Fuente](https://www.ibm.com/cloud/learn/java-spring-boot)


## ¿Cuál es la ventaja de usar Spring Boot?
Algunas de las ventajas de usar Spring  son:
-	Spring Framework ofrece una función de inyección de dependencias que permite que los objetos definan sus propias dependencias que el contenedor de Spring luego les inyecta. Esto permite a los desarrolladores crear aplicaciones modulares que consisten en componentes débilmente acoplados que son ideales para microservicios y aplicaciones de red distribuidas. 
-	Reduce la cantidad de código repetitivo, como inicializar objetos, abrir/cerrar recursos. Ejemplo: La clase JdbcTemplate  nos ayuda a eliminar todo el código estándar que viene con la programación JDBC.
-	Spring Framework se divide en varios módulos, nos ayuda a mantener nuestra aplicación liviana. Por ejemplo, si no necesitamos las funciones de gestión de transacciones de Spring, no necesitamos agregar esa dependencia a nuestro proyecto.
[Fuente](https://www.ibm.com/cloud/learn/java-spring-boot)



## Otros Beneficios de Spring Boot
Spring Boot tiene una serie de características que lo hacen ideal para el desarrollo rápido de aplicaciones Java, incluida la configuración automática, las comprobaciones de estado y las dependencias obstinadas.


| Caracteristica | Beneficio |
| ------ | ------ |
| Servidores integrados | Viene con servidores de aplicaciones preconstruidos Tomcat, Jetty y Undertow que no requieren instalación adicional para su uso. Esto también proporciona implementaciones más rápidas y eficientes que dan como resultado tiempos de reinicio más cortos.|
| Autoconfigurable Drive | Spring y otros frameworks de terceros se configurarán automáticamente. |
| Funciones similares a las de producción | Health checks, métricas y configuraciones externalizadas.|
| Dependencias Starter | Esto proporcionará dependencias obstinadas diseñadas para simplificar la configuración de compilación. Esto también proporciona una flexibilidad completa de la herramienta de construcción (Maven y Gradle).|	
	
## ¿Cómo funciona Spring Boot?
Algunos pueden preguntarse cómo Spring Boot tiene configuraciones automáticas y qué significa eso realmente. Realmente se reduce a tres simples anotaciones de Spring Boot que brindan esta función:

```sh
@SpringBootApplication
@EnableAutoConfiguration
@ComponentScan
```

![alt text](https://www.arquitecturajava.com/wp-content/uploads/spring-application-herencia.png)

[Fuente](https://www.arquitecturajava.com/springbootapplication-una-anotacion-clave/)

**@SpringBootApplication** Es la anotación que aparece en la función main de todo proyecto que definamos con Spring Boot. Ahora bien la mayor parte de los desarrolladores no saben exactamente para que sirve esta anotación y como funciona. Vamos a explicarlo. La anotación @SpringBootApplication es una combinación de las siguientes tres anotaciones de Spring y proporciona la funcionalidad de las tres con solo una línea de código:
[Fuente](https://dzone.com/articles/the-springbootapplication-annotation-example-in-ja)

**@Configuration:** Disponible a partir de la versión 3 de Spring, nos ofrece la posibilidad de realizar una notación que será la encargada de definir a la clase que lo posea como una clase de configuración. Esta configuración para el framework de Spring, estará basada en anotaciones. Y no como en sus orígenes, que estaba basada en XML, lo que lo hacía más complejo. La finalidad de dicha anotación también será el permitir realizar la inyección de dependencias.

**@EnableAutoConfiguration:** La configuración automática de Spring Boot, intenta configurar automáticamente su aplicación Spring en función de las dependencias jar que haya agregado. Si por ejemplo, si HSQLDB (sistema gestor de bases de datos) está en su ruta de clase y no ha configurado manualmente ningún bean de conexión de base de datos, Spring Boot configura automáticamente una base de datos en memoria.

**@ComponentScan:** Se utiliza junto a @Configuration para indicar a Spring donde debe buscar los componentes y será dentro del package que tenemos anotado. Por solo tener que anotarla una vez, poder hacer que todos los packages sean hijos del package de la clase padre (el que contenga el main).

Entre cada una de estas anotaciones, Spring Boot puede proporcionar dependencias de proyectos predeterminadas y permitir que se sobrescriban los valores predeterminados.
[Fuente](https://javadesde0.com/anotacion-springbootapplication/)


## Dependencias de Spring Starter
Spring Boot no solo incluye anotaciones, sino que también usa Spring Starter Dependencies para garantizar que su aplicación comience con las dependencias correctas y que pueda comenzar a trabajar, por así decirlo.

Muchas veces, a medida que una aplicación crece, puede ser difícil configurar correctamente las dependencias del proyecto, los complementos de Spring Boot Starter ayudarán a facilitar la gestión de dependencias. Un ejemplo de dependencias Spring Starter es la dependencia web Spring Boot Starter.

Eso se puede usar para que su aplicación pueda tener Rest Endpoints escritos en su aplicación. En general, ayudan a agilizar el desarrollo de estas aplicaciones para que un equipo comience desde un punto más complejo y se presenten menos agujeros, especialmente con aplicaciones más grandes.

[Fuente](https://www.jrebel.com/blog/what-is-spring-boot)



## Inversión de control
La inversión de control es un principio de programación que significa ceder el control de un objeto a otro objeto que sabe cómo manejarlo. Este principio se utiliza en algunos marcos, como Spring.

Es un patrón de diseño que rompe las dependencias entre objetos y en su lugar depende de abstracciones. La inversión de control se puede lograr a través de la inyección de dependencia, una técnica para separar los componentes de software de las preocupaciones o responsabilidades.
[Fuente](https://medium.com/@nirmalkumar8273/inversion-of-control-and-dependency-injection-in-spring-framework-e8e40b9afd8d)


En los siguiente video se explica de forma mas detallada el concepto:

**Video 1:**

[![Alt text](https://img.youtube.com/vi/dAAB2EqMiC4/0.jpg)](https://www.youtube.com/watch?v=dAAB2EqMiC4)


## Inyección de dependencia
La inyección de dependencia es un subtipo de inversión de control y se implementa mediante inyección de constructor, inyección de setter o inyección de método y se ocupa de cómo los componentes obtienen sus dependencias.

Es un proceso en el que los objetos definen sus dependencias a través de argumentos de constructor, argumentos de un método de fábrica o propiedades que se establecen en la instancia del objeto después de que se construye o se devuelve desde un método de fábrica. Luego, el contenedor inyecta esas dependencias cuando crea el bean. Este proceso es fundamentalmente el inverso del propio bean que controla la creación de instancias o la ubicación de sus dependencias por sí mismo mediante la construcción directa de clases o el patrón de Localizador de servicios . de ahí el nombre Inversión de Control.

La inversión de control es un principio por el cual el control de los objetos se transfiere a un contenedor o marco. La inyección de dependencia es un patrón a través del cual se implementa IoC y el acto de conectar objetos con otros objetos o inyectar objetos en objetos lo realiza el contenedor en lugar del objeto en sí.
[Fuente](https://medium.com/@nirmalkumar8273/inversion-of-control-and-dependency-injection-in-spring-framework-e8e40b9afd8d)

[![Alt text](https://img.youtube.com/vi/gGkeH38XMLk/0.jpg)](https://www.youtube.com/watch?v=gGkeH38XMLk)


## En Spring Framework hay dos tipos de inyección de dependencia: -

**Inyección de constructor:** esto se logra cuando el contenedor invoca un constructor con una serie de argumentos, cada uno de los cuales representa una dependencia, es decir, todas las dependencias se declaran en un solo paso. Esto ayuda a comprender si la clase depende de demasiados servicios. La inyección de constructor es la mejor práctica para inyectar dependencias.
[Fuente](https://medium.com/@nirmalkumar8273/inversion-of-control-and-dependency-injection-in-spring-framework-e8e40b9afd8d)


**Inyección Setter:** esto se logra mediante el contenedor que llama a los métodos setter en sus beans después de invocar un constructor sin argumentos o un método de fábrica estático sin argumentos para crear una instancia de su bean. El contenedor llamará a los métodos setter de nuestra clase. Los objetos de la clase tendrán setters. El contenedor IoC utilizará estos configuradores para proporcionar el recurso en tiempo de ejecución. Se utiliza para dependencias opcionales.
[Fuente](https://medium.com/@nirmalkumar8273/inversion-of-control-and-dependency-injection-in-spring-framework-e8e40b9afd8d)

## ¿Por qué necesitamos inyección de dependencia?
La inyección de dependencia proporciona los objetos que necesita un objeto. Entonces, en lugar de que las dependencias se construyan por sí mismas, se inyectan por algún medio externo. Por ejemplo, tenemos una clase llamada "Cliente" que usa una clase "Registrador" para registrar errores. Entonces, en lugar de crear el "Registrador" desde dentro de la clase, podemos inyectar el mismo a través de un constructor como se muestra a continuación.

El mayor beneficio logrado por este enfoque es el "desacoplamiento". Podemos invocar el objeto del cliente y pasar cualquier tipo de objeto "Registrador".

[Fuente](https://medium.com/@nirmalkumar8273/inversion-of-control-and-dependency-injection-in-spring-framework-e8e40b9afd8d)

## Que es un Bean?

Spring Bean es el concepto clave o la columna vertebral de Spring Framework. Spring Bean es el objeto cuyo ciclo de vida es administrado por Spring IoC. Es importante entenderlo antes de trabajar con Spring Framework. En palabras simples, Spring Bean es el bloque de construcción central para cualquier aplicación Spring

En Spring, los objetos que forman la columna vertebral de su aplicación y que son administrados por el contenedor Spring IoC se denominan beans. Un bean es un objeto que es instanciado, ensamblado y administrado por un contenedor Spring IoC. De lo contrario, un bean es uno de los muchos objetos de su aplicación. Los beans y las dependencias entre ellos se reflejan en los metadatos de configuración utilizados por un contenedor.

El concepto más importante al trabajar en los beans es el contenedor IoC. El contenedor Spring IoC es el sistema de gestión central de Spring Framework. Es responsable de crear, configurar y administrar el ciclo de vida de estos objetos. El contenedor obtiene sus instrucciones sobre qué objetos instanciar, configurar y ensamblar al leer los metadatos de configuración proporcionados en forma de configuraciones XML o anotaciones. Le permite expresar los objetos que componen su aplicación y las ricas interdependencias entre dichos objetos. Veamos el flujo de trabajo de alto nivel del contenedor Spring Ioc.


![alt text](https://prod-acb5.kxcdn.com/wp-content/uploads/2017/11/Spring-IoC-container.png.webp)
Para una mejor comprensión, tomemos el siguiente ejemplo:

El Cliente(Customer) de nuestra tienda online.
Los Pedidos(Orders) realizados por Clientes en nuestra tienda online.
Una clase de dominio típica se verá así:

```sh
@Component
public class Customer{
    private String firstName;
    private String lastName;
    private List orders;
  
    //getter and setter
}

@Component
public class Order{
    private String code;
    private double total;
    private double tax;
    private Product product;
    private Customer owner;

    //getter and setter
}
```
[Fuente](https://www.javadevjournal.com/spring/what-is-a-spring-bean/)
