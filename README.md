# 🔐 Generador de usuarios locales FortiGate

Una herramienta web ágil, segura y ejecutada 100% en el navegador (Client-Side) diseñada para administradores de red y especialistas en ciberseguridad. Permite automatizar la creación de cuentas locales para firewalls FortiGate, generando contraseñas criptográficamente seguras, scripts CLI listos para producción y respaldos en Excel.

## 🚀 Características Principales

* **Procesamiento Masivo:** Carga y procesa grandes listas de cuentas de usuario instantáneamente.
* **Seguridad Criptográfica Avanzada:** Utiliza la API `window.crypto` para generar contraseñas robustas y aleatorias de 12 caracteres para cada cuenta.
* **Integración Directa con FortiGate:** Generación automática del script CLI (`config user local...`) con el formato exacto requerido por FortiOS.
* **Portapapeles Inteligente:** Botón de copiado a un clic para trasladar los comandos generados directamente a la consola del firewall de manera rápida.
* **Respaldos Seguros:** Exportación automática de credenciales a formato Excel (.xlsx) para la gestión y entrega segura a los usuarios.
* **Arquitectura Zero Trust (Privacidad Total):** Al ser una herramienta 100% frontend (Client-Side), ningún dato, usuario o contraseña es enviado a servidores externos. Todo el procesamiento ocurre de manera local y segura en el equipo del administrador.

## 🛠️ Tecnologías Utilizadas

* **Frontend:** HTML5, CSS3, JavaScript (Vanilla).
* **Librerías:** SheetJS (para exportación segura a Excel).
* **Infraestructura:** GitHub Pages.

## 🌐 Acceso a la Herramienta

La herramienta está alojada de forma segura y siempre disponible en el siguiente enlace:
**[🔗 Abrir Generador de usuarios locales FortiGate](https://quantiOCS.github.io/usersfw/)**

---
*Desarrollado y mantenido por kike*
