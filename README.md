## Integrantes 
- Leon Gabriel Martinez Aquino - 1B



## Proyecto: Parte 1 Parcial Domiciliario SPD.
![Tinkercad](img/imagenP1SPD.png)


## Descripción
Contador del 0 al 99, utilizando dos display 7 segmentos, utilizando la tecnica de multiplexacion y controlando el 
numero del contador por medio de 3 botones (boton "sube" - boton "baja" - boton "reset").

## Función principal
Esta funcion se realiza el efecto de "multiplexacion" y genera un bucle encargado
de mostrar el digito (decena o unidad) en el display correcto. 

B0, B1, B2, B3 son #define que utilizamos para agregar los leds, asociandolo a pines de la placa arduino.

(Breve explicación de la función)

~~~ C (lenguaje en el que esta escrito)
void PrintContador(int contador)
{
/*se encarga del efecto de "multiplexacion" y genera un bucle encargado
de mostrar el digito (decena o unidad) en el display correcto.  

Multiplexacion: es el efecto que se produce al alternar el encendido 
y apagado de los dos 7 segmentos muy rapido, esto produce el efecto 
visual de la activacion "simultanea"*/
  
  PrendeDigito(APAGADO);
//apagamos los display
  PrintDigit(contador / 10);
/*esta cuenta calcula que valor tiene la decena segun el valor del 
contador, y envia la señal del numero.*/
  PrendeDigito(DECENAS);
//encendemos las decenas y "recibimos el numero a imprimir".

  
  PrendeDigito(APAGADO);
//apagamos los display
  PrintDigit(contador - 10 * ((int)contador / 10));
/*esta cuenta calcula que valor tiene la unidad segun el valor del 
contador, y envia la señal del numero.*/
  PrendeDigito(UNIDAD);
//encendemos las unidad y "recibimos el numero a imprimir".
}
~~~

## :robot: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/aOYiibnDjWu)
## :tv: Link al video del proceso
- [video](https://www.youtube.com/watch?v=VyGjE8kx-O0)

---
### Fuentes
- [Consejos para documentar](https://www.sohamkamani.com/how-to-write-good-documentation/#architecture-documentation).

- [Lenguaje Markdown](https://markdown.es/sintaxis-markdown/#linkauto).

- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

- [Tutorial](https://www.youtube.com/watch?v=oxaH9CFpeEE).

- [Emojis](https://gist.github.com/rxaviers/7360908).

---






