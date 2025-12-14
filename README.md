# 🏦 Sistema de Cola de Turnos - React + Relay Gateway

Sistema de gestión de turnos tipo banco construido con **React** y [Relay Gateway](https://github.com/Coderic/Relay).

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)
![Vite](https://img.shields.io/badge/Vite-5-646CFF?logo=vite)
![Relay](https://img.shields.io/badge/Relay-Gateway-blueviolet)

## 🚀 Inicio Rápido

### Prerrequisitos

Relay Gateway ejecutándose en `http://localhost:5000`:

```bash
npx relay-gateway
```

### Usar este template

1. Haz clic en **"Use this template"** en GitHub
2. Crea tu nuevo repositorio
3. Clona y ejecuta:

```bash
git clone tu-repositorio
cd tu-repositorio
npm install
npm run dev
```

## 📖 Características

- **Vista Usuario**: Solicitar turno (Cajero o Ejecutivo)
- **Vista Administración**: Ver cola completa en tiempo real
- **Vista Operador**: Atender turnos (múltiples operadores simultáneos)
- **Notificaciones**: Alertas cuando es tu turno
- **Tiempo estimado**: Cálculo automático de espera

## 🎯 Casos de Uso

- 🏦 Bancos y entidades financieras
- 🏥 Clínicas y hospitales
- 🏛️ Oficinas públicas
- 🛒 Atención al cliente
- 📞 Call centers

## 💻 Uso del Hook

```jsx
import { useRelay } from './hooks/useRelay';

function MiComponente() {
  const { connected, enviarATodos, onMensaje } = useRelay('mi-usuario-id');

  useEffect(() => {
    const unsubscribe = onMensaje((data) => {
      if (data.tipo === 'turno_llamando') {
        // ¡Tu turno está siendo llamado!
      }
    });
    return unsubscribe;
  }, [onMensaje]);
}
```

## 📁 Estructura

```
src/
├── hooks/
│   └── useRelay.js    # Hook React para Relay
├── App.jsx               # Componente principal
├── App.css               # Estilos
└── main.jsx              # Entry point
```

## 🔗 Enlaces

- [Relay Gateway](https://github.com/Coderic/Relay)
- [Documentación](https://coderic.github.io/Relay/)
- [Otros ejemplos](https://github.com/Coderic?q=relay-ejemplo)

## 📄 Licencia

MIT © [Coderic](https://github.com/Coderic)
