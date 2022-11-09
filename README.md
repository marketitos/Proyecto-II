# Pagina-Proyecto

## Para poder realizar las animaciones del texto y de las imagenes utilizamos el java script de AOS

### Para poder usarlo ponemos en el body:

 `<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>`

`<script>
  AOS.init();
</script>`

### y En el Head para el css:

#### `< link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet" >`

### Lista de Requisitos: 

![requisitos](https://user-images.githubusercontent.com/108817479/200419859-c31e6fc5-8af0-4828-976a-3a989d5fcb11.PNG)

## ARDUINO

#### Componentes
Para realizar el proyecto utilizamos una ARDUINO UNO con una protoboard de 170 puntos para la conexion de los transistores, esta proto nos sirvio para poder administrar el espacio. Luego el soporte decidimos emplear una caja donde estarian todas las conexiones la cual esta integrada a unos anteojos que tienen un ultrasonido en la parte frontal para poder detectar los obstaculos. Por otro lado tenemos unos sensores infrarrojos a los costados para poder encontrar aquellos obstaculos laterales. Por ultimo para poder lograr darle una alimentacion al proyecto decidimos utilizar una Bateria de 9V.

#### Ideas Futuras
Una de las ideas principales que tuvimos fue poder crear unas tobilleras las cuales tendrian unos sensores que detectarian la parte inferior del cuerpo para que la persona no tuviera ningun problema, otra idea fue integrarle unos auriculares a los anteojos para poder avisarle por voz a la persona si se encuentra un obstaculo cerca de las tobilleras

### Codigo

En este código utilizamos como parámetro principal el map, en este caso lo usamos para definir los rangos de los sensores, esto reemplazaría los if() que teníamos en el anterior código .En el pin 10 y 11 están los sensores infrarrojos. 
El ultrasonido está conectado mediante un Trigger que se encuentra conectado en el pin 9, un Echo que esta conectado al pin 8 y un Buzzer que está en el pin 7, este buzzer cumple la función de emitir un pitido el cual surge después de un determinado delay que se lo colocamos nosotros en el map.
El funcionamiento del Buzzer es el de avisar a la persona que tiene algo o alguien al frente o a los costados, que acá entran los infrarrojos que avisan a los laterales, estos están conectados con un digitalread que le permiten leer el estado y si detecta algo suena el buzzer pero con otro pitido distinto para poder distinguir si es adelante o a los costados.
