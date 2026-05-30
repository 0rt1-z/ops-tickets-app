#  OPS Tickets - App de Gestión de Servicio Técnico

Aplicación móvil Android desarrollada en Kotlin para la gestión de tickets de servicio técnico en campo.

## Descripción del Proyecto

App desarrollada para **OPS Sistemas Operacionales** que permite a los técnicos de campo gestionar sus tickets de servicio, consultar historiales de equipos y solicitar repuestos en tiempo real, mejorando significativamente los tiempos de respuesta y la eficiencia operativa.

## Objetivo

Optimizar los tiempos de respuesta del servicio técnico mediante acceso móvil a información crítica y gestión autónoma de tickets desde el campo, eliminando la necesidad de regresar a la oficina para actualizar estados o solicitar repuestos.

## Funcionalidades Principales

### Para Técnicos:
- 🔐 Login individual con credenciales únicas
- 📋 Visualización de tickets asignados
- 🔄 Actualización de estados (En camino, En proceso, Completado)
- 📝 Formulario de cierre con firma digital del cliente
- 🔍 Consulta de bitácora de equipos por número de serie
- 🛠️ Solicitud de repuestos directamente al administrador
- 🔔 Notificaciones push de nuevos tickets asignados

### Para Administradores:
- 👀 Vista completa de todos los tickets
- 🔎 Filtros avanzados (técnico, estado, fecha, cliente)
- 📦 Gestión de solicitudes de repuestos

## 🛠️ Tecnologías

- **Lenguaje:** Kotlin
- **Plataforma:** Android SDK
- **Base de datos:** Room (SQLite)
- **Networking:** Retrofit (API REST)
- **Arquitectura:** MVVM
- **UI/UX:** Material Design 3
- **Notificaciones:** Firebase Cloud Messaging
- **Control de versiones:** Git + GitHub

## 📚 Documentación

- [📄 Entrega 1 - Idea y Alcance](docs/Entrega1_IdeaAlcance.md)
- [📄 Entrega 2 - Requisitos y Prototipo](docs/Entrega2_OPSTickets.docx)

## 📂 Estructura del Proyecto

```
ops-tickets-app/
├── app/
│   └── src/main/java/com/example/ops/
│       ├── MainActivity.kt                    # Punto de entrada
│       ├── network/
│       │   └── ApiService.kt                 # Servicios REST
│       ├── ui/theme/
│       │   ├── PantallaMenu.kt              # Menú principal
│       │   ├── PantallasTickets.kt          # Lista y detalle de tickets
│       │   ├── PantallaCerrarTicket.kt      # Formulario de cierre
│       │   ├── PantallaProximamente.kt      # Placeholders
│       │   ├── Color.kt                      # Paleta de colores
│       │   ├── Theme.kt                      # Tema Material 3
│       │   └── Type.kt                       # Tipografía
│       └── viewmodel/
│           └── TicketViewModel.kt            # Gestión de estado
├── docs/                                      # Documentación del proyecto
│   ├── Entrega1_IdeaAlcance.md
│   └── Entrega2_OPSTickets.docx
├── .gitignore
└── README.md
```

## 🏗️ Arquitectura Técnica

La aplicación sigue el patrón **MVVM** (Model-View-ViewModel) con Jetpack Compose, proporcionando una arquitectura escalable y mantenible:

- **UI Layer (Jetpack Compose):** Componentes visuales y navegación
- **ViewModel:** Gestión de estado y lógica de presentación
- **Repository:** Abstracción de fuentes de datos
- **Network:** Servicios REST mediante Retrofit
- **Local Storage:** Persistencia con Room Database

## 🧭 Navegación

La app utiliza Jetpack Compose con navegación **type-safe** mediante sealed classes:

### Pantallas Implementadas (✅):
- **Menú Principal** - Dashboard de navegación con 3 opciones
- **Lista de Tickets** - Visualización de tickets con filtros por estado
- **Detalle de Ticket** - Información completa del ticket seleccionado
- **Cierre de Ticket** - Formulario con firma digital del cliente

### Pantallas en Desarrollo (🔄):
- **Bitácora de Equipo** - Historial de servicios por número de serie
- **Solicitud de Repuestos** - Formulario de solicitud de insumos

### Flujo de Navegación:
```
┌─────────────┐
│   MENÚ      │
└──────┬──────┘
       │
       ├─→ TICKETS
       │    ├─→ LISTA
       │    │    └─→ DETALLE
       │    │         ├─→ CIERRE
       │    │         ├─→ BITÁCORA
       │    │         └─→ REPUESTOS
       │    │
       │
       ├─→ BITÁCORA
       │    └─→ HISTORIAL
       │
       └─→ SOLICITAR REPUESTOS
            └─→ FORMULARIO
```

## 🚀 Roadmap del Proyecto

- [x] ✅ **Fase 1:** Definición de idea y alcance (Febrero 2026)
- [x] ✅ **Fase 2:** Requisitos y prototipo (29 de Mayo 2026)
- [ ] ⏳ **Fase 3:** Arquitectura y base técnica
- [ ] ⏳ **Fase 4:** Persistencia y CRUD
- [ ] ⏳ **Fase 5:** Funciones avanzadas
- [ ] ⏳ **Fase 6:** Entrega final y publicación

## 👨‍💻 Autor

**Edwin Ernesto Ortiz Ascencio**  
Proyecto Final - Técnicas de Producción Industrial de Software (Online)  
Universidad Tecnológica de El Salvador

## 📅 Estado Actual

🟢 **En desarrollo** - Entregas 1 y 2 completadas (29 de Mayo 2026)

- ✅ Entrega 1: Idea y Alcance
- ✅ Entrega 2: Requisitos y Prototipo (4 pantallas implementadas)
- 🔄 Entrega 3: Arquitectura y Base Técnica (En progreso)

**Empresa:** OPS Sistemas Operacionales  
**Sector:** Servicios técnicos especializados  
**Repositorio:** GitHub - ops-tickets-app

