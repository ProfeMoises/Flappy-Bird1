# 🐦 Flappy Bird - Edición Canvas

![Flappy Bird](https://img.shields.io/badge/versión-1.0-brightgreen) ![Licencia](https://img.shields.io/badge/licencia-MIT-blue) ![Puntuación](https://img.shields.io/badge/dificultad-adictiva-red)

**Flappy Bird** es un clon del legendario juego móvil que conquistó al mundo en 2013, recreado completamente con **HTML5 Canvas, CSS3 y JavaScript Vanilla**. Controla un pequeño pájaro amarillo esquivando tuberías verdes mientras desafías la gravedad y tu propia paciencia. ¡Perfecto para jugar directamente en el navegador!

---

## 📖 Historia del Juego Original

En mayo de 2013, el desarrollador vietnamita **Dong Nguyen** publicó *Flappy Bird* para iOS. Con gráficos inspirados en los clásicos de 8 bits y una jugabilidad frustrantemente difícil, el juego pasó desapercibido durante meses. Pero en enero de 2014, de repente se volvió viral, alcanzando el primer lugar en descargas de la App Store y generando aproximadamente **50 000 dólares diarios** en publicidad.

Su éxito fue tan abrumador que Nguyen, abrumado por la presión mediática y las acusaciones de plagio, decidió retirarlo de las tiendas en febrero de 2014, tuiteando: *"No puedo soportarlo más"*. A pesar de su desaparición oficial, Flappy Bird dejó un legado imborrable, inspirando incontables clones, memes y hasta estudios sobre adicción a videojuegos.

**Nuestra versión** rinde homenaje a ese clásico, conservando la esencia de simplicidad y frustración que lo hizo famoso, pero con un toque visual moderno y sin depender de servidores externos.

---

## 🎮 Cómo Jugar

El objetivo es simple: **vuela entre las tuberías sin chocar**. Cada par de tuberías superado suma un punto a tu marcador.

1. **Abrir el archivo**: Descarga o clona el archivo HTML y ábrelo en tu navegador favorito (Chrome, Firefox, Edge, Safari, etc.).
2. **Iniciar la partida**: Presiona `ESPACIO` o haz clic en la pantalla para comenzar.
3. **Volar**: El pájaro cae debido a la gravedad. Cada toque o pulsación le da un impulso hacia arriba. Calcula bien la fuerza y el momento.
4. **Evitar obstáculos**: Las tuberías verdes aparecen a intervalos regulares con una separación fija. Debes pasar por el hueco sin tocar los bordes.
5. **Sobrevivir**: El juego termina si el pájaro golpea una tubería o el suelo. Entonces verás tu puntuación final y el récord guardado.

---

## 🕹️ Controles

| Acción | Teclado | Ratón / Touch |
|--------|---------|---------------|
| **Saltar / Volar** | `ESPACIO`, `↑` (flecha arriba), `W` | Clic izquierdo |
| **Reiniciar tras Game Over** | `ESPACIO` | Clic en la pantalla |

> 💡 **Consejo pro**: Realiza toques cortos y rítmicos; no mantengas presionada la tecla. Deja que el pájaro caiga un poco entre cada impulso para tener más control.

---

## 📊 Sistema de Puntuación

- **+1 punto** por cada par de tuberías superado exitosamente.
- La puntuación se muestra en la parte superior central durante la partida.
- Al obtener un punto, una animación flotante "+1" aparece cerca del pájaro.
- El **récord personal** (high score) se guarda automáticamente en el `localStorage` del navegador y se muestra en pantalla al perder.

---

## ✨ Características Principales

- 🎨 **Gráficos vectoriales pintados con Canvas**: Cielo con gradiente, nubes, suelo texturizado, tuberías con sombras y brillo realista, y un pájaro detallado con ojo, pico, ala y cola.
- 🔊 **Efectos visuales**: Vibración de pantalla al chocar, animación de puntuación emergente y texto pulsante para reiniciar.
- 📱 **Responsive y táctil**: Funciona en dispositivos móviles y tablets con eventos táctiles.
- 💾 **Persistencia de récord**: La mejor puntuación se mantiene incluso al cerrar el navegador.
- 🧠 **Física ajustable**: Gravedad, fuerza de salto y velocidad de tuberías modificables en el código.

---

## 🔧 Tecnologías Utilizadas

- **HTML5 Canvas**: Renderizado de todos los elementos del juego (fondo, personajes, obstáculos, HUD).
- **CSS3**: Estilos modernos con gradientes, animaciones `@keyframes`, sombras y diseño centrado.
- **JavaScript (ES6+)**: Lógica del juego, detección de colisiones, gestión de puntuaciones y eventos de teclado/ratón/touch.

---

## 🧱 Estructura Interna del Código

El script está organizado en bloques funcionales para facilitar su comprensión y personalización:

| Bloque | Descripción |
|--------|-------------|
| **Constantes** | Gravedad, fuerza de salto, ancho de tubería, separación, etc. |
| **Variables de estado** | Posición del pájaro, array de tuberías, puntuación, frames. |
| `resetGame()` | Reinicia todas las variables para una nueva partida. |
| `spawnPipe()` | Crea una nueva tubería con altura aleatoria. |
| `checkCollision()` | Detecta colisiones mediante algoritmo círculo-rectángulo. |
| `update()` | Ejecuta la lógica cada frame: física, generación de obstáculos, puntuación y fin de juego. |
| `render()` | Dibuja todos los elementos visuales en el canvas. |
| **Funciones de dibujo** | `drawSky()`, `drawGround()`, `drawPipes()`, `drawBird()`, `drawGameOverOverlay()`. |
| **Eventos** | Listeners para teclado, ratón y pantalla táctil. |
| **Bucle principal** | `gameLoop()` mediante `requestAnimationFrame`. |

---

## 🎯 Curiosidades y Datos Interesantes

- El pájaro original de Flappy Bird se llamaba **Faby**, y muchos fans crearon teorías sobre su trágico destino al chocar.
- Nguyen se inspiró en el juego de ping pong, buscando una mecánica simple pero adictiva.
- Este clon utiliza detección de colisiones **basada en distancias a rectángulos**, lo que permite un ajuste preciso incluso con formas redondeadas.
- El efecto de "shake" (vibración de pantalla) está implementado moviendo el contexto del canvas aleatoriamente durante unos frames tras la colisión.
- La puntuación máxima registrada oficialmente en el Flappy Bird original es de **999 puntos** (aunque muchos jugadores lo consideran casi imposible sin trucos).

---

## 🚀 Cómo Ejecutar Localmente

1. Copia el código HTML completo en un archivo con extensión `.html` (por ejemplo, `flappy_bird.html`).
2. Haz doble clic sobre el archivo para abrirlo en tu navegador web.
3. ¡A jugar!

No necesitas servidores, gestores de paquetes ni conexión a Internet. Es completamente autónomo.

---

## 📝 Personalización Rápida

Si quieres modificar la dificultad, busca estas líneas al inicio del script y ajusta los valores:

```javascript
const GRAVITY = 0.48;          // Aumenta para caer más rápido
const JUMP_FORCE = -7.8;      // Más negativo = salto más alto
const PIPE_SPEED = 2.2;       // Mayor valor = tuberías más rápidas
const PIPE_GAP = 140;         // Más grande = más fácil

📄 Licencia
Este proyecto es de código abierto bajo la licencia MIT. Siéntete libre de estudiarlo, modificarlo y compartirlo. ¡Solo recuerda mencionar al autor original si lo distribuyes!

"La simplicidad es la máxima sofisticación." – Leonardo da Vinci

¡Disfruta jugando y tratando de superar tu propio récord! 🐦✨
