# 🧪 Postman Echo - Pruebas de API

Este proyecto es un ejercicio de práctica diseñado para consolidar los fundamentos del testing de APIs y la automatización de validaciones básicas. Es mi primer proyecto integrando el flujo de trabajo entre **Postman** y **Newman**.

## 🎯 Objetivos del Proyecto
- Configuración y uso de **Variables de Entorno** para dinamizar las pruebas.
- Implementación de scripts de validación en **JavaScript**.
- Ejecución de colecciones a través de la interfaz de línea de comandos (CLI) con **Newman**.

## 📋 Escenarios de Prueba Cubiertos
- **Validación de Métodos:** Pruebas funcionales sobre el método `GET`.
- **Códigos de Estado:** Verificación de respuestas exitosas (200 OK) y manejo de errores (404 Not Found).
- **Pruebas de Performance:** Validación de tiempos de respuesta inferiores a 800ms.
- **Integridad de Datos:** Comprobación de que los parámetros enviados coinciden con los recibidos en el cuerpo de la respuesta (JSON).

## 🚀 Cómo ejecutar las pruebas
Para correr este proyecto localmente, necesitas tener instalado [Node.js](https://nodejs.org/) y Newman.

1. Instala Newman globalmente:
   ```bash
   npm install -g newman
