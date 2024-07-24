# Proyecto de Calculadora de IMC
 <p align=center><img src=images/unnamed%20(3).pngwidth="300" ><p>
---

## Índice
 <details>
  <summary> Descripción del proyecto</summary>
 - Motivación
	 
Mi proyecto consta de la creación de una calculadora de IMC (Índice de Masa Corporal) que compare el resultado obtenido en cada ciclo con los valores normales de IMC correspondientes a los valores de OMS (Organización mundial de la Salud) en personas adultas.


La idea surge cuando en mi trabajo conozco a quien llamaré Cris, quien padece un trastorno alimenticio por lo que debe ser pesada todos los días en ayunas y después de comer. En su caso es un proceso muy difícil y traumático cada vez que debe hacerlo, no puede conocer los valores que maneja en su peso por indicación médica. En base a esta idea, se me ocurrió poder plantear un dispositivo que calcule su IMC en base a su peso y altura, pero sin devolver valores, solamente que se maneje con los leds y la pantalla serial.

Este proyecto está pensado para personas adultas como Cris, que al ser evaluados por profesionales de salud especializados, podría calcular el IMC para saber si está dentro de valores saludables o no. Dejando de lado lo tortuoso que supone para ellos conocer los valores que manejan mientras llevan a cabo un tratamiento clínico en algún establecimiento especializado. 

</details>

  
  <details>
  <summary>  ¿Qué es el IMC?</summary>
  - El Índice de Masa Corporal (IMC) es una medida que relaciona la masa y la altura de un individuo, utilizada como indicador de la salud. Esta se calcula como Peso / Estatura² = IMC
   
</details>

<details>
  <summary># Metodología e Instrumental</summary>
  Arduino UNO es una placa basada en el microcontrolador ATmega328P. Tiene 14 pines de entrada/salida digital (de los cuales 6 pueden ser usando con PWM), 6 entradas analógicas, un cristal de 16Mhz, conexión USB, conector jack de alimentación, terminales para conexión ICSP y un botón de reseteo. Tiene toda la electrónica necesaria para que el microcontrolador opere, simplemente hay que conectarlo a la energía por el puerto USB ó con un transformador AC-DC
	
Si bien para este proyecto se usó una simulación a través del software Proteus, me pareció importante explicarla.
       # ¿Cómo está creado el proyecto?
           Lo que se quiso probar al principio fue implementar una calculadora que sea medianamente interactiva con el usuario.
Al principio opté por usar la pantalla de plasma (lcd), pero más tarde simplemente usé la pantalla serial para lograr esto. 
   Luego de calcular el IMC, otra implementación era la de poder mostrar al usuario un mensaje en donde se le decía que su imc era saludable o que no lo era. Más tarde, opté por llevar esto a cabo también mediante una luz led la cuál considero lo suficientemente gráfica y clara.
         También tenia mis dudas sobre preguntar la opcion de sexo biologico sin que esto pueda dejar al margen a ciertas personas que no se sienten comodas en solo 2 clases, pero visto desde un lado médico y científico se tomaron los parámetros que la OMS maneja (y siendo que esta organizacion suele hacer esta distinción) me pareció mas exacto incluir esta variable para la medición que necesito.


Nuevamente me encontré con la dificultad de no poder recibir de arduino un número de más de un dígito, por lo que me plantee diferentes maneras de poder resolver este problema. Finalmente,  me planteé la idea de que, en lugar de preguntarle al usuario (lo cual es contrario a la filosofía original del proyecto) la placa Arduino debería recabar la información mediante unos sensores de peso y altura que deberían conectarse a ella. Para esta implementación y simulación, lo que se me ocurrió usar fue una variable fina de peso y altura pero me pareció fundamental hacer esta aclaración, dado que no contaba con estos sensores en la simulación. 
Entonces, lo que este proyecto debe hacer es recabar los datos necesarios (que se almacenan en sus respectivas variables), en base a ellos se aplica la fórmula que calcula el imc y almacena este resultado. Luego va a  preguntar al usuario por el sexo biologico para poder medir segun los parametros correctos, Este entonces mide segun sea el caso de A (para f) y B (para m), mostrando  la respuesta esperada “saludable” o “no saludable”.



</details>

<details>
  <summary>Gráficos y Tablas</summary>
  
  - Diagrama de flujo
    <p align=center><img src=images/Screenshot_397.jpg="400" ><p>
  - Diagrama de bloques
    <p align=center><img src=images/Screenshot_396.jpg="400" ><p>
</details>

<details>
  <summary>Conclusión</summary>
  
   Al realizar este proyecto me encontré con ciertas dificultades a la hora de plantearlo, primeramente al ser mi primera experiencia con arduino y lo que eso implica; pero me pareció muy gratificante el poder aprender nuevas cosas e implementación de diversas tecnologías. El ámbito de la salud me parece por demás interesante, y como poder resolver diferentes problemas con los que me he encontrado en mi ámbito laboral con las herramientas que aprendo dia a dia en esta hermosa carrera.

</details>

## Contribuciones
Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para discutir cualquier cambio importante.

## Mis datos
linkedin 
www.linkedin.com/in/nissedgonzalezm

## Gracias por llegar hasta aquí


## Referencias

- [Arduino UNO](https://arduino.cl/arduino-uno/#:~:text=La%20placa%20Arduino%20UNO%20es,de%20toda%20la%20familia%20Arduino.)
- [Índice de Masa Corporal - Wikipedia](https://es.wikipedia.org/wiki/%C3%8Dndice_de_masa_corporal)
- [Organización Mundial de la Salud - IMC](https://www.who.int/entity/dietphysicalactivity/es/index.html)
- [Enterat - IMC](https://www.enterat.com/salud/imc-indice-masa-corporal.php)

