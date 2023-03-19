Aplicación de Android Studio: Dado Normal
Esta es una aplicación simple de Android Studio que sigue un tutorial ya dado que simula el lanzamiento de un dado normal (de 6 caras). La aplicación utiliza el generador de números aleatorios de Java para generar un número aleatorio entre 1 y 6 y lo muestra en la pantalla.

Ejercicios del tutorial :
Ejercicio1:

Añadimos un botón

Ejercicio 2 : Cambiamos el id del botón , se le asigna a una variable a través de findViewById y añadimos una Toast

Ejercicio 3 : Creamos una función que genere un número aleatorio y aparezca en el TextView

Ejercicio 4 : Se añaden imágenes del dado al drawable y se modifica la función diceRoll para llamar a las imagenes

Ejercicio 5 : Se extrae la variable ImageView con un lateInit

Ejercicio 6 : Usar  un vector drawbable compact

                                            STRINGS XML
                                            
A continuacion para la creacion de diferentes Strings Xml segun sus idiomas, **como nos manda el ejercicio**
lo que haremos es es crear un paquete Strings y dentro crearemos varios Strings XML como nos indica cuando hacemos click derecho sobre el paquete
![image](https://user-images.githubusercontent.com/91197896/226192697-658c8994-7061-4033-8e42-d174cd15e298.png)

Despues de eso lo que haremos sera crear dentro del paquete el Strings indicados, y dentro creamos las nuevas referencias de los botones a los cuales llamaremos por ids
![image](https://user-images.githubusercontent.com/91197896/226193537-8475c9fc-cee6-4864-9446-3343cab86a40.png)

                                              IMAGENES EN DRAWABLE
                                              
 Ahora vendrian las imagenes que he selecionado y añadido a la aplicacion para hacerla, cada imagen añadida seria una por una cara del dado mas una con el dado vacio, de tal manera que cuando la aplicacion se iniciara y **le demos al boton**. Iran saliendo todas las caras.

**Imagenes en el drawable:**

![image](https://user-images.githubusercontent.com/91197896/226194726-94eb4051-8764-4084-ad94-390250c5895c.png)

**Codigo en la main**

```
private fun rollDice() {
        val randomInt = Random().nextInt(6) + 1
        val drawableResource = when (randomInt) {
            1 -> R.drawable.dice_1
            2 -> R.drawable.dice_2
            3 -> R.drawable.dice_3
            4 -> R.drawable.dice_4
            5 -> R.drawable.dice_5
            else -> R.drawable.dice_6
        }

        val diceImage: ImageView = findViewById(R.id.dice_image)
        diceImage.setImageResource(drawableResource)
    }   
 ```


                                  FUNCION DIFERENTE A LA RANDOM
 
 Aplicamos una funcion diferente pasa sacar la cara de el dado
```
  val randomInt = (1..6).random()
```


