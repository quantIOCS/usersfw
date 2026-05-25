# usersfw
# 🔐 Generador de Cuentas Firewall (Secure & Client-Side)

Una herramienta web ágil y segura diseñada para administradores de red y especialistas en ciberseguridad. Permite procesar listas masivas de usuarios, generar contraseñas criptográficamente seguras y exportar scripts CLI listos para ser implementados en FortiGate, además de un respaldo en Excel protegido.


## 🛡️ Arquitectura de Seguridad (Zero Trust)

Al estar alojada en una URL pública, es natural preguntarse sobre la privacidad de las credenciales generadas. Esta herramienta está diseñada bajo un enfoque **100% Client-Side**:

* **Cero Servidores (No Backend):** Todo el procesamiento ocurre de manera local en la memoria RAM de tu navegador web. Ningún dato (usuarios, contraseñas o nombres de grupos) se envía a internet, bases de datos o APIs de terceros.
* **Criptografía Robusta:** No usamos funciones matemáticas simples. Las contraseñas (18 caracteres) se generan utilizando la API de hardware del navegador `window.crypto.getRandomValues()`, lo que garantiza una aleatoriedad de grado militar, resistente a la predicción y fuerza bruta.
* **Exportación Segura Local:** El archivo Excel se construye en tu equipo y se empaqueta instantáneamente en un `.zip` protegido por cifrado AES mediante una contraseña maestra elegida por ti. El archivo resultante se descarga directamente desde tu propio navegador a tu disco duro.

## ✨ Características Principales

1. **Anti-Duplicados:** Detecta y elimina automáticamente usuarios repetidos en tu lista antes del procesamiento.
2. **Lógica de FortiGate:** Permite elegir entre crear grupos nuevos (`set member`) o agregar usuarios a grupos existentes sin borrar a los anteriores (`append member`).
3. **ZIP Encriptado:** Genera un archivo `.xlsx` de respaldo, empaquetado dentro de un archivo `.zip` que exige contraseña maestra para ser extraído.
4. **Script CLI Listo:** Entrega el código de línea de comandos en pantalla para copiar y pegar directamente en la consola del firewall.

## 🚀 Cómo utilizar la herramienta

1. Ingresa al [enlace de la herramienta](#).
2. Escribe el **Nombre del Grupo** correspondiente en el firewall.
3. Selecciona si el grupo ya existe (para aplicar un *append* de usuarios) o si es nuevo.
4. Pega tu lista de usuarios (un usuario por línea).
5. Haz clic en **⚡ Procesar Usuarios**.
6. Copia el **Script CLI** para implementarlo en tu equipo.
7. Haz clic en **📦 Descargar ZIP Protegido**, define una contraseña maestra que solo tú conozcas, y guarda el respaldo de forma segura.

## 🛠️ Tecnologías Utilizadas

Esta herramienta funciona en un único archivo `index.html` estático, apoyándose en las siguientes librerías de código abierto cargadas vía CDN:
* [ExcelJS](https://github.com/exceljs/exceljs) - Lectura y escritura del documento XLSX.
* [FileSaver.js](https://github.com/eligrey/FileSaver.js/) - Gestión de descargas en el cliente.
* [zip.js](https://gildas-lormeau.github.io/zip.js/) - Compresión y cifrado AES del archivo ZIP en el navegador.

---

### ⚠️ Descargo de Responsabilidad (Disclaimer)
*Este proyecto es de código abierto y se proporciona "tal cual" sin garantía explícita. El usuario es el único responsable de salvaguardar la contraseña maestra del archivo ZIP y del manejo seguro de las credenciales generadas.*
