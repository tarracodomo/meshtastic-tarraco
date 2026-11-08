# Privacidad y seguridad

@iceman — Tarraco Domo

## Antes de publicar
- No subir claves PSK, claves privadas de identidad, PIN Bluetooth, contraseñas Wi-Fi o MQTT, copias completas de configuración ni volcados de registros sin revisar.
- No publicar URLs ni QR de canales privados: pueden incluir la PSK. Un enlace codificado no significa que el secreto esté protegido.
- Revisar coordenadas GPS, nombres de nodos, identificadores, rutas y metadatos de fotografías. No publicar ubicaciones de terceros sin autorización.
- La configuración inicial puede compartir posición o telemetría. Revisar opciones del firmware y de la app; desactivar o reducir la precisión cuando corresponda.
- El canal predeterminado usa una clave conocida públicamente: no es un canal confidencial. Una clave propia debe compartirse solo con participantes autorizados. El cifrado de contenido no elimina toda exposición de metadatos.
- Evitar MQTT al iniciar las pruebas; estudiar por separado qué datos se envían a Internet y los permisos del broker.

## Si publicas una clave por error
Eliminarla de la rama actual no la borra del historial. Sustituir la clave del canal en todos los nodos afectados y compartir la nueva por un medio privado. Si se expone una clave de identidad o credencial de servicio, seguir el procedimiento de revocación o sustitución del componente correspondiente. No pegar secretos en issues para pedir ayuda.

## Seguridad física y radio
Usar antena, alimentación y batería adecuadas al dispositivo. Seguir límites regionales y normas locales. No forzar límites de tiempo de transmisión ni potencia para buscar más alcance. No usar este proyecto como sistema certificado ni como único canal de emergencia.

## Fuentes
https://meshtastic.org/docs/configuration/tips/
https://meshtastic.org/docs/software/python/cli/usage/
https://meshtastic.org/docs/configuration/radio/lora/
