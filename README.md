📹 Levantamiento de Requerimientos de Software para Plataforma de Búsqueda de Videos de YouTube con Geolocalización
Tecnológico Nacional de México
Instituto Tecnológico de Oaxaca
Ingeniería en Sistemas Computacionales

Materia: Integración De Procesos De Desarrollo De Software
Grupo: 9SA
Actividad: Anteproyecto de software para plataforma de búsqueda de videos de YouTube con geolocalización

Docente: Espinosa Pérez Jacob

Estudiantes:

Romero Flores Brian Michelle - 21160775

Pacheco Solorzano Mauricio – 21160745

Hernández Ruiz Kevin Eduardo – 21160665

Sosa Perera Carlos Alberto – 21160801

Fecha: 22 de septiembre de 2025

📄 Introducción
Este documento presenta el proyecto para el desarrollo de una API Web de búsqueda y reproducción de videos de YouTube con filtros geográficos específicos para México, en el estado de Oaxaca de la región de Valles Centrales.

El objetivo principal es ofrecer una solución que permita a los desarrolladores y usuarios del estado de Oaxaca ubicados en la región de Valles Centrales encontrar contenido relevante y localizado sobre su folclor.

La API utilizará la geolocalización del usuario, el código de estado y la región de Valles Centrales para asegurar que los resultados de búsqueda se adapten a la ubicación específica del usuario, buscando videos con alta relevancia en el área determinada en un radio de 10 kilómetros. Se centrará en la búsqueda y la reproducción de contenido específico.

1. Planteamiento del Problema
Los usuarios de YouTube ubicados en los Valles Centrales, Oaxaca, tienen dificultad para encontrar contenido relevante sobre su localidad. Cuando buscan contenido específico (restaurantes, eventos municipales, talentos locales), el algoritmo de YouTube a menudo presenta resultados globales, populares o genéricos que no se ajustan a su ubicación.

Esto obliga a los usuarios a navegar manualmente a través de miles de videos irrelevantes, lo que consume mucho tiempo. Esta limitación afecta la experiencia del usuario promedio y crea una barrera para el talento local y los pequeños negocios, impidiendo su visibilidad y difusión de información.

2. Justificación
2.1 Análisis de Viabilidad
2.1.1 Viabilidad Técnica
Existe una API de YouTube bien documentada y robusta. Se puede integrar esta API con API de geolocalización (como Google Geolocation API) para crear un filtro de búsqueda que muestre videos geolocalizados en un área específica, cumpliendo el requerimiento de filtrado por coordenadas y región.

2.1.2 Viabilidad Operativa
La API no requerirá cambios significativos en el comportamiento de los usuarios finales, ya que está diseñada para ser una herramienta para desarrolladores que mejora una experiencia de búsqueda ya conocida. Una vez en funcionamiento, requerirá un mantenimiento mínimo enfocado en asegurar la correcta integración con la API de YouTube.

2.2 Limitaciones del Proyecto
Dependencia de API de terceros: El proyecto depende de la API de Datos de YouTube; cualquier cambio en sus términos, cuotas o funcionalidades afectará la API desarrollada.

Limitación técnica: La arquitectura del proyecto se limitará al entorno Web.

Funcionalidades excluidas: La API se limitará estrictamente a la búsqueda y reproducción de videos. No se incluirán funcionalidades como la carga de videos, la gestión de comentarios, las suscripciones o la creación de listas de reproducción.

Limitaciones de cuota: El uso de la API estará restringido por la cuota de consultas diarias establecidas por Google, lo que podría requerir un plan de pago para uso a gran escala.

3. Requerimientos
3.1 Requerimientos Funcionales (RF)
ID

Requerimiento

Descripción

Prioridad

RF1

Búsqueda de videos por ubicación

La API debe permitir buscar videos de YouTube filtrando por coordenadas de latitud y longitud, con un radio de búsqueda de 10 km, para mostrar contenido relevante de los Valles Centrales, Oaxaca.

Alta

RF2

Filtro por país

La API debe limitar los resultados de búsqueda a videos relevantes únicamente para el estado de Oaxaca en los Valles Centrales, utilizando el código del estado y la región.

Alta

RF3

Reproducción de video

La API debe proporcionar los videos encontrados en un formato que permita su reproducción a través de una URL o un reproductor multimedia.

Alta

RF4

Manejo de parámetros

La API debe aceptar y procesar parámetros de entrada, como el término de búsqueda, la ubicación (coordenadas) y el radio de búsqueda de 10 km.

Alta

3.2 Requerimientos No Funcionales (RNF)
ID

Requerimiento

Descripción

Prioridad

RNF1

Documentación clara

La API debe contar con una documentación clara y comprensible para facilitar su integración por parte de los desarrolladores.

Alta

RNF2

Respuestas estándar

La API debe devolver los resultados de búsqueda en un formato JSON estructurado y consistente.

Alta

RNF3

Escalabilidad

La API debe estar diseñada para manejar un gran volumen de solicitudes sin comprometer su rendimiento.

Media

RNF4

Arquitectura Web

La API debe estar orientada exclusivamente a plataformas web.

Alta

RNF5

Autenticación segura

La API debe implementar medidas de seguridad para proteger las claves de la API de Google y garantizar que las peticiones sean seguras.

Alta

RNF6

Protección de datos

La API no debe almacenar información personal de los usuarios para cumplir con las normativas de privacidad.

Alta

4. Enfoque Metodológico
Para la gestión y el desarrollo del proyecto, se adoptará la metodología ágil Scrum.

4.1. Product Backlog
4.1.1 Historias de Usuario
Número

Nombre de la historia de usuario

Descripción

Prioridad

001

Búsqueda de videos por ubicación

Como usuario, quiero buscar videos de YouTube filtrando por ubicación para obtener contenido relevante cercano a mi ubicación actual.

Alto

002

Filtro de búsqueda

Como usuario, quiero limitar los resultados a videos del estado de Oaxaca, Valles Centrales, para visualizar solo información cultural y relevante.

Alto

003

Reproducción de video

Como usuario, quiero reproducir los videos encontrados mediante un enlace directo o un reproductor integrado.

Alto

004

Parámetros en la API

Como desarrollador, quiero enviar parámetros (término de búsqueda, ubicación, radio) para personalizar y controlar los resultados.

Alto

005

Filtros de búsqueda adicionales

Como usuario, quiero aplicar filtros adicionales (fecha de publicación, relevancia o número de vistas) para encontrar videos que se ajusten mejor a mis necesidades.

Alto

006

Información del video

Como usuario, quiero visualizar información básica del video (título, canal, número de vistas, fecha de publicación) junto con el resultado de búsqueda.

Alto

007

Compartir video

Como usuario, quiero compartir los videos encontrados en redes sociales o por enlace directo.

Medio

008

Registro de usuario

Como usuario, quiero registrarme en la plataforma usando mi correo electrónico y contraseña, para poder acceder de forma personalizada.

Alto

009

Inicio de sesión

Como usuario, quiero iniciar sesión con mis credenciales registradas, para poder acceder a mis búsquedas recientes y configuraciones.

Alto

010

Recuperar contraseña

Como usuario, quiero poder recuperar mi contraseña en caso de olvidarla.

Alto

011

Guardar favoritos

Como usuario, quiero que mis videos favoritos se guarden en mi perfil, para recuperarlos en cualquier dispositivo donde inicie sesión.

Medio

012

Inicio de sesión con Google

Como usuario, quiero iniciar sesión con una cuenta de Google, para acceder más rápido sin necesidad de registro manual.

Alto

4.1.2 Plan de Trabajo
Sprint

Actividades

Responsables

Fecha de Inicio

Fecha de Finalización

Duración (Días)

Estado

Sprint 1

Elaboración de requerimientos funcionales y no funcionales. Creación de historias de usuario. Diseño de diagramas UML, E-R y relacional. Diseño UX-UI. Inicio de la bitácora.

Mauricio, Kevin, Carlos, Brian.

20/09/2025

30/09/2025

10

En Proceso.

Sprint 2

Desarrollo del módulo de inicio de sesión. Creación de API para autenticación. Implementación de interfaz de inicio de sesión. Implementación del modelo de base de datos.

Mauricio, Kevin, Carlos, Brian.

01/10/2025

16/10/2025

15

En Proceso.

Sprint 3

Integración y consumo de la API de YouTube. Pruebas de reproducción de videos.

Mauricio, Kevin, Carlos, Brian.

17/10/2025

30/10/2025

13

En Proceso.

Sprint 4

Integración de la API de geolocalización. Implementación de filtros por código de país y estado.

Mauricio, Kevin, Carlos, Brian.

31/10/2025

12/11/2025

12

En Proceso

Sprint 5

Creación de la API de búsqueda principal. Integración de todas las funcionalidades. Pruebas finales y documentación.

Mauricio, Kevin, Carlos, Brian.

13/11/2025

05/12/2025

22

En Proceso

5. Bibliografía
León Pérez Virgen, H., Alberto Salamando Mejía, C., & Stella Valencia Ayala, L. (n.d.). Levantamiento de requerimientos basados en el conocimiento del proceso 1 Requirements gathering based on knowledge of the process Elevação requisitos de conhecimento do processo com base.
