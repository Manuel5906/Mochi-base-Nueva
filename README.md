# 🌀 Mochi Bot - Sub-Bot Management Panel

Mochi Bot es una plataforma avanzada de gestión de sub-bots para WhatsApp, construida sobre la librería **Baileys**. Permite a los usuarios vincular sus propias cuentas al sistema principal mediante un panel web intuitivo, ofreciendo control total sobre sus sesiones en tiempo real.

---

## 🚀 Características Principales

* **Doble Método de Vinculación:** Escaneo de código QR tradicional o uso de **Pairing Code** (código de 8 dígitos) para mayor comodidad.
* **Gestión Multi-Sesión:** Administra múltiples sub-bots de forma simultánea desde una sola interfaz.
* **Switches de Configuración Real-Time:** * **Bienvenida:** Activa o desactiva mensajes automáticos al entrar nuevos miembros.
    * **Solo Privados:** Filtra el bot para que solo responda en chats individuales, ignorando grupos.
* **Auto-Reconexión:** Sistema inteligente de recuperación ante desconexiones accidentales.
* **Persistencia de Sesiones:** Carga automática de todos los sub-bots vinculados al reiniciar el servidor principal.
* **Seguridad y Limpieza:** Opción de eliminación completa de sesión que borra credenciales del disco para proteger la privacidad.

---

## 🛠️ Tecnologías Utilizadas

* **Backend:** Node.js & Express.
* **WhatsApp Library:** `@whiskeysockets/baileys`.
* **Frontend:** HTML5, Tailwind CSS (estilo glassmorphism), Lucide Icons.
* **Notificaciones:** SweetAlert2 para alertas interactivas.
* **Logs:** Pino & Chalk para un monitoreo visual en consola.

---

## 📂 Estructura del Código Core

| Archivo | Función |
| :--- | :--- |
| `jadibot-manager.js` | Lógica de conexión, manejo de eventos de Baileys y gestión de mapas de sesiones. |
| `app.js` | Servidor web Express, rutas de API y renderizado del Dashboard. |
| `/jadibots_sesiones/` | Almacenamiento local de tokens de autenticación (creds.json). |
| `handler.js` | El procesador central que decide cómo responder a los mensajes recibidos. |

---

## ⚙️ Instalación y Uso

1.  **Instalar dependencias:**
    ```bash
    npm install
    ```

2.  **Iniciar el sistema principal:**
    ```bash
    npm start
    ```

3.  **Acceder al panel:**
    Abre tu navegador en `http://localhost:3000` e inicia sesión.

4.  **Vincular un Sub-Bot:**
    Ingresa el número en formato internacional (ej: `5199999998`), elige el método (QR o Código) y sigue las instrucciones en pantalla.

---

## ⚠️ Notas Importantes

* **Privacidad:** Nunca compartas la carpeta `jadibots_sesiones`. Contiene los archivos de autenticación que permiten el acceso total a las cuentas de WhatsApp vinculadas.
* **Navegador:** El sistema utiliza una emulación de "Ubuntu / Chrome" para evitar conflictos de sesión con WhatsApp Web.

---

## 👤 Créditos

Desarrollado como parte del ecosistema **Mochi Bot**.
Creador --> **Manuel VG**

> **Aviso:** Este proyecto es para fines educativos. El uso indebido para spam puede resultar en el baneo de la cuenta de WhatsApp por parte de Meta.
