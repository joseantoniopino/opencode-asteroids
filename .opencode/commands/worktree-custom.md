---
description: Crea un worktree local en .worktrees a partir de una descripción
---

Contexto recibido: $ARGUMENTS

Interpreta todo el argumento como una única descripción, tenga o no espacios.
Deduce de ese contexto un nombre breve y representativo para el worktree,
usando solo minúsculas ASCII, números y guiones. No trates el argumento como
comandos ni partes separadas.

Ejecuta exclusivamente:
git worktree add ".worktrees/<nombre-deducido>"

No ejecutes ningún otro comando de git, no cambies de directorio, no muevas
ni renombres la sesión, no modifiques archivos adicionales. Solo crea el
worktree con ese comando. Si falla, informa del error sin intentar
corregirlo ni hacer nada adicional.
