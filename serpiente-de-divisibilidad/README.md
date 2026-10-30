# Serpiente de divisibilidad

Juego tipo *Snake* para que los alumnos de 1º y 2º de ESO repasen la divisibilidad.
En la parte de arriba aparece una instrucción (por ejemplo *«Número divisible entre 5»*)
y por el tablero se reparten bloques numerados: la serpiente debe comerse **solo** los
que la cumplen. Cada acierto cambia la instrucción y los números.

> Instrucción: Número divisible entre 5
> Aparecen 2 bloques: 15 y 18
> La serpiente se tendrá que comer el bloque con el nº 15, ya que el 18 no es divisible entre 5

## Cómo se juega

- **Mover**: flechas o `W` `A` `S` `D`. En tablet o móvil, desliza el dedo por el tablero.
- **Pausar**: botón *Pausa*, `Espacio` o `P`.
- **Acierto**: la serpiente crece, sumas puntos y sale una instrucción nueva.
- **Fallo**: pierdes una vida (tienes 3) y aparece la explicación del error
  (*«18 no es divisible entre 5»*). La instrucción se mantiene, así que puedes reintentarlo.
- **Bordes**: si sales por un lado del tablero, apareces por el opuesto.
- **Fin de partida**: al quedarte sin vidas o al morderte la cola.
  Al terminar se listan los últimos fallos con su explicación, para repasarlos.

La dificultad crece sola: cada 5 aciertos subes de nivel, y con el nivel aumentan la
velocidad, el rango de números (hasta 150), el número de bloques en pantalla (de 2 a 6)
y el tipo de instrucciones.

## Nivel inicial

En la pantalla de inicio se elige con qué nivel empezar (1 a 4), según lo que se haya
dado en clase; a partir de ahí sigue subiendo al jugar. La elección se recuerda en el
navegador, así que basta con configurarlo una vez por ordenador.

## Contenidos que repasa

| Nivel | Instrucciones que empiezan a salir |
|-------|------------------------------------|
| 1 | divisible entre *n*, múltiplo de *n*, que NO sea múltiplo de *n* (criterios del 2, 3, 5, 9, 10 y 11) |
| 2 | número primo, número compuesto, divisor de *n* |
| 3 | que NO sea divisible entre *n*, múltiplo común de *a* y *b*, divisor común de *a* y *b* |
| 4 | el mcm de *a* y *b*, el MCD de *a* y *b* |

Cada nivel **añade** instrucciones a las anteriores: empezando en el 4 pueden salir todas.

Los distractores se sortean por todo el rango del nivel, con más probabilidad cuanto
más *cerca* están de un número válido (para que haya que calcular de verdad en lugar de
acertar de un vistazo), pero sin cortar por distancia: así «el mayor», «el menor» o
«cualquier impar» no son pistas fiables. En «primo» salen impares compuestos (9, 15, 21…)
y en «compuesto», primos de todo el rango. El modo `?test=1` comprueba este reparto.

Las preferencias (idioma, nivel, mejor puntuación) se guardan en el navegador si se puede;
si el almacenamiento está bloqueado o tiene valores raros, el juego funciona igual.

## Idiomas

Las instrucciones salen en español o en inglés. En la pantalla inicial puedes elegir
**Mezcla ES/EN** (por defecto, cada instrucción sale al azar en un idioma), **Solo español**
o **Only English**. La elección se recuerda en el navegador.

## Cómo usarlo en clase

Los alumnos entran con el enlace https://salasgar.github.io/serpiente-de-divisibilidad/.

Es un único archivo sin dependencias: basta con abrir `index.html` con doble clic en
cualquier navegador. Funciona también desde un pendrive, sin internet ni instalación.

Este `index.html` es la única copia del juego: vive en el repositorio del sitio
(`salasgar.github.io/serpiente-de-divisibilidad/`) y cada commit que se empuja queda publicado.

## Comprobar que las matemáticas son correctas

Abre `index.html?test=1`. Se ejecuta una batería de pruebas que contrasta las funciones
del juego contra implementaciones independientes (primos mediante criba de Eratóstenes,
MCD y mcm por fuerza bruta) y genera cientos de rondas en todos los niveles verificando
que siempre haya al menos un bloque correcto, al menos un distractor, ningún número mal
etiquetado y ningún bloque superpuesto.

## Autoría

© 2026 Juan Luis Salas García. El aviso aparece en letra pequeña bajo el tablero, en la
etiqueta `<meta name="author">` y en un comentario al principio de `index.html`.
