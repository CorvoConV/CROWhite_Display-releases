# CROWhite Display: versiones publicadas

Firmware de la pantalla táctil CROWhite Display (Waveshare ESP32-P4-WIFI6-Touch-LCD-7B) para las
impresoras CROWhite I2XY e Indu. El código está en un repositorio privado. Aquí solo se publican
los binarios **firmados y cifrados** que la pantalla instala por WiFi.

- `versiones/vX.Y.Z/`: `CROWhite_Display.bin`, `manifiesto.txt` y `notas.md` de cada versión.
- Cada etiqueta `vX.Y.Z` crea su release (`.github/workflows/release.yml`). La pantalla lee
  `releases/latest/download/manifiesto.txt`.
- Un `.bin` sin la firma del propietario se rechaza en la pantalla aunque esté publicado aquí.

No edites estos archivos a mano: los genera `tools/publicar_version.py` del repositorio del firmware.
