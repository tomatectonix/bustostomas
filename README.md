# JARVIS

> Asistente personal desarrollado en C# y .NET, diseñado para experimentar con interacción, automatización, personalidad y seguridad.

##  Descripción

JARVIS es un proyecto personal desarrollado como parte de mi aprendizaje en programación.

La idea es construir progresivamente un asistente capaz de interactuar con el usuario, comprender comandos, responder de forma dinámica y ejecutar determinadas tareas mediante un sistema modular.

El proyecto no busca ser simplemente un chatbot, sino convertirse progresivamente en un asistente personal configurable, donde cada capacidad pueda desarrollarse y mejorarse de forma independiente.

---

##  Objetivos

- Crear un asistente funcional utilizando C#.
- Implementar interacción mediante texto.
- Desarrollar un sistema de personalidad configurable.
- Procesar diferentes tipos de comandos.
- Automatizar tareas.
- Trabajar con archivos y datos.
- Incorporar APIs y servicios externos.
- Implementar un sistema modular.
- Controlar los permisos de las acciones que puede realizar el asistente.
- Registrar las acciones realizadas mediante logs.
- Priorizar la seguridad y el control del usuario.

---

## 🧠 Personalidad

Una de las características principales de JARVIS será su personalidad.

La intención es que el asistente no responda siempre de manera completamente genérica, sino que pueda mantener una identidad y un estilo de comunicación configurables.

A futuro, la personalidad podría incluir:

- Nombre e identidad del asistente.
- Forma de expresarse.
- Preferencias de comunicación.
- Contexto de conversaciones.
- Configuración del comportamiento.
- Diferentes perfiles de personalidad.

La personalidad será una capa independiente de la lógica principal del programa para evitar que ambas partes estén completamente acopladas.

---

##  Arquitectura modular

JARVIS será desarrollado utilizando módulos independientes.

Una posible estructura:

JARVIS
│
├── Core
│   ├── Lógica principal
│   ├── Comandos
│   └── Configuración
│
├── Personality
│   └── Sistema de personalidad
│
├── Commands
│   ├── Sistema
│   ├── Archivos
│   └── Automatización
│
├── Security
│   ├── Permisos
│   └── Validaciones
│
├── Logging
│   └── Registro de acciones
│
└── Integrations
    └── APIs y servicios externos

La estructura podrá cambiar a medida que el proyecto evolucione.

---

##  Sistema de permisos

Una de las características que quiero incorporar al proyecto es un sistema de permisos.

JARVIS no debería poder realizar cualquier acción automáticamente.

Las acciones podrían clasificarse según su nivel de riesgo.

Ejemplo:

### 🟢 Bajo riesgo
- Consultar información.
- Realizar cálculos.
- Mostrar la hora.
- Procesar texto.

### 🟡 Riesgo moderado
- Crear archivos.
- Modificar archivos.
- Ejecutar determinadas tareas.

### 🔴 Alto riesgo
- Eliminar archivos.
- Ejecutar comandos sensibles.
- Modificar configuraciones importantes.

Para determinadas acciones, JARVIS debería solicitar autorización explícita al usuario.

Ejemplo:

> JARVIS necesita acceder a `/Proyectos`.
>
> ¿Autorizás esta acción?
>
> `Sí / No`

El objetivo es que el usuario mantenga el control sobre las acciones realizadas por el asistente.

---

##  Registro de acciones

JARVIS también podrá mantener un registro de determinadas acciones.

Ejemplo:

```text
[23:41] Usuario autorizó acceso a /Proyectos
[23:42] JARVIS creó Proyecto.cs
[23:43] Usuario rechazó acceso a /Privado
