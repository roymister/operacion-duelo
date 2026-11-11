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

## Publicarlo con GitHub Pages
1. Crea un repositorio nuevo en GitHub (por ejemplo `operacion-duelo`), público.
2. Sube **todo el contenido de esta carpeta** (`index.html`, la carpeta `lib/`, `README.md` y `.nojekyll`).
   - Desde la web: *Add file → Upload files* y arrastra los archivos y la carpeta.
   - O por consola:
     ```bash
     git init
     git add .
     git commit -m "Operación Duelo 1v1"
     git branch -M main
     git remote add origin https://github.com/TU_USUARIO/operacion-duelo.git
     git push -u origin main
     ```
3. En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.
4. Espera 1–2 minutos. El juego queda en: `https://TU_USUARIO.github.io/operacion-duelo/`

Comparte ese enlace con tus amigos.

## Probarlo en tu PC
Abrir `index.html` con doble clic **no funciona** (el navegador bloquea los módulos en `file://`). Levanta un servidor local en la carpeta:
```bash
python -m http.server 8000
```
y entra a `http://localhost:8000`.

## Estructura
```
index.html              Juego completo (mapa, IA del bot, HUD, sonidos)
lib/three.module.js     Three.js r160 (motor 3D)
lib/LICENSE-three.txt   Licencia MIT de Three.js
.nojekyll               Para que GitHub Pages sirva los archivos tal cual
```
