# CROWhite Display 0.4.0
- **Actualizaciones cifradas:** el archivo publicado va cifrado. La pantalla lo descifra mientras lo descarga y sigue comprobando la firma y la vuelta atrás (`actualizaciones.md`).
- **Menos información interna en el binario:** sin nombres de archivo y función en asserts y comprobaciones. Si hay un fallo, se localiza con el backtrace y el `.elf` de esa versión.
- **Esta versión se instala por USB:** las anteriores no pueden descifrar el archivo.
