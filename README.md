# Kanban Board con Google Auth - Práctica React

Este proyecto implementa un tablero Kanban funcional con un sistema de autenticación basado en Google Identity Services y persistencia de datos local.

## 🚀 Funcionalidades Implementadas

### 1. Autenticación (Google One Tap & Button)
- **Integración oficial:** Uso de la librería `https://accounts.google.com/gsi/client`.
- **Manejo de JWT:** Extracción de datos del usuario (Nombre, Foto, Email) mediante la decodificación del token de Google.
- **Sesión persistente:** El estado del usuario se mantiene tras recargar la página (F5) mediante `localStorage`.

### 2. Tablero Kanban
- **Gestión de Tareas:** Creación de tareas vinculadas automáticamente al autor logueado.
- **Flujo de Estados:** Movimiento dinámico de tareas entre las columnas: *To Do*, *In Progress* y *Done*.
- **Autoría:** Cada tarea muestra el nombre del usuario de Google que la creó, cumpliendo con el requisito de vinculación de datos.

### 3. Arquitectura Técnica
- **Context API:** Uso de `AuthContext` y `TaskContext` para una gestión de estado global limpia y eficiente.
- **Persistencia:** Sincronización automática de todas las tareas con el almacenamiento local del navegador.

## 🛠️ Instrucciones para el corrector

1. Ejecutar `npm install` para instalar las dependencias.
2. Ejecutar `npm start` para iniciar la aplicación.
3. **Nota sobre Google Auth:** Para que el login funcione, el origen `http://localhost:3000` debe estar autorizado en la consola de Google Cloud (configurado en el Client ID del proyecto).
