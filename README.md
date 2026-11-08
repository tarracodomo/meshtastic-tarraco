# Meshtastic Tarraco

@iceman — Tarraco Domo
https://tarracodomo.com

Guía independiente en español para preparar y probar nodos Meshtastic. No es un proyecto oficial ni una red de cobertura garantizada. Meshtastic y el firmware pertenecen a sus respectivos autores.

## Estado
Documentación inicial preparada con asistencia de IA, basada en documentación oficial. No se han realizado ni verificado pruebas de radio para este repositorio. No contiene firmware propio, claves, configuraciones privadas ni posiciones de nodos.

## Qué necesitas
- Dos dispositivos compatibles con Meshtastic para una prueba propia, con variante de radio adecuada para la banda y el país.
- Antena compatible con banda y conector del dispositivo; no transmitir sin la antena correcta conectada.
- Cable USB de datos, alimentación adecuada y un móvil con la aplicación oficial o un navegador compatible con el método de conexión elegido.

## Puesta en marcha
1. Identificar modelo exacto y variante de radio antes de descargar firmware. No asumir que una placa de 915 MHz sirve para una configuración europea de 868 MHz.
2. Leer https://meshtastic.org/docs/getting-started/ y las instrucciones del fabricante.
3. Si el equipo ya funciona, respaldar privadamente su configuración antes de cambiarlo. No actualizar ni borrar por rutina.
4. Para una instalación nueva, usar https://flasher.meshtastic.org/ y seleccionar el modelo exacto y una versión estable recomendada por el proyecto. Guardar versión y fecha de instalación. El flasheo puede borrar ajustes.
5. Conectar la app al nodo y establecer la región que corresponda al país, a la banda del hardware y a la normativa vigente antes de transmitir. En España, para hardware europeo de 868 MHz, consultar la opción EU_868 y su documentación actual; no copiar configuraciones de otros países ni forzar potencia/frecuencia.
6. Para comunicar dos nodos, comprobar compatibilidad de región, preset y frecuencia/canal de radio. Para leer mensajes del canal compartido deben coincidir sus ajustes y clave. Cambiar el nombre del canal puede afectar la selección automática de frecuencia.
7. Empezar con rol CLIENT. No usar ROUTER o REPEATER solo para intentar ganar alcance sin estudiar la topología y las recomendaciones oficiales.
8. Revisar transmisión de posición, telemetría, MQTT y seguridad antes de salir a probar. Para la primera prueba no hace falta activar MQTT ni una pasarela a Internet.
9. Enviar unos pocos mensajes de prueba entre equipos propios, verificar recepción en ambos extremos y registrar el resultado. No saturar la red ni emitir en bucle.

## Uso y límites
LoRa permite intercambiar mensajes de baja tasa de datos; no sustituye una conexión a Internet, voz continua ni vídeo. Alcance y entrega dependen de relieve, edificios, antenas, interferencia y configuración. Un aviso de envío o ACK no demuestra que una persona haya leído el mensaje. No usar como único medio para emergencias.

## Pruebas reproducibles
Usar pruebas/registro.csv. Registrar solo alias de nodos propios y zonas generales, no domicilios ni coordenadas. Separar mensajes enviados, recibidos y confirmados; anotar distancia aproximada solo si se conoce. RSSI y SNR se registran únicamente si la herramienta los muestra: no estimarlos ni atribuirlos a toda la ruta multihop.

## Privacidad
Leer docs/PRIVACIDAD.md antes de publicar capturas o configuraciones. Una URL o QR de canal puede contener su clave. El canal predeterminado no debe tratarse como privado.

## Trabajo pendiente
- Identificar modelos concretos disponibles para pruebas.
- Comprobar instalación y configuración en dos nodos propios.
- Documentar una prueba local real con datos anonimizados.
- Añadir fotografías propias sin coordenadas ni códigos QR.
- Revisar resultados antes de recomendar configuraciones.

## Referencias oficiales
https://meshtastic.org/docs/getting-started/
https://meshtastic.org/docs/getting-started/initial-config/
https://meshtastic.org/docs/configuration/radio/lora/
https://meshtastic.org/docs/configuration/tips/
https://meshtastic.org/docs/software/python/cli/usage/

## Autoría y derechos
Preparado para @iceman — Tarraco Domo con asistencia de IA. Derechos reservados sobre contenido original; sin licencia de redistribución concedida por ahora. Las marcas, firmware y bibliotecas externos conservan sus derechos y licencias. No hay afiliación oficial con Meshtastic.
