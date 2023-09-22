# TC 1028.414 Proyecto - TAQUERÍA TEC
## CONTEXTO (Avance 1)
Para este proyecto, he decidio basarme en aplicaciones de entrega de alimentos como Rappi, Uber eats, Didi food, etc. El programa desplegará un menú de opciones. En el menú, tendrás la opción de observar la carta de una taquería, en la que se ofrecerá una variedad de sabor de tacos, sabores y tamaños de agua, y complementos como cebollas preparadas y chicharrón de queso para realizar un pedido. En la carta se mostrarán todos los productos y sus precios. La segunda opción del menú será continuar con la realización de tu pedido, donde ingresarás los productos que deseas. Al terminar con tu pedido se preguntará sobre la propina, en caso de agregar propina, se calculará el porcentaje deseado. La tercera opción hará una confirmación y mostrará el total, con o sin propina. Finalmente, el programa terminará con tu pedido con una encuesta de servicio.
## Operadores (Avance 2)
En el programa que estoy trabajando, habrá una sección en la que el usuario podrá consultar cuánto deberá pagar después de realizar su orden, por lo que incluiré operadores para realizar algunos cálculos. Estos cálculos son la suma de los precios de los productos seleccionados, y en caso de que el usuario deseé agregar propina, se hará un segundo cálculo para arrogar el total después de agregar el porcentaje de propina deseado.

Para este avance realicé un código prueba que hace el trabajo de los cálculos de la cuenta total, con o sin propina, del pedido realizado. Al correr el código se pide el ingreso de los productos deseados y sus características (sabor, tamaño, cantidad, precio). Luego, se pregunta al usuario si desea agregar un complemento a su orden, dando dos opciones. El programa buscará un "si" por respuesta (sin importar las mayúsculas o minúsculas) en caso de el usuario deseé un complemento. Si obtiene un "si" por respuesta, se pedirá el complemento y su precio, y calculará el total a pagar agregando el costo del complemento a la cuenta. Si el prgrama no encuentra un "si" por respuesta, seguirá con el código. Después se preguntará al usuario si desea agregar propina. Al igual que la parte del complemento, si el programa recibe un "si" por respuesta, pedirá el ingreso de la propina el porcentaje, calculará la propina, la agregará a la cuenta e imprimirá el total del pedido. Si no desea agregar propina, solo imprimirá el total.

Para la realización de estos cálculos, he agregado las siguientes operaciones al programa:

>**Cálculo del total sin propina (con complemento):**
>
>>**total = (precio_taco * cantidad_tacos) + precio_agua + precio_extra**

>**Cálculo del total con propina:**
>
>>**total = (total * (porcentaje / 100)) + total**

## Funciones (Avance 3)
Como se ha mencionado anteriormente, el programa hará distintas tareas para completar un pedido, como mostrar la carta, resgistrar los productos seleccionados, calcular el total, la propina y confirmar la orden. Declararé una serie de funciones, una para cada tarea, para la facilidad de lectura del código y la realización de cada tarea. 

Agregue al código las siguientes funciones:

>**Mostrar_Menu: Función que muestra el Menú de opciones.**
>
>**Opcion_Menu: Función que evalua la opción dada por el usuario.**
>
>**Mostrar_Carta: Función que muestra la carta de productos y precios de la taquería.**
>
>**Realizar_Pedido: Función que se encarga de registrar el pedido mediante inputs y, haciendo uso de otras funciones, calcula el total tomando en cuenta si el usuario elijó algún complemento y/o decidió agregar propina.**
>
>**Confirmacion_Pedido_Propina: Función que imprime la confirmación del pedido si el usuario decidió agregar propina.**
>
>**Confirmacion_Pedido: Función que imprime la confirmación del pedido si el usuario decidió no agregar propina.**
>
>**Finalizar_Pedido: Función que imprime un mensaje de confirmación, y además muestra la encuesta de servicio, donde se calificará el servicio en una escala del 1 al 5.**
>
>**Complemento: Función que realiza el cálculo del total del pedido con complemento.**
>
>**Total: Función que realiza el cálculo del total del pedido sin complemento.**
>
>**Propina: Función que realiza el cálculo del total del pedido con propina.**

## Estructuras de decisión (Avance 4)
En las funciones principales, declaradas dentro del código de mi programa, utilicé estructuras de decisión con condicionales if. En la función de Opcion_Menu, hice uso de condicionales para determinar cual es la opción que el usuario eligió para así mandar a llamar la función correspondiente a realizar cierta tarea. En las siguientes cuatro funciones (Realizar_Pedido, Confirmacion_Pedido_Propina, Confirmacion_Pedido, Finalizar_Pedido), también utilice condicionales, sin embargo, el trabajo de estas condicionales será determinar distintas características. En Realizar_Pedido, el trabajo de las condicionales es determinar si el usuario elige un complemento para su pedido y si desea agregar propina. El precio total del pedido dependerá de estas decisiones, por lo que si se cumple alguna de estas condiciones, el precio total del pedido se modificará mediante el uso de otras fucniones. Por otro lado, en Confirmacion_Pedido y Confirmacion_Pedido_Propina, las condicionales se encargarán de evaluar si en el pedido sí se agregó complemento y/o propina, para así imprimir el complemento (en caso de agregar uno) y si la cuenta va abierta o cerrada. Finalmente, en Finalizar_Pedido, se utilizan las condicionales para la encuesta de servicio, donde el ususario calificará del 1 al 5 el servicio del programa. La condicional evaluará la calificación del ususario para imprimir un mensaje de despedida, agradecimiento o una disculpa en caso de un mal servicio.

## Estructuras de repetición (Avance 5)
En mi código de python incorporé estructuras 'while' en algunas de las funciones que se utilizan en el programa. El primer ciclo while lo utilizo para que el usuario pueda seguir interactuando con el Menú las veces que deseé hasta que se finalice el pedido. En el siguiente ciclo, dentro de la función Realizar_Pedido, se inicia un ciclo while infinito y se utiliza para permitir que el usuario tome múltiples elementos del pedido sin tener que volver al menú principal después de cada elemento. El programa pregunta al usuario si desea agregar tacos a su pedido. Si el usuario responde "si", se toman los detalles del pedido de tacos, se calcula el costo y se suma al total. Si responde "no", se establecen las variables relacionadas con tacos en None y 0. Luego, el programa hace una pregunta similar para las bebidas y los complementos. Toma los detalles del pedido, calcula los costos y los suma al total_pedido. Finalmente, se pregunta al usuario si desea agregar más elementos al pedido. Si responde "si", el bucle continúa y se repite el proceso para agregar otro elemento. Si responde "no", se rompe el bucle while y el programa vuelve al menú.

## Avance 6 (comenzado)
Adicionalmente, comencé con la incorporación de diccionarios dentro del código para almacenar el precio de cada uno de los productos de la taquería. Hice uso de la función get() en la función de Realizar_Pedido para acceder a los valores de los diccionarios. Y también, utilice cadenas f para la impresión de la confirmación del pedido. 

**NOTA**: En algunos casos específicos al realizar el pedido, el programa no responde correctamente. Esto debido a que no terminé correctamente con la incorporación de estos diccionarios. Lo seguiré trabajando para el siguiente avance (Avance 6), mejorando los diccionarios, impresiones, agregando listas y/o más ciclos si es necesario. 

El siguiente código contiene la parte del programa con las funciones declaradas y sus estructuras de decisión: [proyecto.py](proyecto.py)
