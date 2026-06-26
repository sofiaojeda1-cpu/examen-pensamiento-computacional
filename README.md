# Examen Pensamiento Computacional
 
**Alumna** Sofía Ojeda  

---

## 1. Descripción del proyecto
Este proyecto es una aplicación interactiva que convierte tu cámara web en un espejo artístico. Creé un sistema que reacciona cuando presionas diferentes teclas y cambia la forma en que te ves en la pantalla, todo acompañado de un sonido cada vez que cambias de efecto.

---

## 2. Marco Conceptual y Referente Artístico
Me inspiré en el **Arte Cinético** y en los espejos digitales de artistas modernos como *Daniel Rozin*. La idea es que la persona que mira la pantalla no sea espectador, sino que se convierta en parte de la obra. Al moverte frente a la cámara o presionar las teclas, alteras los colores, el tamaño y la forma de lo que estás viendo. Pasamos de un efecto donde la imagen se rompe en cuadritos de grises a otro donde los píxeles cobran vida y se inflan como si tuvieran relieve cuando les pasas el mouse por encima.

---

## 3. Cómo se usa.
Para probar el proyecto, se presionar las teclas **1, 2 o 3** en tu teclado:
* `Tecla 1 (Estado 0)`: La cámara con un filtro morado.
* `Tecla 2 (Estado 1)`: La imagen se transforma en un pixelado en blanco y negro.
* `Tecla 3 (Estado 2)`: La imagen se transforma en un pixelado de color azul que se agrandan cuando pasas el puntero del mouse por encima de ellos.

---

## 4. Cómo funciona por dentro.

* **Variables Propias:** Usé variables para guardar el `video` de la cámara, el `estado` de la pantalla (0, 1 o 2), el archivo de `sonido` para el clic y una `imagenAnterior`.
* **Condicionales:** El código usa `if` como interruptores. En `keyPressed()` para cambiar el estado y activar el sonido, y en `draw()` para el efecto visual de color en la pantalla.
* **Funciones Propias:** Creé funciones hechas por mí para ordenar el código por bloques según cada estado: `dibujarEstadoNormal()`, `dibujarEstadoPixelado()` y `dibujarEstadoInteractivo()`.
* **Bucles:** Usé `for` en el estado 1 y 2. Para poder capturar los colores de la cámara y dibujar los pixeles.
* **Medir distancias:** En el Estado 2, uso la función `dist()` para saber qué tan cerca está el mouse de cada pixel.
* **El map():** Uso `map()` para cambiar su tamaño de forma proporcional, entre más cerca está el mouse, más grande se infla el cuadro.
* **El random():** Uso `random()` en el Estado 2 para añadir una vibración en el relieve de los píxeles cuando se agrandan con el mouse.
* **Multimedia:** Al presionar 1,2 o 3 suena el archivo multimedia que agregue.

---

## 5. Registro del Proceso

### Paso 1 - Tecla 1: El inicio morado
* **Qué hace:** Es la pantalla de bienvenida con un filtro de color morado transparente (`tint`) dentro de mi función propia.
* **Captura del estado:** ### Paso 2 - Tecla 2: El pixelado blanco y negro
* **Qué hace:** Convierte la imagen en una pantalla de bloques grises 
* **Captura del estado:** ### Paso 3 - Tecla 3: El pixelado interactivo que se infla
* **Qué hace:** Los píxeles reaccionan al mouse usando `dist()`, tiene un tinte azul, vibran con `random()` y se agrandan de forma con `rectMode(CENTER)`.

---

## 6. Documentación del proceso y referentes
<img width="361" height="554" alt="images (2)" src="https://github.com/user-attachments/assets/69e22c7e-bbff-418e-8736-e0c5aad95d90" />
<img width="547" height="365" alt="images (1)" src="https://github.com/user-attachments/assets/131c7f7a-5ef4-41b5-8f6d-afe8de72886a" />
<img width="694" height="440" alt="images" src="https://github.com/user-attachments/assets/79ba0562-b7ca-44a9-a42e-46948022b7cf" />
<img width="903" height="667" alt="Captura de pantalla 2026-06-25 220107" src="https://github.com/user-attachments/assets/d5a0c635-99c7-4a0d-9d58-add9793c5425" />
<img width="876" height="660" alt="Captura de pantalla 2026-06-26 010914" src="https://github.com/user-attachments/assets/9f503578-5ab7-4272-bf37-dbaa167032df" />
<img width="865" height="677" alt="Captura de pantalla 2026-06-26 010933" src="https://github.com/user-attachments/assets/2e180c81-6065-4d66-9c07-db16a4775365" />
<img width="916" height="678" alt="Captura de pantalla 2026-06-26 010953" src="https://github.com/user-attachments/assets/04531a55-5208-492f-888e-c110811e88f1" />




---

## 7. Lo que aprendí y dificultades
* **Problemas:** Al principio, cuando los pixeles del Estado 2 se agrandaban al pasar el mouse, se estiraban solo hacia la derecha y hacia abajo, haciendo que el efecto se viera raro y desalineado.
* **Cómo lo arreglé:** Me di cuenta que se dibujan los rectángulos desde la esquina superior izquierda de forma predeterminada. Lo solucioné usando `rectMode(CENTER)` antes de dibujar el cuadro, lo que obliga a los píxeles a crecer parejos hacia todos los lados desde su propio centro.
---

## 8. Diagrama de flujo
<img width="1024" height="1536" alt="Diagrama de flujo" src="https://github.com/user-attachments/assets/c7366b5e-d70a-446b-94b7-ccfa21fc2b35" />
