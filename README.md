# Asteroids

Clon del clásico arcade **Asteroids** implementado en canvas HTML5 puro, sin dependencias ni bundler.

## Descripción

Nave espacial en un campo de asteroides con envolvimiento de bordes (el espacio es toroidal). Destruye asteroides para sumar puntos: los grandes se parten en medianos, los medianos en pequeños. Algunos dejan un power-up de velocidad o de disparo triple.

## Tecnologías

- **HTML5 Canvas** — renderizado 2D
- **JavaScript (ES6+)** — lógica del juego en un solo archivo `game.js`
- Sin frameworks, sin bundler, sin dependencias

## Cómo correr

Abre `index.html` directamente en el navegador (doble clic), o usa un servidor local:

```bash
npx serve .
```

Luego visita `http://localhost:3000`.

## Controles

| Tecla     | Acción     |
| --------- | ---------- |
| `←` `→`   | Rotar nave |
| `↑`       | Propulsar  |
| `Espacio` | Disparar   |

## Puntuación

| Asteroide | Puntos |
| --------- | ------ |
| Grande    | 20     |
| Mediano   | 50     |
| Pequeño   | 100    |
| Estrella fugaz | 200 |

## Características

- 3 vidas con invencibilidad temporal al reaparecer (parpadeo)
- Asteroides se parten en fragmentos más pequeños al ser destruidos
- Partículas de explosión al destruir asteroides
- Velocidad: algunos asteroides dejan un power-up que duplica la velocidad de la nave durante 5 segundos. Recoger otro reinicia el tiempo.
- Disparo triple: durante 5 segundos, cada disparo lanza tres balas simultáneas en un abanico estrecho de −4°, 0° y +4°. Recoger otro reinicia el tiempo; puede combinarse con velocidad.
- Estrella fugaz: aparece ocasionalmente, es dorada y deja una estela. Se mueve más rápido, desaparece tras 6 segundos y no se fragmenta. Destruirla es opcional para avanzar de nivel.
