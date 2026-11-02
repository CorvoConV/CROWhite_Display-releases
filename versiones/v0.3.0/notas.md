# CROWhite Display 0.3.0
- **Transferir G-code del pendrive o la microSD a `/gcodes` por WiFi:** si la pantalla tiene WiFi, el archivo se sube con `rr_upload` a cientos de KB/s en lugar de a ~5 KB/s por cable. Se comprueba con el CRC-32 y el tamaño, y solo se le da el nombre final si todo cuadra (`usb-pendrive.md`).
- Con cable y sin WiFi se sigue copiando por la UART. Si la Duet no responde por WiFi antes de escribir nada, la copia sigue sola por cable.
- Sin cable (conexión por WiFi), la transferencia ya está disponible.
