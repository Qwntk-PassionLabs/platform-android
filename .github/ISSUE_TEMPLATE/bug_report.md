name: Reportar un bug
description: Describe un error que encontraste en el proyecto
title: "[BUG] "
labels: [bug]

body:
  - type: markdown
    attributes:
      value: |
        Gracias por ayudarnos a mejorar este proyecto. Por favor llena la siguiente información.

  - type: input
    id: environment
    attributes:
      label: Entorno
      description: ¿En qué dispositivo, versión de Android o emulador ocurrió?
      placeholder: Ej. Android 13, Pixel 6

  - type: textarea
    id: steps
    attributes:
      label: Pasos para reproducir
      description: Describe paso a paso cómo reproducir el bug
      placeholder: 1. Abre la app\n2. Toca el botón X\n3. Se cierra inesperadamente

  - type: textarea
    id: expected
    attributes:
      label: Comportamiento esperado
      description: ¿Qué debería pasar en lugar del error?
      placeholder: La app debería mostrar un mensaje de confirmación

  - type: textarea
    id: logs
    attributes:
      label: Logs o capturas
      description: Si tienes logs o imágenes, agrégalas aquí
