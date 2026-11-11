# 🎯 Operación Duelo 1v1

![JavaScript](https://img.shields.io/badge/JavaScript-ES2022-F7DF1E?logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-r160-000000?logo=threedotjs&logoColor=white)
![WebGL](https://img.shields.io/badge/WebGL-3D-990000?logo=webgl&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![Plataforma](https://img.shields.io/badge/PC%20%7C%20Móvil-compatible-2ea44f)

Shooter 3D en primera persona estilo *Call of Duty* que corre directamente en el navegador. Te enfrentas 1 vs 1 contra un bot con inteligencia artificial en **Distrito en ruinas**, un mapa urbano con dos bases enemigas.

### 🎮 [**JUGAR AHORA →**](https://roymister.github.io/operacion-duelo/)

> No requiere instalación. Funciona en PC (teclado y mouse) y en celular (controles táctiles).

---

## 📸 Vista previa


<img width="1812" height="824" alt="image" src="https://github.com/user-attachments/assets/68dade4d-1711-45e0-ade6-fb57a5797bf5" />


---

## ✨ Características

- **Motor 3D en tiempo real** con Three.js (WebGL): iluminación, sombras dinámicas, niebla atmosférica y tone mapping.
- **Mapa urbano en ruinas** con edificios de varios pisos, daños por explosiones, vehículos abandonados, cables eléctricos y horizonte urbano.
- **Dos bases** (Alfa y Bravo): punto de reaparición de cada equipo, con reabastecimiento de munición y regeneración de salud.
- **Bot con IA**:
  - Búsqueda de rutas con **BFS** sobre una grilla de navegación.
  - Detección del jugador por **línea de visión** y campo de visión.
  - Tiempo de reacción, ráfagas de disparo y movimiento lateral en combate.
  - 3 niveles de dificultad: Recluta, Regular y Veterano.
- **Sistema de coberturas**: obstáculos de distintas alturas y opción de agacharse para cubrirse.
- **Balística hitscan** con detección de impactos por *ray casting* contra cajas de colisión (AABB) y daño extra por tiro a la cabeza.
- **Mecánicas tipo CoD**: apuntar con mira (ADS), retroceso, dispersión, recarga, sprint, regeneración de salud, indicador de daño, hitmarkers, killfeed y minimapa con radar.
- **Texturas procedurales**: todas las texturas se generan por código con ruido (*value noise* / *fBm*), sin archivos de imagen externos.
- **Audio sintetizado** con Web Audio API.
- **Soporte móvil**: joystick virtual, botones táctiles, asistencia de apuntado y modo de rendimiento automático.

---

## 🕹️ Controles

| Acción | PC | Celular |
|---|---|---|
| Moverse | `W` `A` `S` `D` | Joystick izquierdo |
| Apuntar | Mouse | Arrastrar en la mitad derecha |
| Disparar | Clic izquierdo | Botón **FUEGO** |
| Apuntar con mira | Clic derecho / `F` | Botón **MIRA** |
| Agacharse | `C` | Botón **AGACH.** |
| Correr | `Shift` | Joystick al tope |
| Recargar | `R` | Botón **RECARGA** |
| Pausa | `P` / `Esc` | Botón **II** |

---

## 🛠️ Tecnologías

| Tecnología | Uso |
|---|---|
| **JavaScript (ES Modules)** | Lógica del juego, IA, físicas y colisiones |
| **Three.js** | Renderizado 3D con WebGL |
| **Canvas 2D API** | Generación de texturas procedurales y minimapa |
| **Web Audio API** | Efectos de sonido sintetizados |
| **HTML5 + CSS3** | Interfaz (HUD, menús, controles táctiles) |
| **GitHub Pages** | Despliegue |

---

## 🧠 Aspectos técnicos destacados

- **Colisiones y física**: colisión círculo-AABB para jugador y bot, con deslizamiento suave contra paredes.
- **Ray casting propio** (*slab method*) para disparos, línea de visión del bot e impactos en superficies.
- **Navegación del bot**: grilla de 0.5 m generada a partir de los obstáculos, ruta con BFS y suavizado de trayectoria.
- **Arma en primera persona** renderizada en una segunda pasada para que no atraviese paredes.
- **Detección de dispositivo** para adaptar controles, interfaz y calidad gráfica.

---

## 🚀 Ejecutar en local

```bash
git clone https://github.com/roymister/operacion-duelo.git
cd operacion-duelo
python -m http.server 8000
```

Abre `http://localhost:8000` en el navegador.

> Abrir `index.html` con doble clic no funciona porque el navegador bloquea los módulos ES en `file://`.

---

## 📁 Estructura

```
operacion-duelo/
├── index.html    # Juego completo: motor, mapa, IA, HUD y controles
├── README.md
└── .nojekyll
```

---

## 👤 Autor

**Roy Malpartida Sánchez**
Estudiante de Ingeniería de Sistemas · Universidad César Vallejo


