# NPC

Para la alegría de todas y todos vamos a continuar trabajando con los NPCs (Non-Player Character) o PNJ (personaje no jugador) en castellano. En esta ocasión debemos extender las capacidades de Trebor, nuestro guardia de Skyrim, e incorporar un nuevo personaje. 

#### Vengan de a muches

El guardia debe tener la capacidad de interactuar con varios personajes jugadores (PJ) y mantener un hilo de conversación para cada uno de ellos. Es decir, por ejemplo si tenemos los PJ Hamilton y Tirion, si interactúa por primera vez con Hamilton le responde `'Hola forastero'` y si luego interactúa por primera vez con Tirion le debe responder también  `'Hola forastero'`.

#### Opinión del pueblo

Además, el guardia debe tener la capacidad de tener diálogos diferentes según la opinión que tiene el pueblo, Riverwood, sobre el personaje con el que está interactuando. El pueblo puede ver a un personaje jugador como prometedor o desconocido. 

Cuando Trebor habla con un personaje calificado como prometedor por Riverwood su hilo de diálogo es: (1) 'Bienvenido aventurero!', (2) 'Espero que tengas una buena estadía en Riverwood'.

Cuando habla con un personaje desconocido por Riverwood su hilo de diálogo es (1) 'Hola forastero', (2) '¿Todo bien?' y  (3)'¿Algún problema?'

#### Influencer

También se pide agregar un nuevo personaje no jugador Carolina la curandera de Riverwood. Debe funcionar de la misma forma que el guardia pero su repertorio es:

- Personajes prometedores según Riverwood: (1) 'Salud aventurero!', (2) 'Toma esta pócima que te hará crecer el pelo. Y cuando tengas una aflicción, ven a verme' 

- Personajes desconocidos por Riverwood: (1) '¿Estás enfermo Forastero?',  (2) 'Ah, solo quieres conversar' y (3) 'Cuando tengas una aflicción, ven a verme’

Además, Carolina es muy influyente en la opinión de Riverwood, cuando un personaje completa el diálogo con la curandera, es decir llega a la última frase de su repertorio, esto hace que pase a ser calificado como prometedor según Riverwood, y que tanto el guardia como Carolina reinicien sus hilos de conversaciones con dicho personaje.

#### Punto de partida

Deben importar el código inicial `Ejercicio1-PNJ-Episodio2.CodigoInicial.st` y construir su solución a partir de ahí. En dicho paquete encontrarán al objeto `TreborElGuardiaDeSkyrim`, con el mismo funcionamiento visto en clase y a dos objetos que agrupan las pruebas de funcionamiento del guaria y la curandera `PruebasInteracionesConTreborElGuardia` y `PruebasInteracionesConCarolinaLaCurandera`. El objetivo de estas pruebas es ayudarlos/as a implementar lo pedido. En ellas encontrarán que tienen que implementar algunos métodos para poder completar las pruebas.

##### Sugerencias: 

Vayan haciendo pasar las pruebas `PruebasInteracionesConTreborElGuardia` según el orden de cada prueba (de 1 a la 9). Y luego hagan pasar las pruebas `PruebasInteracionesConCarolinaLaCurandera` y también aquí siguiendo el orden sugerido (de 1 a la 11)

## Tips

**¿Cómo crear una colección ordenada?**

```smalltalk
unaColeccion := OrderedCollection new.
```

**¿Cómo agregarle un objeto a una colección?**

```smalltalk
unaColeccion add: 'Hola'
```

**¿Cómo preguntarle a una colección si incluye o no un objeto?**

```smalltalk
unaColeccion includes: 'Hola'
```

**¿Cómo crear un diccionario?**

```smalltalk
unDiccionario := Dictionary new.
```

**¿Cómo asociarle una clave y un valor a un diccionario?**

```smalltalk
unDiccionario := Dictionary new.
unDiccionario at: 'unaClave' put: 'unValor'
```

**¿Cómo acceder al valor de una clave o a un valor por defecto si el diccionario no contiene dicha clave?**

```smalltalk
unDiccionario := Dictionary new.
unDiccionario at: 'unaClave' ifAbsent: [ 'unValorPorDefecto' ]
```


**¿Cómo evaluar unas colaboraciones u otras según un objeto booleano?**

```smalltalk
unBooleano ifTrue: [ "envios de mensajes para cuando unBooleano es true" ] ifFalse: [ "envios de mensajes para cuando unBooleano es false"  ]
```


