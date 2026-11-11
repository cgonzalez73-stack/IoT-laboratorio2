# Enlaces del Laboratorio 2 — Estación IoT

Este archivo reúne los enlaces a los recursos desplegados para este laboratorio. Las instrucciones originales de la actividad están en [README.md](README.md).

| Recurso | Enlace | Qué contiene |
|---|---|---|
| Simulación en Wokwi | https://wokwi.com/projects/480407033583407105 | Proyecto ESP32 con el circuito (DHT22 y OLED SSD1306), el firmware `sketch.ino` completo y las bibliotecas instaladas. Al iniciar la simulación se envían 24 mediciones a la API |
| API Flask en Render | https://iot-laboratorio2.onrender.com | Servicio web desplegado desde este repositorio con `app.py` |
| Comprobación de la API | https://iot-laboratorio2.onrender.com/salud | Debe responder `{"estado":"ok"}` |
| Consulta de mediciones | https://iot-laboratorio2.onrender.com/mediciones | Lista en JSON de las mediciones recibidas (GET) |
| Descarga de mediciones | https://iot-laboratorio2.onrender.com/descargar | Descarga el archivo `mediciones.json` |

## Notas

- El servicio de Render usa el plan gratuito, por lo que se suspende tras un periodo sin uso. La primera visita puede tardar unos 50 segundos en responder.
- Las mediciones se guardan en la memoria del servidor y no en una base de datos. Si el servicio se reinicia o se suspende, la lista queda vacía. Para volver a llenarla basta con ejecutar otra vez la simulación en Wokwi.
- En la prueba realizada, el ESP32 envió un lote de 24 registros y la API respondió con el código HTTP 201.
