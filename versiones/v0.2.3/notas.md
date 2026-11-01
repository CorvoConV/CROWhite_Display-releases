# CROWhite Display 0.2.3
- **Actualización:** la pantalla vuelve a reiniciarse sola a los 3 s de instalar una versión. Fallaba porque, justo al pulsar Instalar, la aplicación tomaba el estado anterior por una cancelación. El arreglo se nota al actualizar **desde** esta versión.
- **Pantallas según la impresora:** en segundo plano solo se crean las pantallas exclusivas de la impresora identificada. Las de la otra impresora se crean solo si se abren. Ahorra PSRAM y tiempo de arranque.
