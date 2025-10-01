# 📹 API de Búsqueda de Videos de YouTube con Geolocalización
## Proyecto de Plataforma de Búsqueda Localizada

---

## 💡 Introducción

[cite_start]Este documento presenta el proyecto para el desarrollo de una **API Web** de búsqueda y reproducción de videos de YouTube con **filtros geográficos específicos** para la región de **Valles Centrales, Oaxaca, México**[cite: 31, 32].

[cite_start]El objetivo principal es permitir a desarrolladores y usuarios en esta área encontrar **contenido relevante y localizado** sobre su folclor[cite: 32]. [cite_start]La API utilizará la geolocalización del usuario y códigos de estado/región para asegurar que los resultados de búsqueda se adapten a la ubicación específica, buscando videos en un radio de **10 kilómetros**[cite: 33].

### Problema que Resuelve

[cite_start]Los usuarios en los Valles Centrales tienen dificultad para encontrar contenido localmente relevante en YouTube, ya que el algoritmo a menudo presenta resultados globales o genéricos[cite: 37, 38]. [cite_start]Esto obliga a los usuarios a navegar manualmente y dificulta la visibilidad del talento y negocios locales[cite: 39, 41, 42].

---

## ✅ Requerimientos del Software

### Requerimientos Funcionales (RF)

| ID | Requerimiento | Descripción Clave | Prioridad |
| :--- | :--- | :--- | :--- |
| **RF1** | Búsqueda por ubicación | [cite_start]Filtrar videos por coordenadas de latitud y longitud, con un radio de búsqueda de **10 km**[cite: 65, 69]. | [cite_start]Alta [cite: 69] |
| **RF2** | Filtro regional | [cite_start]Limitar los resultados a videos relevantes únicamente para el estado de **Oaxaca en los Valles Centrales**[cite: 66, 69]. | [cite_start]Alta [cite: 69] |
| **RF3** | Reproducción de video | [cite_start]Proporcionar los videos encontrados en un formato que permita su **reproducción por URL** o reproductor multimedia[cite: 67, 69]. | [cite_start]Alta [cite: 69] |
| **RF4** | Manejo de parámetros | [cite_start]Aceptar y procesar el término de búsqueda, la ubicación (coordenadas) y el radio de 10 km[cite: 68, 69]. | [cite_start]Alta [cite: 69] |

### Requerimientos No Funcionales (RNF)

| ID | Requerimiento | Descripción Clave | Prioridad |
| :--- | :--- | :--- | :--- |
| **RNF1** | Documentación clara | [cite_start]Contar con una documentación clara y compresible para facilitar la integración a desarrolladores[cite: 71, 77]. | [cite_start]Alta [cite: 77] |
| **RNF2** | Respuestas estándar | [cite_start]Devolver los resultados de búsqueda en un formato **JSON** estructurado y consistente[cite: 72, 77]. | [cite_start]Alta [cite: 77] |
| **RNF4** | Arquitectura Web | [cite_start]La API debe estar orientada **exclusivamente a plataformas web**[cite: 74, 77]. | [cite_start]Alta [cite: 77] |
| **RNF5** | Autenticación segura | [cite_start]Implementar medidas de seguridad para proteger las claves de la API de Google[cite: 75, 77]. | [cite_start]Alta [cite: 77] |
| **RNF6** | Protección de datos | [cite_start]**No debe almacenar información personal** de los usuarios[cite: 76, 77]. | [cite_start]Alta [cite: 77] |
| **RNF3** | Escalabilidad | [cite_start]Diseñada para manejar un gran volumen de solicitudes sin comprometer el rendimiento[cite: 73, 77]. | [cite_start]Media [cite: 77] |

---

## 📐 Enfoque Metodológico

[cite_start]Para la gestión y el desarrollo del proyecto se adoptará la metodología ágil **Scrum**[cite: 79]. [cite_start]Esto permitirá la adaptación a necesidades cambiantes, mejor comunicación en el equipo y entrega continua de valor[cite: 80].

### Product Backlog: Historias de Usuario (Selección)

El *Product Backlog* se compone de varias historias de usuario, incluyendo:

| HU | Nombre de la Historia | Descripción Clave | Usuario | Prioridad |
| :--- | :--- | :--- | :--- | :--- |
| **HU001** | Búsqueda por ubicación | [cite_start]Buscar videos de YouTube filtrando por ubicación para obtener contenido **cercano**[cite: 84]. | [cite_start]Cliente [cite: 84] | [cite_start]Alto [cite: 84] |
| **HU002** | Filtro de búsqueda | [cite_start]Limitar los resultados a videos del estado de **Oaxaca, Valles Centrales**[cite: 87]. | [cite_start]Cliente [cite: 87] | [cite_start]Alto [cite: 87] |
| **HU003** | Reproducción de video | [cite_start]Reproducir los videos encontrados mediante un **enlace directo o reproductor integrado**[cite: 90]. | [cite_start]Cliente [cite: 90] | [cite_start]Alto [cite: 90] |
| **HU004** | Parámetros en la API | [cite_start]Enviar parámetros como término de búsqueda, ubicación y radio para **personalizar** los resultados[cite: 93]. | [cite_start]Desarrollador [cite: 93] | [cite_start]Alto [cite: 93] |
| **HU008** | Registro de usuario | [cite_start]Registrarse en la plataforma con correo y contraseña para un acceso **personalizado**[cite: 105]. | [cite_start]Cliente [cite: 105] | [cite_start]Alto [cite: 105] |
| **HU012** | Inicio de sesión con Google | [cite_start]Iniciar sesión con una cuenta de Google (**OAuth**) para un acceso más rápido[cite: 117]. | [cite_start]Cliente [cite: 117] | [cite_start]Alto [cite: 117] |

### Plan de Trabajo (Sprints)

| Sprint | Actividades Principales | Fecha de Finalización | Duración (Días) | Estado |
| :--- | :--- | :--- | :--- | :--- |
| **Sprint 1** | [cite_start]Elaboración de requerimientos, historias de usuario y diseño UX/UI[cite: 120]. | [cite_start]30/09/2025 [cite: 120] | [cite_start]10 [cite: 120] | [cite_start]En Proceso [cite: 120] |
| **Sprint 2** | [cite_start]Desarrollo de módulo de **inicio de sesión**, API de autenticación e implementación del modelo de base de datos[cite: 120]. | [cite_start]16/10/2025 [cite: 120] | [cite_start]15 [cite: 120] | [cite_start]En Proceso [cite: 120] |
| **Sprint 3** | [cite_start]**Integración y consumo de la API de YouTube** y pruebas de reproducción[cite: 120]. | [cite_start]30/10/2025 [cite: 120] | [cite_start]13 [cite: 120] | [cite_start]En Proceso [cite: 120] |
| **Sprint 4** | [cite_start]Integración de la **API de geolocalización** e implementación de filtros por código de país y estado[cite: 120]. | [cite_start]12/11/2025 [cite: 120] | [cite_start]12 [cite: 120] | [cite_start]En Proceso [cite: 120] |
| **Sprint 5** | [cite_start]Creación de la **API de búsqueda principal**, integración de todas las funcionalidades, pruebas finales y documentación[cite: 120]. | [cite_start]05/12/2025 [cite: 120] | [cite_start]22 [cite: 120] | [cite_start]En Proceso [cite: 120] |

---

## 🛠️ Viabilidad y Limitaciones

### Viabilidad Técnica
[cite_start]Es viable[cite: 48]. [cite_start]Se utilizarán la **API de YouTube Data** (bien documentada y robusta) y la **API de geolocalización de Google** (como Google Geolocation API) para crear el filtro de búsqueda geolocalizado[cite: 48, 49, 50, 51].

### Limitaciones del Proyecto
* [cite_start]**Dependencia de API de terceros:** El proyecto depende directamente de la API de Datos de YouTube, y cualquier cambio en sus términos o cuotas la afectará[cite: 57].
* [cite_start]**Limitación técnica:** La arquitectura se limita al **entorno Web**[cite: 58].
* [cite_start]**Funcionalidades excluidas:** La API se limita estrictamente a la **búsqueda y reproducción** de videos[cite: 59]. [cite_start]No incluirá carga de videos, gestión de comentarios, suscripciones, ni listas de reproducción[cite: 60].
* [cite_start]**Limitaciones de cuota:** El uso estará restringido por la cuota de consultas diarias de Google, por lo que un uso a gran escala podría requerir un plan de pago[cite: 61, 62].

---

## 👥 Equipo del Proyecto
| Rol | Docente | Estudiantes |
| :--- | :--- | :--- |
| **Docente** | [cite_start]Espinosa Pérez Jacob [cite: 7] | - |
| **Estudiantes** | - | [cite_start]Romero Flores Brian Michelle [cite: 9] |
| | - | [cite_start]Pacheco Solorzano Mauricio [cite: 10] |
| | - | [cite_start]Hernández Ruiz Kevin Eduardo [cite: 11] |
| | - | [cite_start]Sosa Perera Carlos Alberto [cite: 12] |

[cite_start]*Documento original: Levantamiento de requerimientos de software para plataforma de búsqueda de videos de YouTube con geolocalización[cite: 6].*
