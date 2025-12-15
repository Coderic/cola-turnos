# 🏦 Sistema de Cola de Turnos - React + Relay Gateway

Sistema de gestión de turnos tipo banco con múltiples operadores construido con **React** y **[Relay Gateway](https://github.com/Coderic/Relay)**.

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)
![Vite](https://img.shields.io/badge/Vite-5-646CFF?logo=vite)
![Relay](https://img.shields.io/badge/Relay-Gateway-blueviolet)

## 📖 Sobre este Ejemplo

Este ejemplo funcional demuestra cómo construir un sistema de gestión de cola de turnos en tiempo real, similar a los sistemas usados en bancos, oficinas públicas o servicios al cliente. Este ejemplo muestra:

- 🎫 **Solicitud de turnos** - Los clientes pueden solicitar un turno para ser atendidos
- 👨‍💼 **Múltiples operadores** - Varios operadores pueden atender turnos simultáneamente
- ⚡ **Actualización en tiempo real** - Los turnos se actualizan instantáneamente en todas las pantallas
- 📊 **Pantalla de turnos** - Visualización pública de los turnos en curso
- 🔔 **Notificaciones** - Alertas cuando es tu turno o cuando un operador está disponible
- 📈 **Estadísticas** - Tiempo de espera, turnos atendidos, operadores activos

Este ejemplo pertenece a la colección de ejemplos de **[Relay Gateway](https://github.com/Coderic/Relay)**, un gateway de comunicación en tiempo real diseñado para ser inmutable y agnóstico.

## 🚀 Inicio Rápido

### Prerrequisitos

- Node.js 18+ o Docker
- Relay Gateway ejecutándose (ver [documentación de Relay](https://relay.coderic.net))

### Instalación

```bash
# Clonar el repositorio
git clone https://github.com/Coderic/cola-turnos.git
cd cola-turnos

# Instalar dependencias
npm install
```

### Configuración

Asegúrate de tener Relay Gateway ejecutándose. Puedes usar el endpoint público para pruebas:

```javascript
// En tu código, el conector se conecta a:
const relay = new RelayConector('http://demo.relay.coderic.net');
```

O ejecuta Relay localmente:

```bash
# Opción 1: Con npx (recomendado para pruebas)
npx @coderic/relay

# Opción 2: Con Docker Compose
docker compose up -d
```

### Desarrollo

```bash
# Iniciar servidor de desarrollo
npm run dev
```

Abre tu navegador en `http://localhost:5173` (o el puerto que Vite asigne).

### Producción

```bash
# Construir para producción
npm run build

# Los archivos estarán en la carpeta dist/
```

## 🎯 Uso

1. **Abrir múltiples pestañas** para simular diferentes roles:
   - **Cliente**: Solicita turnos y espera ser atendido
   - **Operador**: Atiende turnos y los marca como completados
   - **Pantalla pública**: Muestra los turnos en curso
2. **Solicitar un turno** como cliente
3. **Atender turnos** como operador - Los turnos se asignan automáticamente
4. **Observar** cómo los turnos se actualizan en tiempo real en todas las pantallas

## 🔗 Enlaces

- 📦 [Repositorio](https://github.com/Coderic/cola-turnos)
- 🐛 [Issues](https://github.com/Coderic/cola-turnos/issues)
- 🌐 [Demo en línea](https://coderic.org/cola-turnos/)
- 📚 [Documentación de Relay](https://relay.coderic.net)
- ⚡ [Relay Gateway](https://github.com/Coderic/Relay)

## 🛠️ Tecnologías

- **React** - Biblioteca JavaScript para construir interfaces de usuario
- **Vite** - Build tool y dev server
- **Relay Gateway** - Gateway de comunicación en tiempo real
- **Socket.io** - Comunicación WebSocket

## 📝 Licencia

MIT
