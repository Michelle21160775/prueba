# 🚀 Anteproyecto de Software: Plataforma de Búsqueda de Videos de YouTube con Geolocalización

## Información del Proyecto
| Detalle | Valor |
| :--- | :--- |
| **Institución** | [cite_start]Tecnológico Nacional de México, Instituto Tecnológico de Oaxaca [cite: 1, 2] |
| **Materia** | [cite_start]Integración De Procesos De Desarrollo De Software [cite: 4] |
| **Grupo** | [cite_start]9SA [cite: 5] |
| **Actividad** | [cite_start]Anteproyecto de software para plataforma de búsqueda de videos de YouTube con geolocalización [cite: 6] |
| **Docente** | [cite_start]Espinosa Pérez Jacob [cite: 7] |
| **Fecha** | [cite_start]22 de septiembre de 2025 [cite: 13] |

### Estudiantes
* [cite_start]Romero Flores Brian Michelle - 21160775 [cite: 9]
* [cite_start]Pacheco Solorzano Mauricio – 21160745 [cite: 10]
* [cite_start]Hernández Ruiz Kevin Eduardo – 21160665 [cite: 11]
* [cite_start]Sosa Perera Carlos Alberto – 21160801 [cite: 12]

---

## 💡 Introducción
[cite_start]Este documento presenta el proyecto para el desarrollo de una **API Web** de búsqueda y reproducción de videos de YouTube con filtros geográficos específicos para México, en el estado de Oaxaca, región de Valles Centrales[cite: 31].

[cite_start]El objetivo principal es ofrecer una solución que permita a desarrolladores y usuarios de Valles Centrales encontrar **contenido relevante y localizado** sobre su folclor[cite: 32]. [cite_start]La API utilizará la geolocalización del usuario, el código del estado y la región para asegurar que los resultados de búsqueda se adapten a la ubicación específica, buscando videos con alta relevancia en un radio de **10 kilómetros**[cite: 33].

## ❌ 1. Planteamiento del Problema
[cite_start]Los usuarios de YouTube en los Valles Centrales, Oaxaca, tienen dificultad para encontrar contenido relevante sobre su localidad[cite: 37]. [cite_start]El algoritmo de YouTube a menudo presenta resultados globales, populares o genéricos que no se ajustan a su ubicación[cite: 38]. [cite_start]Esto obliga a los usuarios a navegar manualmente a través de miles de videos irrelevantes[cite: 39].

[cite_start]Esta limitación afecta la experiencia del usuario y crea una barrera para el talento local y los pequeños negocios, cuyo contenido queda opacado por el volumen masivo de videos globales[cite: 40, 42].

## ✅ 2. Justificación

### 2.1 Análisis de Viabilidad

#### Viabilidad Técnica
[cite_start]Existe la API de YouTube Data, que es robusta y está bien documentada, y se puede integrar con una API de geolocalización (como Google Geolocation API) para crear el filtro de búsqueda por área específica[cite: 48, 49, 50, 51].

#### Viabilidad Operativa
[cite_start]La API no requerirá cambios significativos para el usuario final, ya que serán los desarrolladores quienes la implementarán para mejorar la experiencia de búsqueda que ya conocen[cite: 53, 54]. [cite_start]Requerirá mantenimiento mínimo, principalmente para asegurar la correcta integración con la API de YouTube[cite: 55].

### 2.2 Limitaciones del Proyecto
* [cite_start]**Dependencia de API de terceros**: El proyecto depende de la API de Datos de YouTube, y cualquier cambio en sus términos, cuotas o funcionalidades la afectará directamente[cite: 57].
* [cite_start]**Limitación técnica**: La arquitectura del proyecto se limitará al **entorno Web**[cite: 58, 74].
* **Funcionalidades excluidas**: Se limitará estrictamente a la **búsqueda y reproducción de videos**. [cite_start]No incluirá funciones como carga de videos, gestión de comentarios, suscripciones, creación de listas de reproducción, o historial[cite: 59, 60].
* [cite_start]**Limitaciones de cuota**: El uso estará restringido por la cuota de consultas diarias de Google, requiriendo un plan de pago para uso a gran escala[cite: 61, 62].

---

## 🛠️ 3. Requerimientos

### 3.1 Requerimientos Funcionales (RF)

| ID | Requerimiento | Descripción | Prioridad |
| :--- | :--- | :--- | :--- |
| **RF1** | Búsqueda de videos por ubicación | [cite_start]Permitir buscar videos de YouTube filtrando por coordenadas de latitud y longitud, con un radio de búsqueda de **10 km**, para mostrar contenido relevante de los Valles Centrales, Oaxaca[cite: 65, 69]. | [cite_start]Alta [cite: 69] |
| **RF2** | Filtro por país | [cite_start]Limitar los resultados de búsqueda a videos relevantes únicamente para el estado de Oaxaca en los Valles Centrales, utilizando el código del estado y la región[cite: 66, 69]. | [cite_start]Alta [cite: 69] |
| **RF3** | Reproducción de video | [cite_start]Proporcionar los videos encontrados en un formato que permita su reproducción a través de una URL o un reproductor multimedia[cite: 67, 69]. | [cite_start]Alta [cite: 69] |
| **RF4** | Manejo de parámetros | [cite_start]Aceptar y procesar parámetros de entrada como el término de búsqueda, la ubicación (coordenadas) y el radio de búsqueda de **10 km**[cite: 68, 69]. | [cite_start]Alta [cite: 69] |

### 3.2 Requerimientos No Funcionales (RNF)

| ID | Requerimiento | Descripción | Prioridad |
| :--- | :--- | :--- | :--- |
| **RNF1** | Documentación clara | [cite_start]Contar con una documentación clara y compresible para facilitar su integración por parte de los desarrolladores[cite: 71, 77]. | [cite_start]Alta [cite: 77] |
| **RNF2** | Respuestas estándar | [cite_start]Devolver los resultados de búsqueda en un formato **JSON** estructurado y consistente[cite: 72, 77]. | [cite_start]Alta [cite: 77] |
| **RNF3** | Escalabilidad | [cite_start]Estar diseñada para manejar un gran volumen de solicitudes sin comprometer su rendimiento[cite: 73, 77]. | [cite_start]Media [cite: 77] |
| **RNF4** | Arquitectura Web | [cite_start]Estar orientada exclusivamente a plataformas web[cite: 74, 77]. | [cite_start]Alta [cite: 77] |
| **RNF5** | Autenticación segura | [cite_start]Implementar medidas de seguridad para proteger las claves de la API de Google y garantizar que las peticiones sean seguras[cite: 75, 77]. | [cite_start]Alta [cite: 77] |
| **RNF6** | Protección de datos | [cite_start]No almacenar información personal de los usuarios para cumplir con las normativas de privacidad[cite: 76, 77]. | [cite_start]Alta [cite: 77] |

---

## ⚡ 4. Enfoque Metodológico
[cite_start]Se adoptará la metodología ágil **Scrum** para la gestión y desarrollo del proyecto[cite: 79]. [cite_start]Esta metodología permitirá una rápida adaptación a las necesidades cambiantes, mejor comunicación y entrega de valor continua y eficiente[cite: 80].

### 4.1. Historias de Usuario (Product Backlog)
| ID | Historia de Usuario | Usuario | Prioridad | Riesgo | Descripción | Criterios de Aceptación |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **001** | [cite_start]Búsqueda por ubicación [cite: 84] | [cite_start]Cliente [cite: 84] | [cite_start]Alto [cite: 84] | [cite_start]Alto [cite: 84] | [cite_start]Como usuario, quiero buscar videos de YouTube filtrando por ubicación para obtener contenido relevante cercano a mi ubicación actual[cite: 84]. | Aceptar coordenadas. [cite_start]/ Devolver videos dentro del radio de **10 km**[cite: 84]. [cite_start]/ Resultados ordenados por relevancia y/o fecha de publicación[cite: 84]. |
| **002** | [cite_start]Filtro de búsqueda [cite: 87] | [cite_start]Cliente [cite: 87] | [cite_start]Alto [cite: 87] | [cite_start]Alto [cite: 87] | [cite_start]Como usuario, quiero limitar los resultados de búsqueda a videos del estado de Oaxaca, específicamente de los Valles Centrales, para visualizar solo información cultural y relevante a mi región[cite: 87]. | Aplicar filtro por región/código de estado. / Videos geolocalizados en Valles Centrales. [cite_start]/ Combinable con término de búsqueda[cite: 87]. |
| **003** | [cite_start]Reproducción de video [cite: 90] | [cite_start]Cliente [cite: 90] | [cite_start]Alto [cite: 90] | [cite_start]Alto [cite: 90] | [cite_start]Como usuario, quiero reproducir los videos encontrados mediante un enlace directo o un reproductor integrado para poder ver el contenido sin salir de la plataforma[cite: 90]. | Cada video debe incluir una URL válida. / Ofrecer la opción de reproductor integrado. [cite_start]/ Experiencia de reproducción fluida[cite: 90]. |
| **004** | [cite_start]Parámetros en la API [cite: 93] | [cite_start]Desarrollador [cite: 93] | [cite_start]Alto [cite: 93] | [cite_start]Alto [cite: 93] | [cite_start]Como desarrollador, quiero enviar parámetros como término de búsqueda, ubicación y radio de búsqueda para personalizar y controlar los resultados obtenidos[cite: 93]. | Aceptar al menos tres parámetros: término, lat/lon y radio. / Validar los parámetros. [cite_start]/ Devolver mensaje de error claro si el parámetro es inválido[cite: 93]. |
| **005** | [cite_start]Filtros adicionales [cite: 96] | [cite_start]Cliente [cite: 96] | [cite_start]Alto [cite: 96] | [cite_start]Medio [cite: 96] | [cite_start]Como usuario, quiero aplicar filtros adicionales (fecha de publicación, relevancia o número de vistas) para encontrar videos que se ajusten mejor a mis necesidades[cite: 96]. | Permitir seleccionar al menos un filtro. / Resultados se actualizan en tiempo real. [cite_start]/ Mostrar mensaje si no hay videos que cumplan el criterio[cite: 96]. |
| **006** | [cite_start]Información del video [cite: 99] | [cite_start]Cliente [cite: 99] | [cite_start]Alto [cite: 99] | [cite_start]Medio [cite: 99] | [cite_start]Como usuario, quiero visualizar información básica del video (título, canal, vistas, fecha de publicación) junto al resultado de búsqueda para decidir cuál reproducir[cite: 99]. | Cada resultado debe mostrar título, canal, vistas y fecha. / Información debe coincidir con la oficial de YouTube. [cite_start]/ Manejar datos faltantes (ej: "No disponible")[cite: 99]. |
| **007** | [cite_start]Compartir video [cite: 102] | [cite_start]Cliente [cite: 102] | [cite_start]Medio [cite: 102] | [cite_start]Bajo [cite: 102] | [cite_start]Como usuario, quiero compartir los videos encontrados en redes sociales o por enlace directo, para mostrar a otros el contenido localizado[cite: 102]. | Incluir botón de “Compartir”. / Generar enlace directo al video de YouTube. [cite_start]/ Permitir copiar enlace o enviarlo mediante opciones rápidas (ej. WhatsApp)[cite: 102]. |
| **008** | [cite_start]Registro de usuario [cite: 105] | [cite_start]Cliente [cite: 105] | [cite_start]Alto [cite: 105] | [cite_start]Alto [cite: 105] | [cite_start]Como usuario, quiero registrarme en la plataforma usando mi correo electrónico y contraseña, para poder acceder de forma personalizada al buscador[cite: 105]. | Validar que el correo no esté registrado. / Contraseña debe cumplir requisitos de seguridad. / Redirigir a pantalla principal si es exitoso. [cite_start]/ Mostrar mensaje de error si falla (ej. “Correo ya registrado”)[cite: 105]. |
| **009** | [cite_start]Inicio de sesión [cite: 108] | [cite_start]Cliente [cite: 108] | [cite_start]Alto [cite: 108] | [cite_start]Alto [cite: 108] | [cite_start]Como usuario, quiero iniciar sesión con mis credenciales registradas, para poder acceder a mis búsquedas recientes y configuraciones personalizadas[cite: 108]. | Ingresar correo y contraseña válidos. / Mostrar pantalla principal con perfil cargado si es correcto. [cite_start]/ Mostrar mensaje “Correo o contraseña inválidos” si es incorrecto[cite: 108]. |
| **010** | [cite_start]Recuperar contraseña [cite: 111] | [cite_start]Cliente [cite: 111] | [cite_start]Alto [cite: 111] | [cite_start]Alto [cite: 111] | [cite_start]Como usuario, quiero poder recuperar mi contraseña en caso de olvidarla, para no perder el acceso a la plataforma[cite: 111]. | [cite_start]Permitir al usuario establecer una nueva contraseña y usarla en su próximo inicio de sesión[cite: 111]. |
| **011** | [cite_start]Guardar favoritos [cite: 114] | [cite_start]Cliente [cite: 114] | [cite_start]Medio [cite: 114] | [cite_start]Bajo [cite: 114] | [cite_start]Como usuario, quiero que mis videos favoritos se guarden en mi perfil, para recuperarlos en cualquier dispositivo donde inicie sesión[cite: 114]. | Cargar favoritos del usuario al iniciar sesión. [cite_start]/ Debe existir la opción de borrar un video de favoritos[cite: 114]. |
| **012** | [cite_start]Inicio de sesión con Google [cite: 117] | [cite_start]Cliente [cite: 117] | [cite_start]Alto [cite: 117] | [cite_start]Alto [cite: 117] | [cite_start]Como usuario, quiero iniciar sesión con una cuenta de Google, para acceder más rápido sin necesidad de registro manual[cite: 117]. | Permitir autenticación mediante OAuth de Google. / Si es la primera vez, registrarlo automáticamente. [cite_start]/ Si ya existe, redirigir a su perfil[cite: 117]. |

### 4.2. Plan de Trabajo (Sprints)
> [cite_start]**Nota:** Todos los responsables son: Mauricio, Kevin, Carlos y Brian[cite: 120].

| Sprint | Actividades | Fecha de Inicio | Fecha de Finalización | Duración (Días) | Estado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Sprint 1** | - Elaboración de requerimientos funcionales y no funcionales. / - Creación de historias de usuario. / - Diseño de diagramas UML, E-R y relacional. / - Diseño UX-UI. [cite_start]/ - Inicio de la bitácora[cite: 120]. | [cite_start]20/09/2025 [cite: 120] | [cite_start]30/09/2025 [cite: 120] | [cite_start]10 [cite: 120] | [cite_start]En Proceso [cite: 120] |
| **Sprint 2** | - Desarrollo del módulo de inicio de sesión. / - Creación de API para autenticación. / - Implementación de interfaz de inicio de sesión. [cite_start]/ - Implementación del modelo de base de datos[cite: 120]. | [cite_start]01/10/2025 [cite: 120] | [cite_start]16/10/2025 [cite: 120] | [cite_start]15 [cite: 120] | [cite_start]En Proceso [cite: 120] |
| **Sprint 3** | - Integración y consumo de la API de YouTube. [cite_start]/ - Pruebas de reproducción de videos[cite: 120]. | [cite_start]17/10/2025 [cite: 120] | [cite_start]30/10/2025 [cite: 120] | [cite_start]13 [cite: 120] | [cite_start]En Proceso [cite: 120] |
| **Sprint 4** | - Integración de la API de geolocalización. [cite_start]/ - Implementación de filtros por código de país y estado[cite: 120]. | [cite_start]31/10/2025 [cite: 120] | [cite_start]12/11/2025 [cite: 120] | [cite_start]12 [cite: 120] | [cite_start]En Proceso [cite: 120] |
| **Sprint 5** | - Creación de la API de búsqueda principal. / - Integración de todas las funcionalidades. [cite_start]/ - Pruebas finales y documentación[cite: 120]. | [cite_start]13/11/2025 [cite: 120] | [cite_start]05/12/2025 [cite: 120] | [cite_start]22 [cite: 120] | [cite_start]En Proceso [cite: 120] |

---

## 🎨 Diseño UI/UX
Puedes visualizar el diseño en el siguiente enlace:
[cite_start][Diseños en Figma](https://www.figma.com/proto/PAJOEq0nK6mXi4uzOmQgAa/API_YOUTUBE?node-id=1-3149&t=w0FBCGQir9JpiJrU-1) [cite: 123]

---
