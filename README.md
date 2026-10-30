# MedLink

**Plataforma web para centralizar, organizar y estructurar información médica personal.**

MedLink es un proyecto de la asignatura Capstone de Ingeniería en Informática, sede San Joaquín. Su objetivo es reunir documentos de salud en un solo lugar y convertir su información relevante en una historia personal de salud ordenada y trazable, con mecanismos para compartir antecedentes de manera selectiva.

Este repositorio reúne la documentación, las evidencias grupales e individuales y los diseños del proyecto, organizados por fase.

## El problema que buscamos resolver

Los antecedentes médicos de una persona suelen estar distribuidos entre distintos centros de salud, correos electrónicos, archivos PDF, fotografías, recetas y exámenes. Esa fragmentación dificulta encontrar información cuando se necesita, mantener un registro actualizado y compartir antecedentes con distintos profesionales.

MedLink propone que cada usuario pueda administrar sus documentos, consultar su historial y controlar qué información comparte y con quién.

## Objetivo y funcionalidades previstas

Desarrollar una plataforma web que permita gestionar documentos y antecedentes de salud, conservando la relación entre cada dato registrado y su documento de origen.

El producto mínimo viable (MVP) contempla:

- **Gestión de usuarios:** registro, inicio de sesión y acceso a la información personal.
- **Gestión documental:** carga, clasificación y consulta de exámenes, recetas e informes médicos.
- **Extracción de información:** procesamiento de un conjunto acotado de documentos para obtener datos estructurados, con revisión y corrección del usuario antes de confirmarlos.
- **Historia personal de salud:** visualización cronológica de antecedentes y acceso al documento que los respalda.
- **Intercambio selectivo:** acceso de solo lectura a documentos seleccionados para otra cuenta autenticada, con vencimiento y posibilidad de revocación.
- **Seguridad y trazabilidad:** autorización por recurso, almacenamiento privado de archivos y registro de acciones relevantes.

El diseño inicial considera una historia de salud por titular de cuenta. La herramienta de extracción u OCR está pendiente de selección; sus resultados requieren revisión humana y no constituyen un diagnóstico médico.

## Estado del proyecto

Según el avance documentado de la fase 2, MedLink se encuentra en la etapa de diseño. Se cuenta con la definición del proyecto, los roles del equipo, el stack tecnológico, mockups y propuestas iniciales de arquitectura y modelo de datos.

El backend, el frontend y las pruebas figuran como actividades no iniciadas en ese avance. El repositorio contiene evidencias y diseños; todavía no incluye una aplicación ejecutable ni instrucciones de instalación.

## Fases del proyecto

### Fase 1 · Definición del proyecto APT

**Estado documentado: completada.**

En esta fase se definieron el problema, la relevancia de la solución, los objetivos y el alcance inicial de MedLink. También se relacionó el proyecto con las competencias del perfil de egreso, se evaluó su factibilidad y se establecieron la metodología, los roles y el plan de trabajo.

Las evidencias disponibles incluyen:

- [Guía de definición del proyecto](FASE_1/Evidencias%20Grupales/1.5_GuiaEstudiante_Fase%201_Definicion%20Proyecto%20APT_MEDLINK.docx).
- [Presentación de fase 1](FASE_1/Evidencias%20Grupales/MEDLINK_Fase1.pptx).
- [Pauta de evaluación formativa](FASE_1/Evidencias%20Grupales/1.4_APT122_FormativaFase1.docx).
- [Evidencias individuales](FASE_1/Evidencias%20Individuales/): autoevaluación de competencias, diarios de reflexión y autoevaluación de la fase.

### Fase 2 · Desarrollo del proyecto APT

**Estado documentado: en curso, con avances de diseño.**

Esta fase transforma los requerimientos en diseños que servirán de base para implementar la plataforma. Los mockups se rehicieron y se entregaron como evidencia de esta etapa. Se documentaron la arquitectura inicial, las responsabilidades de los componentes y las entidades y relaciones del modelo de datos.

También se reajustó el cronograma original de 18 semanas para finalizar en la semana 16. Se mantienen los objetivos y la metodología; el ajuste reduce el tiempo de diseño y cierre, y contempla desarrollo y pruebas en paralelo.

Las evidencias disponibles incluyen:

- [Guía de desarrollo y monitoreo del proyecto](Fase_2/Evidencias_Grupales/2.4_GuiaEstudiante_Fase%202_DesarrolloProyecto%20APT.docx).
- [Presentación de avance de fase 2](Fase_2/Evidencias_Proyecto/MEDLINK%20_Fase%202%20_1.pptx).
- [Mockups de la plataforma](Fase_2/Evidencias_Proyecto/MOCKUPS/).
- [Arquitectura inicial de MedLink](Fase_2/Evidencias_Proyecto/ARQUITECTURA/Arquitectura_inicial_MEDLINK.md).
- [Modelo inicial de datos](Fase_2/Evidencias_Proyecto/MODELO_DATOS/Modelo_datos_inicial_MEDLINK.md).
- [Evidencias individuales](Fase_2/Evidencias_Individuales/): diarios de reflexión de los integrantes.

### Próximas entregas y cierre

El plan contempla implementar e integrar el MVP, validar sus funcionalidades y controles de acceso, y preparar la documentación y demostración final. Los entregables previstos son el prototipo funcional, los resultados de pruebas, la documentación técnica, el manual de uso y la presentación del sistema.

Actualmente no hay una carpeta de fase 3 ni evidencias de cierre en el repositorio. Estos entregables permanecen como trabajo planificado.

## Plan de trabajo actualizado

La planificación registrada en la fase 2 establece el cierre en la **semana 16**. Las semanas corresponden al período académico del proyecto.

| Actividad | Período planificado | Responsables |
| --- | --- | --- |
| Backend y extracción de información | Semanas 8 a 13 | Nicolás Yáñez y Felipe Chavarría |
| Frontend e interfaz web | Semanas 9 a 14 | Nicolás Yáñez y Camilo Pérez |
| Pruebas, validación y seguridad | Semanas 11 a 15 | Equipo completo |
| Documentación y cierre | Semanas 15 a 16 | Equipo completo |

La documentación se elabora durante el proyecto; las dos últimas semanas se destinan a consolidar las entregas y el cierre. El detalle de los ajustes está en la guía de desarrollo de fase 2.

## Diseño técnico

El stack seleccionado para la implementación es:

| Capa | Tecnologías previstas |
| --- | --- |
| Frontend | React, TypeScript, Vite y Tailwind CSS |
| Backend y API REST | Python, Django y Django REST Framework |
| Base de datos | PostgreSQL |
| Diseño de interfaces | Figma |

La arquitectura propone un backend como monolito modular, con módulos para documentos, extracción, historial, accesos compartidos y auditoría. PostgreSQL almacenará metadatos e información estructurada; los documentos originales se conservarán en almacenamiento privado y se consultarán mediante la API con control de acceso.

El modelo lógico contempla las entidades **Usuario, Documento, Extracción, Antecedente, Acceso compartido, Documento compartido y Auditoría**. Los diagramas y las reglas se encuentran en los documentos de arquitectura y modelo de datos enlazados en la fase 2. Son propuestas de diseño, no componentes ya implementados.

## Metodología de trabajo

Se utiliza desarrollo incremental guiado por especificaciones. Antes de implementar cada funcionalidad se definen sus requerimientos, criterios de aceptación, diseño técnico y tareas. Luego se desarrolla, integra, prueba y documenta el incremento.

El equipo realiza seguimiento del avance y revisa las decisiones relevantes de forma conjunta. Para el desarrollo y las validaciones se prevé utilizar datos de prueba simulados o anonimizados.

## Estructura del repositorio

```text
.
├── README.md
├── FASE_1/
│   ├── Evidencias Grupales/        # Definición, pauta y presentación
│   └── Evidencias Individuales/    # Autoevaluaciones y reflexiones
└── Fase_2/
    ├── Evidencias_Grupales/        # Informe de avance y monitoreo
    ├── Evidencias_Individuales/    # Diarios de reflexión
    └── Evidencias_Proyecto/
        ├── ARQUITECTURA/           # Diseño inicial de componentes
        ├── MODELO_DATOS/           # Entidades, relaciones y reglas
        ├── MOCKUPS/                # Capturas de las interfaces propuestas
        └── MEDLINK _Fase 2 _1.pptx
```

## Equipo

| Integrante | Áreas de trabajo previstas |
| --- | --- |
| Nicolás Yáñez | Arquitectura, datos, backend, frontend e integración |
| Felipe Chavarría | Arquitectura, modelo de datos y backend |
| Camilo Pérez | Frontend e integración |

El levantamiento de requerimientos, las pruebas, la seguridad y la documentación son responsabilidades compartidas por el equipo.
