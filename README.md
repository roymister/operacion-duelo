# Operación Duelo 1v1

Shooter en primera persona estilo CoD, hecho con HTML + JavaScript + [Three.js](https://threejs.org).
Tú (Base Alfa) contra un bot (Base Bravo) en el mapa **Distrito en ruinas**. Gana el primero en llegar a 10 bajas.

## Jugar
Abre el enlace de GitHub Pages del repositorio (ver abajo). Funciona en **PC** (teclado y mouse) y en **celular** (controles táctiles, en horizontal).

| Tecla | Acción |
|---|---|
| W A S D | Moverse |
| Mouse | Apuntar |
| Clic izquierdo | Disparar |
| Clic derecho / F | Apuntar con mira |
| C | Agacharse |
| Shift | Correr |
| R | Recargar |
| P / Esc | Pausa |

**En celular:** joystick a la izquierda para moverte (empújalo al tope para correr), arrastra en la mitad derecha para apuntar, y usa los botones FUEGO, MIRA, AGACH. y RECARGA. Al tocar *Desplegar* el juego pasa a pantalla completa. Incluye una ligera ayuda para apuntar y un modo de rendimiento automático.

## Estructura
```
index.html              Juego completo (mapa, IA del bot, HUD, sonidos)
lib/three.module.js     Three.js r160 (motor 3D)
lib/LICENSE-three.txt   Licencia MIT de Three.js
.nojekyll               Para que GitHub Pages sirva los archivos tal cual
```
