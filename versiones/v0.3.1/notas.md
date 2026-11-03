# CROWhite Display 0.3.1
- **Imprimir desde la pantalla abre Trabajo en curso:** al confirmar Imprimir (en el detalle del archivo o en Imprimir otra vez), la pantalla espera a que la Duet esté imprimiendo y entonces cambia sola, desde la pantalla en que esté. Si en 60 s no empieza, no salta más tarde. Antes solo saltaba desde Inicio.
- **Estimación de la copia según la vía:** antes de copiar se indica si irá por WiFi o por cable, con su tiempo: unos 100 KB/s por WiFi y unos 2,4 KB/s por cable. Antes siempre suponía el cable: 10 min para un archivo de 1,4 MB que por WiFi tardó 10 s.
- **Reconexión por WiFi tras perder el enlace:** el propietario vio que, tras un corte durante una impresión, la pantalla no volvía a conectar con ninguna impresora hasta reiniciarla, aunque el PC sí llegaba a ellas. Causa probable, sin confirmar por falta de log: la consulta mDNS de `<nombre>.local` esperaba sin límite y bloqueaba todas las peticiones (`wifi-pantalla.md`). Cambios:
  - la consulta mDNS espera como mucho 3 s;
  - se recuerda la IP de cada impresora, y se usa si mDNS no contesta;
  - la WiFi de la pantalla reintenta también si se pierde un intento sin aviso o si se pierde la IP;
  - el log anota los fallos de consulta y de mDNS.
