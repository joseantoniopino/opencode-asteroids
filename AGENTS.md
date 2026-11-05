# Guía del repositorio

- Juego de navegador sin dependencias ni compilación: `index.html` define el canvas y los estilos, y carga `game.js` como script clásico. Este archivo gestiona la entrada, el estado, el renderizado y el bucle con `requestAnimationFrame`.
- Para ejecutarlo, abre `index.html` directamente o usa `npx serve .` y visita `http://localhost:3000`.
- Las dimensiones están duplicadas: mantén sincronizados el ancho y alto del canvas en `index.html` con `W` y `H` en `game.js`.
- Las posiciones se envuelven en los bordes, pero `dist()` usa distancia euclídea normal: las colisiones no se detectan a través de bordes opuestos.
- El README menciona potenciadores y un asteroide de estrella fugaz, pero el código actual no implementa ninguno de los dos.
- No hay pruebas, lint ni compilación configurados. Para comprobar la sintaxis, ejecuta `node --check game.js`; verifica los cambios de jugabilidad en el navegador (flechas, espacio, colisiones, vidas, niveles y reinicio tras perder, según corresponda).
