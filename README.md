# CapstoneAgecare
Capstone Agecare


# AgeCare

## Tranquilidad a Distancia

AgeCare es una plataforma digital integral de cuidado de adultos mayores. Diseñada para dar tranquilidad a las familias que cuidan a un ser querido a distancia, AgeCare reúne en un único lugar todo lo necesario para el bienestar y monitoreo de adultos mayores.

---

## Características Principales

### Monitoreo de Salud en Tiempo Real
Acceso centralizado al estado de salud del adulto mayor, medido por dispositivos vestibles (wearables) e integrado en una vista única y coherente.

### Sistema Inteligente de Alertas
Notificaciones automáticas y contextuales que mantienen informados a los cuidadores y familiares sobre cambios significativos en la salud.

### Comunicación Asistida por IA
Herramientas de comunicación potenciadas con inteligencia artificial que facilitan la interacción entre todos los actores del ecosistema de cuidado.

### Vistas Diferenciadas por Rol
Cada usuario accede a la información y funcionalidades diseñadas específicamente para su rol:
- **Familiar**: Observa el estado de salud y recibe alertas
- **Cuidador**: Opera el día a día y captura datos del paciente
- **Médico**: Prescribe y ajusta el plan de medicamentos
- **Adulto Mayor**: Interfaz radicalmente simple, accesible y de voz primero

### Interfaz Voice-First para Adultos Mayores
Diseño accesible y orientado a voz que mantiene conectado, acompañado y estimulado al adulto mayor, promoviendo su participación activa.

---

## Equipo

- **Franco Barra** - Desarrollo
- **Claudia Iosue** - Desarrollo
- **Felipe Varas** - Desarrollo
- **César Gacitúa** - Fullstack

---

## Proyecto Capstone

AgeCare es el proyecto de capstone para el título de Ingeniero Informático en Duoc UC, Escuela de Informática y Telecomunicaciones.

---

## Estructura del Proyecto

```
agecare/
├── docs/              # Documentación del proyecto
├── src/               # Código fuente
├── tests/             # Pruebas unitarias e integración
├── deployment/        # Configuración de despliegue
└── README.md          # Este archivo
```

---

## Arquitectura

AgeCare está compuesto por tres frentes de desarrollo con datos compartidos del paciente:

**App Flutter (agecare_app)**
Aplicación móvil multiplataforma (iOS y Android) con interfaz accesible y voice-first para adultos mayores, cuidadores y familiares.

**Backend (FastAPI)**
API REST y WebSocket que centraliza la persistencia de datos, lógica de negocio, gestión de alertas y comunicación en tiempo real. Arquitectura planificada: FastAPI + PostgreSQL en Azure.

**Panel de Administración Web**
Interfaz web para médicos y administradores del sistema.

---

## Tecnologías

App Flutter
- Flutter SDK 3.4.0 o superior
- Dart 3.4.0+
- Firebase para notificaciones push
- Spike API para integración de wearables
- Health Kit (iOS) y Health Connect (Android)

Backend (Especificación)
- FastAPI con Python 3.12+
- PostgreSQL (Azure Database)
- Azure App Service o Container Apps
- Azure Blob Storage
- Azure Notification Hubs
- WebSockets para comunicación en tiempo real

---

## Comenzando

### Requisitos

- Flutter SDK versión 3.4.0+
- Xcode (para iOS) y/o Android Studio (para Android)
- Cuenta Firebase configurada
- Acceso a credenciales de Spike API (opcional, para integración de wearables real)

### Instalación rápida (modo demo)

```bash
flutter pub get
flutter run --dart-define=USE_MOCKS=true
```

Usuario de prueba: demo@agecare.app / agecare123

### Instalación con backend real

```bash
flutter run \
  --dart-define=USE_MOCKS=false \
  --dart-define=API_BASE_URL=https://api-dev.agecare.app \
  --dart-define=SPIKE_APP_ID=1234
```

### Variables de configuración

La app se configura mediante dart-define en tiempo de compilación:

- `USE_MOCKS` (bool, defecto: true) — Activa el modo demo sin backend
- `API_BASE_URL` (string, defecto: https://api-dev.agecare.app) — Endpoint del backend
- `SPIKE_APP_ID` (int, defecto: 0) — Identificador para integración de wearables
- `USE_WEARABLE_SIMULATOR` (bool, defecto: true) — Simulador de dispositivo vestible

### Dependencias externas

- **Backend AgeCare**: Persistencia y lógica de negocio
- **Firebase / FCM**: Notificaciones push
- **Spike API**: Integración de wearables (HealthKit, Health Connect, Garmin, Whoop)
- **Azure Notification Hubs**: Distribución de notificaciones
- **App Store Connect / Google Play Console**: Compras in-app

---

## Documentación

Ver Guía de Instalación y Despliegue para detalles completos sobre:
- Configuración de cada frente (Flutter, Backend, Web Admin)
- Variables de entorno
- Pasos de build para release
- Integración con servicios externos

---

## Licencia

[Especificar la licencia del proyecto]

---

*Última actualización: Septiembre 2026*
