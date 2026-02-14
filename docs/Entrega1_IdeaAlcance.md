# ENTREGA 1 - IDEA Y ALCANCE DEL PROYECTO

**Asignatura:** Técnicas de Producción Industrial de Software  
**Estudiante:** Edwin Ernesto Ortiz Ascencio
**Fecha:** 13 de febrero de 2026

---

## INTRODUCCIÓN

El presente documento corresponde a la primera entrega del proyecto final de la asignatura, en la cual se define la idea de negocio, el problema a resolver y el alcance de la aplicación móvil Android que se desarrollará durante el curso.

La aplicación propuesta busca optimizar la gestión de servicios técnicos en campo para la empresa OPS Sistemas Operacionales, permitiendo a los técnicos acceder a información relevante en tiempo real y mejorar los tiempos de respuesta del servicio. Este proyecto aplicará un enfoque industrial de desarrollo que incluye levantamiento de requisitos, diseño incremental, implementación con buenas prácticas, pruebas y documentación técnica.

---

## 1. EMPRESA SELECCIONADA Y PROBLEMA

**Empresa:** OPS Sistemas Operacionales  
**Sector:** Servicios técnicos especializados en mantenimiento de equipos de oficina

**Problema identificado:**

Los técnicos de campo actualmente enfrentan limitaciones en la gestión de sus servicios debido a la falta de acceso inmediato a la información de tickets asignados. El proceso actual requiere que el técnico regrese a la oficina para solicitar repuestos, actualizar el estado de los tickets y registrar el cierre de servicios, lo que genera retrasos significativos en los tiempos de respuesta. Adicionalmente, no cuentan con acceso rápido al historial de equipos mientras están en campo, dificultando el diagnóstico y la toma de decisiones durante la visita técnica.

---

## 2. OBJETIVO DE LA APLICACIÓN

Desarrollar una aplicación móvil Android que permita a los técnicos de campo gestionar sus tickets de servicio de manera autónoma y en tiempo real, desde la visualización de asignaciones hasta el cierre completo del servicio con firma digital del cliente. La aplicación también facilitará la consulta de historiales de equipos y la solicitud anticipada de repuestos directamente desde el sitio del cliente.

**Beneficio esperado:**

La implementación de esta solución reducirá considerablemente el tiempo de respuesta del servicio técnico al eliminar desplazamientos innecesarios a la oficina. Los técnicos podrán solicitar repuestos antes de finalizar la visita, optimizando los recursos y mejorando la eficiencia operativa de la empresa. Además, se logrará una trazabilidad completa del estado de cada ticket en tiempo real.

---

## 3. ALCANCE DEL PROYECTO

### Funcionalidades incluidas:

**Módulo de autenticación:**
- Sistema de login individual para cada técnico con validación de credenciales

**Módulo de gestión de tickets (Técnicos):**
- Visualización exclusiva de tickets asignados al técnico autenticado
- Actualización de estados: En camino, En proceso, Completado
- Consulta de información del ticket: cliente, modelo de equipo, número de serie y problema reportado
- Sistema de notificaciones push para nuevos tickets asignados

**Módulo de cierre de servicios:**
- Formulario de cierre con campos específicos:
  - Informe técnico
  - Observaciones
  - Contador Blanco y Negro
  - Contador Color
  - Captura de firma digital del cliente

**Módulo de consulta de equipos:**
- Búsqueda de equipos por número de serie
- Visualización de bitácora e historial de servicios previos del equipo

**Módulo de solicitud de repuestos:**
- Búsqueda de cliente y equipo asignado
- Selección de equipo por número de serie
- Campo de descripción para solicitud de repuestos/tóner
- Envío directo al administrador del sistema

**Módulo administrativo (Jefe Técnico/Administrador):**
- Visualización de todos los tickets del sistema
- Filtros por técnico, estado, fecha y cliente
- Gestión de solicitudes de repuestos recibidas

**Infraestructura técnica:**
- Integración con API REST del sistema existente (conexión vía IP pública)
- Base de datos local con Room para almacenamiento en caché
- Implementación de arquitectura MVVM

### Exclusiones del alcance:

- Creación de nuevos tickets (se realiza desde el sistema principal)
- Asignación de técnicos a tickets (gestión administrativa)
- Control de inventario completo de repuestos
- Funcionamiento sin conexión a internet (modo offline completo)
- Sistema de mensajería interna entre técnicos
- Geolocalización o planificación de rutas
- Generación de reportes en formato PDF
- Alta, baja o modificación de clientes y equipos

---

## 4. LISTA DE PANTALLAS Y FUNCIONES PRINCIPALES

**Pantalla 1 - Login**  
Autenticación del usuario mediante credenciales. Validación contra API del sistema principal.

**Pantalla 2 - Dashboard de Tickets**  
Listado de tickets asignados al técnico con filtros por estado (Pendiente, En camino, En proceso, Completado). Indicadores visuales de prioridad y notificaciones de nuevos tickets.

**Pantalla 3 - Detalle de Ticket**  
Visualización completa de la información del ticket: nombre del cliente, modelo del equipo, número de serie, problema reportado y estado actual. Opciones para cambiar el estado del ticket y acceder a la bitácora del equipo.

**Pantalla 4 - Bitácora de Equipo**  
Búsqueda y consulta del historial de servicios de un equipo mediante su número de serie. Muestra especificaciones técnicas y registro de intervenciones anteriores.

**Pantalla 5 - Formulario de Cierre de Ticket**  
Captura de datos finales del servicio: informe del técnico, observaciones, contadores de impresión (B/N y Color) y firma digital del cliente mediante canvas táctil. Validación de campos obligatorios antes del envío.

**Pantalla 6 - Solicitud de Repuestos**  
Selección de cliente, búsqueda de equipo por serie, campo de descripción de los repuestos necesarios y envío de la solicitud al administrador. Confirmación de recepción.

**Pantalla 7 - Perfil de Usuario**  
Información del técnico autenticado, estadísticas básicas de tickets gestionados y opción de cierre de sesión.

**Pantallas adicionales (roles administrativos):**

**Pantalla 8 - Panel de Control Administrativo**  
Vista global de todos los tickets con filtros avanzados por múltiples criterios.

**Pantalla 9 - Gestión de Solicitudes**  
Listado de solicitudes de repuestos pendientes con opciones de marcado y seguimiento.

---

**Nota:** Este proyecto se desarrollará de forma incremental según el cronograma establecido en el curso, con entregas parciales que permitan validar el progreso y realizar ajustes necesarios en cada fase.
