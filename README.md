# TFG: Gestión de Incidencias en el Suministro de Agua 🚰

[![Kotlin](https://img.shields.io/badge/Kotlin-1.8-blue?logo=kotlin)](https://kotlinlang.org/) 
[![Android Studio](https://img.shields.io/badge/Android_Studio-2023-green?logo=androidstudio)](https://developer.android.com/studio) 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Tabla de Contenidos
- [Introducción](#introducción)
- [Descripción del Proyecto](#descripción-del-proyecto)
- [Características](#características)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Video Informativo](#video-informativo)
- [Diagrama de Arquitectura](#diagrama-de-arquitectura)
- [Diagrama Entidad Relación](#diagrama-entidad-relación)
- [Tiempos Invertidos](#tiempos-invertidos)
- [Contacto](#contacto)

## Introducción

¡Bienvenidos a mi proyecto! En este TFG he trabajado para desarrollar una solución que ayude a *mejorar la gestión del agua*. La aplicación permite que los trabajadores encargados de la gestión reporten incidencias en tiempo real, notificando a los vecinos afectados.

## Descripción del Proyecto

En este proyecto, he desarrollado una herramienta que sirva para:

- *Permita reportar incidencias* de forma rápida y precisa.
- *Notifique automáticamente* a los vecinos de la zona afectada.
- *Visualice las averías* mediante un mapa interactivo, facilitando la identificación de la ubicación exacta.



## Características

- *Reporte de Incidencias:*  
  Los trabajadores pueden indicar el punto exacto de la avería en un mapa interactivo.
  
- *Notificaciones Push:*  
  Alertas automáticas para los vecinos que se vean afectados. Indicando las horas en las que dicho corte de agua va a afectarles.  
  
- *Interfaz Amigable:*  
  Diseño intuitivo y moderno que facilita la interacción de los trabajadores.

### Funcionalidades Adicionales:
- 🔒 *Seguridad:* Gestión segura de datos.
- 🌐 *Actualización en Tiempo Real:* Información siempre al día.
- 📊 *Estadísticas:* Visualización de datos históricos y tendencias.

## Tecnologías Utilizadas

- *Kotlin:* Lenguaje principal de desarrollo.
- *Android Studio:* Entorno de desarrollo integrado (IDE).
- *Firebase Cloud Messaging:* Sistema de notificaciones en tiempo real.
- *Google Maps API:* Integración de mapas para la geolocalización.

| Tecnología                | Descripción                                               |
|---------------------------|-----------------------------------------------------------|
| *Kotlin*                | Lenguaje de programación moderno y conciso                |
| *Android Studio*        | IDE robusto para el desarrollo de aplicaciones Android    |
| *Firebase Cloud Messaging* | Envío de notificaciones push en tiempo real             |
| *Google Maps API*       | Servicios de mapas y geolocalización interactiva            |

## Video informativo 

[![video](https://www.aragondigital.es/asset/thumbnail,1280,720,center,center/media/aragondigital/images/2024/11/25/2024112519295538460.jpg)](https://www.youtube.com/watch?v=Wo04LKhya_A)

## Diagrama de Arquitectura
```mermaid
graph TD;
    A[Usuario] --> B[Aplicación Android];
    B --> C[Interfaz de Usuario];
    B --> D["Controlador/Presentador (MVVM)"];
    D --> E[Servicios de Backend];
    E --> F["Firebase Cloud Messaging<br>(Notificaciones Push)"];
    E --> G["Base de Datos<br>(Firebase Firestore o Realtime Database)"];
    D --> H["Google Maps API<br>(Geolocalización y Mapeo)"];
```

## Diagrama Entidad Relación
```mermaid
erDiagram
    TRABAJADOR {
      int id
      string name
      string email
    }
    INCIDENTE {
      int id
      string descripcion
      datetime reportadoAt
    }
    VECINO {
      int id
      string nombre
      string direccion
    }
    NOTIFICACION {
      int id
      datetime enviadoAt
    }
    
    TRABAJADOR ||--o{ INCIDENTE : reports
    INCIDENTE ||--|{ NOTIFICACION : triggers
    VECINO ||--o{ NOTIFICACION : receives
```

## Tiempos invertidos
```mermaid
gantt
  title Tiempo Invertido en el Proyecto
  dateFormat  YYYY-MM-DD
  section Fases del Proyecto
  Investigación       :done,    inv, 2025-01-01, 15d
  Diseño              :done,    des, 2025-01-16, 20d
  Desarrollo          :active,  dev, 2025-02-05, 40d
  Pruebas             :active,  test,2025-03-17, 15d
  Documentación       :         doc, 2025-04-01, 10d

```

## Contacto  

Si tienes alguna pregunta, sugerencia o quieres contribuir al proyecto, puedes contactarme a través de:  

📧 **Email:** [serranolampre@gmail.com](mailto:serranolampre@gmail.com)  
🔗 **LinkedIn:** [Julia Serrano Lampre](https://www.linkedin.com/in/juliaserranolampre/)  
🐙 **GitHub:** [Selampr](https://github.com/selampr)  









