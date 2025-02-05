**Rol: Administrador**

+ index.html (Inicio de Sesión)
|   └── dashboard.html (Dashboard Administrador / Gestión de Periodos)
|       ├── Sidebar
|       |   ├── Periodos (dashboard.html - Activo)
|       |   ├── Puntos de Evaluación (puntos-evaluacion.html)
|       |   ├── Docentes (docentes-listado.html)
|       |   └── Configuración (configuracion.html)
|       ├── Contenido Principal
|       |   ├── Gráficas Dashboard
|       |   └── Sección Gestión de Periodos
|       |       └── Tabla de Periodos
|       |           └── Botón "Evaluaciones" (enlace a evaluaciones-periodo.html)
|       └── Navbar
|           └── Dropdown "Perfil Usuario"
|               ├── Mi Perfil (perfil.html)
|               └── Cerrar Sesión (index.html)
|
├── puntos-evaluacion.html (Gestión de Puntos de Evaluación)
|   ├── Sidebar (Mismo que dashboard.html, "Puntos de Evaluación" Activo)
|   ├── Contenido Principal
|   |   ├── Título y Descripción
|   |   └── Card Catálogo de Puntos de Evaluación
|   |       └── Tabla de Puntos de Evaluación
|   |           └── Botones "Editar", "Deshabilitar/Habilitar"
|   └── Navbar (Mismo que dashboard.html)
|
├── docentes-listado.html (Listado de Docentes)
|   ├── Sidebar (Mismo que dashboard.html, "Docentes" Activo)
|   ├── Contenido Principal
|   |   ├── Gráficas Superiores (Pastel: Divisiones y Tipos de Contrato)
|   |   ├── Card Filtros de Búsqueda
|   |   └── Card Lista de Docentes
|   |       └── Tabla de Docentes
|   |           └── Botón "Histórico" (enlace a historico-docente.html)
|   |       └── Paginación
|   └── Navbar (Mismo que dashboard.html)
|
├── configuracion.html (Configuración del Sistema)
|   ├── Sidebar (Mismo que dashboard.html, "Configuración" Activo)
|   ├── Contenido Principal
|   |   ├── Título y Descripción
|   |   ├── Sección Configuración General
|   |   └── Sección Configuración Global de Puntos de Evaluación (Tabla Checkboxes)
|   └── Navbar (Mismo que dashboard.html)
|
├── evaluaciones-periodo.html (Evaluaciones del Periodo - Vista Detallada)
|   ├── Sidebar (Mismo que dashboard.html, "Periodos" Activo)
|   ├── Contenido Principal
|   |   ├── Título y Descripción del Periodo
|   |   └── Sección por cada Punto de Evaluación (10 secciones)
|   |       ├── Título del Punto
|   |       ├── Gráficas (Promedio por División y Tipo de Docente)
|   |       └── Tabla de Docentes Evaluados en el Punto
|   └── Navbar (Mismo que dashboard.html)
|
├── evaluacion.html (Página de Evaluación de un Docente)
|   ├── Sidebar (Mismo que dashboard.html, "Periodos" Activo)
|   ├── Contenido Principal
|   |   ├── Título del Periodo y Docente
|   |   └── Card Formulario de Evaluación (10 campos numéricos para los Puntos)
|   |   └── Card Lista de Docentes Pendientes/Completadas
|   └── Navbar (Mismo que dashboard.html)
|
├── perfil.html (Perfil de Usuario Administrador)
|   ├── Sidebar (Mismo que dashboard.html, "Periodos" Activo)
|   ├── Contenido Principal
|   |   ├── Título "Mi Perfil"
|   |   └── Card Formulario Perfil (Datos Usuario)
|   └── Navbar (Mismo que dashboard.html)
|
└── gestion-evaluadores.html (Gestión de Evaluadores por Punto)
    ├── Sidebar (Mismo que dashboard.html, "Docentes" Activo)
    ├── Contenido Principal
    |   ├── Título y Descripción
    |   └── Card Lista de Evaluadores (para el punto específico)
    |       └── Tabla de Evaluadores
    |           └── Botones "Editar", "Compartir"
    └── Navbar (Mismo que dashboard.html)


**Rol: Evaluador**

+ evaluador-login.html (Inicio de Sesión Evaluador)
|   └── evaluador-dashboard.html (Dashboard Evaluador / Listado de Periodos)
|       ├── Sidebar
|       |   ├── Volver al Dashboard (dashboard.html - Oculto en este dashboard)
|       |   ├── Logo UTEZ
|       |   ├── Menú Evaluador
|       |   |   ├── Periodos (evaluador-dashboard.html - Activo)
|       |   |   ├── Docentes (evaluador-docentes.html)
|       |   |   └── Mi Perfil (perfil-evaluador.html)
|       ├── Contenido Principal
|       |   ├── Título y Bienvenida
|       |   └── Card Periodos de Evaluación Activos
|       |       └── Lista de Periodos
|       |           └── Botón "Evaluar" (enlace a evaluador-captura-evaluacion.html si activo, evaluador-ver-evaluacion.html si inactivo)
|       └── Navbar
|           └── Dropdown "Perfil Usuario"
|               ├── Mi Perfil (perfil-evaluador.html)
|               └── Cerrar Sesión (index.html)
|
├── evaluador-docentes.html (Listado de Docentes - Vista Evaluador)
|   ├── Sidebar (Mismo que evaluador-dashboard.html, "Docentes" Activo)
|   ├── Contenido Principal
|   |   ├── Título y Descripción (División DATID)
|   |   ├── Card Filtros de Búsqueda (Nombre y Tipo de Contrato)
|   |   └── Card Tabla de Docentes (Filtrada a División DATID)
|   |       └── Tabla de Docentes
|   |           └── Botón "Histórico" (enlace a evaluador-historico-docente.html)
|   |       └── Paginación
|   └── Navbar (Mismo que evaluador-dashboard.html)
|
├── evaluador-captura-evaluacion.html (Captura de Evaluación - Periodo Activo - Evaluador)
|   ├── Sidebar (Mismo que evaluador-dashboard.html, "Periodos" Activo)
|   ├── Contenido Principal
|   |   ├── Título y Descripción (Periodo, Punto de Evaluación, División)
|   |   ├── Card Filtros de Docentes (Nombre y Tipo de Contrato)
|   |   └── Card Tabla de Docentes (para captura de calificaciones)
|   |       └── Tabla de Docentes
|   |           └── Campo Input Numérico "Calificación" por docente
|   |       └── Botones "Registrar Calificaciones", "Cancelar"
|   └── Navbar (Mismo que evaluador-dashboard.html)
|
├── evaluador-ver-evaluacion.html (Ver Evaluación - Periodo Finalizado - Evaluador)
|   ├── Sidebar (Mismo que evaluador-dashboard.html, "Periodos" Activo)
|   ├── Contenido Principal
|   |   ├── Título y Descripción (Periodo Finalizado, Punto de Evaluación, División, "Vista Solo Lectura")
|   |   ├── Card Filtros de Docentes (Nombre y Tipo de Contrato)
|   |   └── Card Tabla de Docentes (Vista de evaluaciones capturadas - Read-Only)
|   |       └── Tabla de Docentes
|   |           └── Calificación mostrada como texto (no editable)
|   |       └── Botón "Volver"
|   └── Navbar (Mismo que evaluador-dashboard.html)
|
├── evaluador-historico-docente.html (Histórico de Evaluación Docente - Vista Evaluador)
|   ├── Sidebar (Mismo que evaluador-dashboard.html, "Docentes" Activo)
|   ├── Contenido Principal
|   |   ├── Título y Descripción (Punto de Evaluación específico, Docente)
|   |   ├── Card Promedio General (para el Punto de Evaluación)
|   |   └── Card Tabla Cardex (Histórico por Periodo - Solo Punto de Evaluación)
|   |       └── Tabla Cardex (Periodo vs. Punto de Evaluación)
|   └── Navbar (Mismo que evaluador-dashboard.html)
|
└── perfil-evaluador.html (Perfil de Usuario Evaluador)
    ├── Sidebar (Mismo que evaluador-dashboard.html, "Periodos" Activo)
    ├── Contenido Principal
    |   ├── Título "Mi Perfil de Evaluador"
    |   ├── Card "Cambiar Contraseña" (Formulario)
    |   └── Card "Tokens de Acceso Temporal"
    |       └── Botón "Generar Token" (Modal)
    |       └── Tabla de Tokens Generados
    |           └── Botón "Enviar Correo" (Modal)
    └── Navbar (Mismo que evaluador-dashboard.html)
