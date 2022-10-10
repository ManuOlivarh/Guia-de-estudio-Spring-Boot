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


## ¿Cuál es la ventaja de usar Spring ?
Algunas de las ventajas de usar Spring  son:
-	Spring Framework ofrece una función de inyección de dependencias que permite que los objetos definan sus propias dependencias que el contenedor de Spring luego les inyecta. Esto permite a los desarrolladores crear aplicaciones modulares que consisten en componentes débilmente acoplados que son ideales para microservicios y aplicaciones de red distribuidas.
- 
-	Reduce la cantidad de código repetitivo, como inicializar objetos, abrir/cerrar recursos. Ejemplo: La clase JdbcTemplate  nos ayuda a eliminar todo el código estándar que viene con la programación JDBC.
-	Spring Framework se divide en varios módulos, nos ayuda a mantener nuestra aplicación liviana. Por ejemplo, si no necesitamos las funciones de gestión de transacciones de Spring, no necesitamos agregar esa dependencia a nuestro proyecto.



## Beneficios de las botas de resorte
Spring Boot tiene una serie de características que lo hacen ideal para el desarrollo rápido de aplicaciones Java, incluida la configuración automática, las comprobaciones de estado y las dependencias obstinadas.


| Caracteristica | Beneficio |
| ------ | ------ |
| Servidores integrados | Viene con servidores de aplicaciones preconstruidos Tomcat, Jetty y Undertow que no requieren instalación adicional para su uso. Esto también proporciona implementaciones más rápidas y eficientes que dan como resultado tiempos de reinicio más cortos.|
| Autoconfigurable Drive | Spring y otros frameworks de terceros se configurarán automáticamente. |
| Funciones similares a las de producción | Health checks, métricas y configuraciones externalizadas.|
| Dependencias Iniciales | Esto proporcionará dependencias obstinadas diseñadas para simplificar la configuración de compilación. Esto también proporciona una flexibilidad completa de la herramienta de construcción (Maven y Gradle).|

	
	
	
	
¿Cómo funciona Spring Boot?
Algunos pueden preguntarse cómo Spring Boot tiene configuraciones automáticas y qué significa eso realmente. Realmente se reduce a tres simples anotaciones de Spring Boot que brindan esta función:

@SpringBootApplication
@EnableAutoConfiguration
@ComponentScan
Entre cada una de estas anotaciones, Spring Boot puede proporcionar dependencias de proyectos predeterminadas y permitir que se sobrescriban los valores predeterminados.

@SpringBootApplication
@SpringBootApplication se usa en el punto de entrada de la aplicación, agregue la clase en la que reside debe tener el método principal de la aplicación. La anotación es necesaria y proporcionará cada una de las otras dos anotaciones a su aplicación Spring Boot, ya que @SpringBootApplication incluye ambas en su interior.

@EnableAutoConfiguration
@EnableAutoConfiguration hace solo que proporciona a cada una de las clases representativas la capacidad de configuración automática.

@ComponentScan
Por último, @ComponentScan en la inicialización escaneará todos los beans y las declaraciones de paquetes.

Dependencias de Spring Starter
Spring Boot no solo incluye anotaciones, sino que también usa Spring Starter Dependencies para garantizar que su aplicación comience con las dependencias correctas y que pueda comenzar a trabajar, por así decirlo.

Muchas veces, a medida que una aplicación crece, puede ser difícil configurar correctamente las dependencias del proyecto, los complementos de Spring Boot Starter ayudarán a facilitar la gestión de dependencias. Un ejemplo de dependencias Spring Starter es la dependencia web Spring Boot Starter.

Eso se puede usar para que su aplicación pueda tener Rest Endpoints escritos en su aplicación. En general, ayudan a agilizar el desarrollo de estas aplicaciones para que un equipo comience desde un punto más complejo y se presenten menos agujeros, especialmente con aplicaciones más grandes.

[Fuente](https://www.jrebel.com/blog/what-is-spring-boot)

