---
title: "G-A-GTI-01 V8 — Guía de Diligenciamiento"
source_file: "Guia_Diligenciamiento_SI_V8_Definitiva.docx"
conversion: semantic-markdown
note: "Texto y tablas conservados; imágenes decorativas, formato visual y espacios vacíos omitidos para reducir tokens."
---

## GUÍA DE DILIGENCIAMIENTO

Ficha de Caracterización de un Sistema de Información

| Código | G-A-GTI-01 · V8 | Versión | 8 |
| --- | --- | --- | --- |
| Vigencia | 01/07/2026 | Proceso | Gestión de Servicios de Información y Soporte Tecnológico |

| NOTA — Sobre esta guía — Esta guía orienta el diligenciamiento de la Ficha de Caracterización de Soluciones Tecnológicas (F-A-GTI-01) y su consolidación en el Catálogo Institucional de Soluciones Tecnológicas (F-A-GTI-02). Está alineada con los lineamientos MGGTI.LI.SI.02, .08, .09, .10, .12, MAE.LI.ASI.01-03 del Marco de Gestión y Gobierno de TI — MinTIC 2023, y con el procedimiento P-A-GTI-03 V5 «Desarrollar y mantener sistemas de información y componentes». |
| --- |

| NOTA — Novedades de la versión 8 — Se incorpora la Sección 9 (Seguridad, continuidad e insumos para el Plan de Mantenimiento), alineada con el Catálogo F-A-GTI-02 V4. Se actualiza la matriz de secciones condicionales (3.3), se amplía el glosario (Sección 10.16 a 10.23) y el checklist de calidad (Sección 11). Se recuperan tres campos que existían en el vocabulario pero no en la Ficha: Dependencia ejecutora, Número de registro RNBD y Monitoreo activo. |
| --- |

# ANTES DE EMPEZAR

| NOTA — Esta sección es la puerta de entrada. Léala primero. Le dirá exactamente qué preparar, a quién convocar y por qué sección de la guía continuar. |
| --- |

| Paso | Qué hacer — responsable |
| --- | --- |
| 1 | Identifique la solución. Tenga a mano el nombre oficial, la sigla y el nombre del proceso de negocio que soporta. Responsable: Líder Funcional. |
| 2 | Clasifique la Naturaleza (N1-N8) leyendo la Sección 3.1 y el árbol de decisión. Esta elección define qué secciones de la Ficha debe diligenciar. |
| 3 | Convoque los 4 roles necesarios (Sección 4.2). Duración estimada de sesión: 90 minutos. |
| 4 | Solicite datos de costos al Área de Contratos usando el Formato de Solicitud TCO (Sección 7.3). Envíe con mínimo 3 días hábiles de antelación. |
| 5 | Diligencie la Ficha sección por sección siguiendo la Sección 5, incluida la nueva Sección 9. Al finalizar, transcriba los datos al Catálogo F-A-GTI-02. |

# 1. PROPÓSITO, ALCANCE Y BASE NORMATIVA

## 1.1 Propósito

Esta guía orienta paso a paso el diligenciamiento de la Ficha de Caracterización de Soluciones Tecnológicas, define el vocabulario controlado y la taxonomía aplicable, establece los criterios de calidad de los datos, y describe el flujo de trabajo que vincula la Ficha con el Catálogo Institucional de Soluciones Tecnológicas y con el procedimiento P-A-GTI-03 "Desarrollar y mantener sistemas de información y componentes".

Está dirigida a quienes participan en las sesiones de levantamiento del catálogo: líderes técnicos de TI, responsables funcionales de las áreas usuarias, profesionales de la OTIC que consolidan la información, y a las áreas financiera y de contratos que aportan los datos de costos y de soporte.

## 1.2 Alcance

La guía aplica a todas las soluciones tecnológicas del Ministerio independientemente de su naturaleza: sistemas de información, aplicaciones, componentes técnicos, integraciones, plataformas, servicios tecnológicos, soluciones analíticas y herramientas transversales. No aplica a equipos físicos, dispositivos de usuario final ni infraestructura de red, los cuales se inventarían por instrumentos distintos.

## 1.3 Base normativa y lineamientos

La Ficha y el Catálogo dan cumplimiento a los siguientes lineamientos del Marco de Gestión y Gobierno de TI (MinTIC, 2023) y del Modelo de Referencia de Arquitectura Empresarial:

| Lineamiento | Descripción | Qué obliga |
| --- | --- | --- |
| MGGTI.LI.SI.02 | Catálogo de Sistemas de Información | Construir y gestionar el catálogo con la caracterización de cada solución. |
| MGGTI.LI.SI.08 | Manual del usuario, técnico y de operación | Todas las soluciones deben tener documentación técnica y funcional actualizada. |
| MGGTI.LI.SI.09 | Plan de mantenimiento | Elaborar plan de mantenimiento anual, cuyo insumo es el catálogo (ver nueva Sección 9). |
| MGGTI.LI.SI.10 | Servicios de mantenimiento con terceros | Definir ANS cuando el soporte esté contratado con terceros. |
| MGGTI.LI.SI.12 | Atributos de calidad / requerimientos no funcionales | Identificar y verificar atributos de calidad asociados a la solución. |
| MAE.LI.ASI.01 | Arquitecturas de referencia | La Ficha debe ubicar la solución en la(s) zona(s) de la arquitectura de referencia. |
| MAE.LI.ASI.02 | Arquitecturas de solución | Mantener documentada la arquitectura de cada solución integrada al ecosistema. |
| MAE.LI.ASI.03 | Caracterización de los Sistemas de Información | Necesaria para modelar vistas en relación con SI, procesos e infraestructura. |
| MSPI (MinTIC) | Modelo de Seguridad y Privacidad de la Información | Valorar el riesgo de seguridad de cada solución. Base normativa de la nueva Sección 9. |
| NTC 5854 / WCAG | Accesibilidad web | Verificar accesibilidad en soluciones de cara al ciudadano. Base normativa de la nueva Sección 9. |

Marco legal complementario aplicable al diligenciamiento:

- Ley 1712 de 2014 — Clasificación de la información pública.
- Ley 1581 de 2012 y Decreto 1074 de 2015 — Protección de datos personales y registro en el RNBD ante la SIC.
- Ley 594 de 2000 — Gestión documental y conservación de información de valor archivístico (relevante para retiros).
- Decreto 767 de 2022 — Política de Gobierno Digital.
# 2. INSTRUMENTOS Y CÓMO SE RELACIONAN

La caracterización de soluciones tecnológicas en el Ministerio se opera con tres instrumentos articulados:

| Instrumento | Función |
| --- | --- |
| F-A-GTI-01 · Ficha de Caracterización | Formulario de captura por solución. Documento Word diligenciado en sesiones con responsable técnico y funcional. Es el registro oficial de cada solución y es firmado por los responsables. Una ficha por solución. |
| F-A-GTI-02 · Catálogo Institucional | Hoja de cálculo que consolida la información de todas las fichas. Es la vista de portafolio de la OTIC y la fuente de los tableros de gestión, alertas de caducidad, avance por dependencia y el futuro plan de mantenimiento. |
| G-A-GTI-01 · Esta guía | Manual de referencia que explica cada campo, define el vocabulario controlado, y establece la trazabilidad Ficha ↔ Catálogo. |

## 2.1 Articulación con el procedimiento de desarrollo

La Ficha no vive aislada del ciclo de desarrollo. El procedimiento P-A-GTI-03 "Desarrollar y mantener sistemas de información y componentes" incluye en su actividad 9 de la fase "Desplegar en Producción" la actualización del catálogo, momento en el cual la Ficha se diligencia por primera vez en estado completo y se realizan la primera clasificación TIME y el primer cálculo de TCO.

| Fase del P-A-GTI-03 | Acción sobre la Ficha / Catálogo |
| --- | --- |
| Analizar y levantar requerimientos | Crear Ficha en estado «En Levantamiento». Diligenciar Secciones 1, 4 y 5. |
| Definir arquitectura de software | Diligenciar Sección 2 y registrar enlaces a artefactos de arquitectura en la wiki. |
| Desplegar en producción — Act. 9 | Actualizar Ficha a estado «Completa». Primera clasificación TIME, primer TCO y primera valoración de seguridad (Sección 9). Cargar consolidado al Catálogo. |
| Mantenimiento (anual) | Revisión anual de Ficha. Actualizar TCO, incidentes, vencimientos, seguridad. Reclasificar TIME si aplica. |
| Eventos disparadores | Reclasificación fuera de ciclo por vencimiento de soporte, cambio normativo, incidente grave, cambio de responsables (ver Sección 4.3). |

# 3. TAXONOMÍA DE SOLUCIONES TECNOLÓGICAS

## 3.1 Árbol de decisión N1 vs N2 — las más confundidas

| Criterio de decisión | Interpretación y resultado |
| --- | --- |
| P1: ¿La solución gestiona datos de negocio del Ministerio de forma persistente (base de datos propia)? | Si SÍ, avance a P2. Si NO, probablemente es N2 o N3. |
| P2: ¿La solución soporta uno o varios procesos institucionales completos (trámites, contratos, PQRSD, nómina)? | Si SÍ → es N1 (Sistema de información). Ejemplo: SIGTRAM gestiona el proceso completo de trámites ambientales. |
| P3: ¿La solución resuelve una tarea puntual o es un canal de interacción sin procesar el negocio internamente? | Si SÍ → es N2 (Aplicación). Ejemplo: app web de radicación → N2; el proceso lo gestiona el sistema detrás. |
| Todavía tiene dudas | Consulte la columna "Cuándo usarla" de la tabla N1-N8, o comuníquese con el Coordinador TI antes de la sesión. |

La caracterización adopta una taxonomía de dos niveles. El primer nivel (Naturaleza) determina qué secciones de la Ficha son obligatorias para esa solución. El segundo nivel (Tipo detallado) precisa la categoría específica dentro de la naturaleza.

| NOTA — Cómo usar la taxonomía — Al iniciar el diligenciamiento, escoja primero la Naturaleza (8 valores). Esa elección activa las secciones aplicables de la Ficha y desactiva las que no apliquen. Luego escoja el Tipo detallado (45 valores) de la lista filtrada según la Naturaleza. |
| --- |

## 3.2 Nivel 1 — Naturaleza de la solución

| ID | Naturaleza | Definición operativa | Cuándo usarla | Ejemplos |
| --- | --- | --- | --- | --- |
| N1 | Sistema de información | Solución que soporta uno o varios procesos institucionales, gestiona datos del negocio y puede estar compuesta por módulos, reglas, usuarios, integraciones y persistencia. | Alcance funcional completo que soporta un proceso institucional. | REAA, sistema de PQRSD, sistema de nómina. |
| N2 | Aplicación | Software con funcionalidad acotada, orientada a una tarea, canal o necesidad específica. | Resuelve necesidad puntual sin constituir un sistema institucional completo. | App web de radicación, app móvil de reporte. |
| N3 | Componente | Elemento técnico o funcional que hace parte de una solución mayor y puede tener ciclo de vida propio. | Microservicios, motores, módulos o componentes reutilizables gestionables. | Microservicio de autenticación, motor de reportes. |
| N4 | Integración | Mecanismo mediante el cual dos o más sistemas intercambian información o consumen capacidades entre sí. | API, servicio web, hub, ESB, middleware, iPaaS. | API REST, servicio web SOAP, hub, conector ETL. |
| N5 | Plataforma | Capacidad tecnológica base que habilita múltiples servicios, aplicaciones o procesos. | Funciona como plataforma corporativa o institucional. | ERP, CRM, CMS, BPM, IAM, repositorio documental. |
| N6 | Servicio tecnológico | Servicio de TI que habilita operación, despliegue, soporte, monitoreo, disponibilidad o consumo tecnológico. | Servicio cloud, SaaS, DevOps, hosting, repositorio. | Microsoft 365, servicio cloud, pipeline CI/CD. |
| N7 | Solución analítica | Solución orientada al almacenamiento, procesamiento, análisis, visualización o explotación de datos. | BI, dashboard, DWH, data lake, ETL/ELT, GIS analítico. | Power BI, dashboard institucional, data warehouse. |
| N8 | Herramienta transversal | Herramienta común a varias áreas, procesos o soluciones, sin pertenecer exclusivamente a uno. | Capacidades comunes de seguridad, firma, IA, monitoreo, automatización. | SIEM, WAF, firma electrónica, RPA, chatbot. |

## 3.3 Secciones condicionales según la Naturaleza

No todas las secciones de la Ficha aplican igual a todas las soluciones. La siguiente matriz indica qué secciones son Obligatorias (O), Recomendadas (R), Opcionales (·) o No aplican (—) según la Naturaleza:

| Sección de la Ficha | N1 | N2 | N3 | N4 | N5 | N6 | N7 | N8 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1. Identificación general | O | O | O | O | O | O | O | O |
| 2. Arquitectura y despliegue | O | O | O | O | O | O | O | O |
| 2.b Contrato de interfaz (API/integración) | · | · | R | O | R | · | · | · |
| 3. Ciclo de vida y soporte | O | O | O | O | O | O | O | O |
| 4. Valor y gobierno de datos | O | O | R | R | O | R | O | R |
| 4.b Cobertura de proceso / usuarios activos | O | O | · | · | O | · | R | · |
| 5. Responsabilidad y gobierno | O | O | O | O | O | O | O | O |
| 6. Calidad — DOFA funcional | O | O | · | · | R | · | R | · |
| 6.b Calidad — Indicadores técnicos | O | O | O | O | O | O | O | O |
| 6.c Clasificación TIME | O | O | R | R | O | R | O | R |
| 7. Dimensión económica (TCO) | O | O | R | R | O | O | R | R |
| 8. Estado de la documentación | O | O | O | O | O | O | O | O |
| 9. Seguridad y continuidad | O | O | R | R | O | R | R | R |
| 9.b Insumos plan de mantenimiento | O | O | R | R | O | R | O | R |

| NOTA — O = Obligatoria · R = Recomendada · · = Opcional · — = No aplica. Si un campo no aplica a su naturaleza, déjelo en blanco y registre "No aplica por Naturaleza N#" en observaciones. Las filas 9 y 9.b son nuevas de la versión 8. |
| --- |

| NOTA — Por qué importa la condicionalidad — Forzar a diligenciar DOFA funcional o cobertura de proceso para una API o un microservicio genera datos artificiales que ensucian el catálogo. Si un campo no aplica a la naturaleza, no se diligencia ni se reporta como vacío. |
| --- |

# 4. FLUJO DE TRABAJO: CUÁNDO Y CÓMO USAR LA FICHA

| NOTA — Principio rector — La Ficha no se diligencia una sola vez. Recorre tres momentos en el ciclo de vida de la solución y se actualiza al menos anualmente. El campo «Fase de diligenciamiento» de la Sección 1 debe reflejar siempre el momento actual. |
| --- |

## 4.1 Los tres momentos de diligenciamiento

| Momento | Cuándo ocurre | Secciones a completar | Responsable principal |
| --- | --- | --- | --- |
| 1. Preliminar · En Levantamiento | Al aprobarse la iniciativa o proyecto que origina la solución. | Secciones 1, 4 y 5 (Identificación, Valor, Responsables). | Líder Funcional + Enlace de TI |
| 2. Producción · Completa | Cuando la solución sale a producción (Act. 9 del P-A-GTI-03). | Todas las secciones aplicables según Naturaleza. Primera TIME, primer TCO, primera valoración de seguridad. | Líder Técnico de TI |
| 3. Revisión · En Revisión / Actualizada | Anual, vinculada a la planeación presupuestal del año siguiente. | Actualización de versión, vencimientos, TCO, incidentes, seguridad y reclasificación TIME. | Líder Técnico + Líder Funcional |

## 4.2 Participantes mínimos por sesión

El diligenciamiento de la Ficha requiere la participación articulada de cuatro roles. La sesión funcional y la técnica pueden separarse en agendas distintas, pero ambas son obligatorias.

| Rol | Aporta principalmente | Secciones que diligencia |
| --- | --- | --- |
| Responsable Técnico (TI) | Información técnica de la solución, plataforma, versiones, integraciones, incidentes, riesgos, seguridad. | Secciones 2, 3, 6.b, 7 y 9 (parte técnica). |
| Responsable Funcional (Área usuaria) | Procesos que soporta, valor para la entidad, satisfacción de usuarios, DOFA funcional. | Secciones 1, 4, 5 y parte de 6. |
| Área Financiera / Contratos | Costos reales de licencias, soporte e infraestructura. Vencimientos. | Sección 7 (TCO) y campos de vencimiento de la Sección 3. |
| Líder de TI (Coordinador) | Síntesis del análisis TIME, clasificación estratégica y prioridad de intervención. | Campo TIME de la Sección 6.c y validación general de la Ficha. |

## 4.3 Disparadores de reclasificación fuera del ciclo anual

Además de la revisión anual, los siguientes eventos obligan a actualizar la Ficha y reclasificar TIME de forma inmediata.

| Evento disparador | Acción mínima requerida | Plazo |
| --- | --- | --- |
| Vencimiento de soporte en < 6 meses sin renovación planificada | Reclasificar a M (Migrar) y activar proceso contractual. | Inmediato |
| Cambio normativo que afecte la solución | Revisar marco legal, clasificación de información y obligaciones derivadas. | 30 días |
| Incidente grave que supere el umbral del ANS por más de 3 días | Revisar eficiencia técnica y posible reclasificación TIME. | 15 días |
| Fin del ciclo de vida declarado por el fabricante del componente central | Reclasificar a M o E según valor al negocio. | Inmediato |
| Cambio de Responsable Técnico o Funcional | Actualizar Sección 5 y revalidar la Ficha completa. | 30 días |
| Absorción de funcionalidades por otra solución | Evaluar E (Eliminar) si la solución queda sin procesos activos. | 60 días |
| Incidente de seguridad con afectación de datos personales | Revisar Sección 4 y 9 (seguridad) y notificar a la SIC si aplica. | Inmediato |

# 5. GUÍA DE DILIGENCIAMIENTO CAMPO A CAMPO

| NOTA — Convención de roles: T = Responsable Técnico TI · F = Responsable Funcional · $ = Contratos/Financiero · C = Coordinador TI. Campos marcados con (*) son de obligatorio diligenciamiento para todas las naturalezas; los demás aplican según la matriz de la Sección 3.3. Nunca use 'XXXX' o 'N/A' sin justificación cuando exista vocabulario controlado; use 'No definido' o 'Pendiente de verificación'. |
| --- |

## 5.1 Sección 1 — Identificación general

| Campo | Criterio de diligenciamiento | Error frecuente |
| --- | --- | --- |
| ID solución (*) | Código único con patrón SYS-NNNN (N1), APP-NNNN (N2), CMP-NNNN (N3), INT-NNNN (N4), PLT-NNNN (N5), SVC-NNNN (N6), BI-NNNN (N7), HT-NNNN (N8). El Coordinador TI reserva el código. | Usar nombres descriptivos en vez del código estándar. |
| Nombre oficial (*) | Nombre completo y oficial. Coherente con contratos y actos administrativos. | Poner la sigla como nombre. |
| Sigla / Acrónimo | Sigla común con la que se conoce la solución, sin puntos. | Inventar siglas que nadie usa. |
| Naturaleza (*) | Elegir N1–N8 usando el árbol de decisión de la Sección 3.1. | Escoger por intuición sin revisar la definición operativa. |
| Tipo detallado (*) | Elegir de la lista filtrada por la Naturaleza (glosario 10.2). No texto libre. | Texto libre o valores fuera del vocabulario. |
| Categoría Institucional (*) | Estratégica / Misional / Apoyo / Evaluación / Otros. Una sola. | Texto libre, valores mixtos. |
| Descripción de la solución (*) | Máximo 10 líneas. Qué hace, para quién, en qué contexto. No copiar el objeto del contrato. | Copiar el objeto contractual. |
| Funcionalidades principales | Entre 3 y 10 funciones clave, con verbos de acción. | Listar características técnicas en vez de funciones. |
| Dependencia dueña del proceso (*) | Dependencia dueña del PROCESO DE NEGOCIO que soporta la solución. | Confundir con la dependencia que ejecuta el proyecto técnico. |
| Dependencia ejecutora | Dependencia que ejecuta el proyecto técnico, cuando es distinta de la dueña del proceso. | Dejarlo vacío cuando sí hay una dependencia ejecutora distinta. |
| No. iniciativa / proyecto origen | ID del proyecto formal. Si es preexistente: «Preexistente». | Dejar en blanco; impide rastrear la inversión original. |
| Fase de diligenciamiento (*) | En Levantamiento / Completa / En Revisión / Actualizada. | Marcar «Completa» por apariencia de cumplimiento. |
| Prioridad de diligenciamiento asignada (*) | La define la OTIC: 1-Prioritaria / 2-Programada / 3-Diferida, según el plan de cierre de brechas por dependencia. | Dejarlo sin asignar indefinidamente. |

## 5.2 Sección 2 — Arquitectura y despliegue tecnológico

| Campo | Criterio de diligenciamiento | Error frecuente |
| --- | --- | --- |
| Procesos institucionales que soporta | Nombre EXACTO del proceso vigente del Mapa de Procesos. Varios separados por punto y coma. | Usar nombres informales o procesos descontinuados. |
| Módulos / Componentes | Liste módulos con su propósito. Si no aplica: «Sin modularización formal». | Inventar módulos para llenar el campo. |
| Entradas (Inputs) | Qué información recibe la solución y de dónde proviene. | Describir solo entradas de usuario y omitir integraciones. |
| Salidas (Outputs) | Qué produce: reportes, archivos, notificaciones, eventos. | Confundir salida con función. |
| Sistemas con los que se integra | Nombres de otros sistemas con los que intercambia datos. Uno por línea. | Agrupar todas las integraciones en un solo texto. |
| Tipo de integración | Protocolo (API REST, SOAP, FTP, SFTP, DB Link, archivo plano) + dirección. | Indicar solo «API» sin protocolo ni dirección. |
| Interopera con entidades externas | Sí / No. Si Sí, completar el campo siguiente. | Confundir con integraciones internas. |
| Entidades externas integradas | Nombres oficiales de entidades del Estado u organizaciones. | Listar sistemas en lugar de entidades. |
| Zona de arquitectura de referencia | Zona del Blueprint: Canales / Transaccional / Interoperabilidad / Notificaciones / Almacenamiento / Seguridad / Transversal. | Dejar en blanco por desconocimiento del Blueprint. |
| Modelo de despliegue (*) | On-Premises / Nube Pública / Nube Privada / Híbrida / SaaS / PaaS / No Definido. | Marcar «SaaS» cualquier cosa en la nube. |
| Tipo de arquitectura | Monolítico / Microservicios / SOA / Cliente-Servidor / N-Capas / Serverless. | Usar «No Documentado» por defecto. |
| Sistema operativo y versión | SO y versión del servidor principal. | Indicar solo «Linux» o «Windows» sin versión. |
| Versión y lenguaje de programación | Lenguaje(s) y versión. | Indicar lenguaje sin versión. |
| Plataforma y versión de base de datos | Motor y versión. | Indicar solo «SQL» u «Oracle» sin versión. |

## 5.3 Sección 3 — Ciclo de vida y soporte

| ATENCIÓN — Atención: vencimiento de soporte — Si el vencimiento ya pasó o está dentro de los próximos 6 meses, notifique inmediatamente al área de contratación y a la OTIC. Obliga a reclasificación TIME (ver disparador 4.3). |
| --- |

| Campo | Criterio de diligenciamiento | Error frecuente |
| --- | --- | --- |
| Estado actual de la solución (*) | Activo / En Migración / En Mantenimiento / En Desarrollo / Deprecado / Retirado. | Estados inventados como «Funcionando». |
| Versión actual | Formato Mayor.Menor.Parche (ej. 3.2.1). | Usar fecha como versión. |
| Fecha de salida a producción (*) | DD/MM/AAAA. | Dejar en blanco; usar formato numérico serial. |
| Fecha de última actualización | DD/MM/AAAA de la última versión mayor. | Confundir con último parche menor. |
| Tipo de desarrollo (*) | Desarrollo Propio / A la Medida / COTS / Open Source / SaaS / Híbrido. | Marcar «Híbrido» como comodín. |
| Fabricante / Proveedor (*) | Empresa o equipo que construyó la solución. | Confundir fabricante con proveedor de soporte. |
| Soporte técnico: ¿con quién? (*) | Empresa o área que brinda soporte actualmente. | Repetir el fabricante sin verificar quién opera el contrato. |
| Soporte vence en (*) | DD/MM/AAAA. | Almacenar como número serial; dejar en blanco. |
| Tipo de licenciamiento (*) | Propietario-Perpetuo / Propietario-Suscripción / Open Source-GPL/MIT/Apache / Freeware. | «Sin Definir» por defecto. |
| Estado del ANS (*) | Vigente / Vencido / No Aplica / En Negociación. | Marcar «Vigente» sin verificar el contrato. |
| Indicadores del ANS | Métricas pactadas: disponibilidad, tiempo de respuesta, ventana de mantenimiento. | Texto genérico como «cumple ANS». |

## 5.4 Sección 4 — Valor para la entidad y gobierno de datos

| Campo | Criterio de diligenciamiento | Error frecuente |
| --- | --- | --- |
| Objetivos estratégicos que apoya | Número del objetivo del Plan Estratégico Institucional al que contribuye. | Vincular a objetivos genéricos sin trazabilidad. |
| Marco legal mandatorio | ¿Existe ley, decreto o resolución que obliga esta solución? Cite el acto normativo. | Indicar «N/A» sin verificar. |
| Nivel de criticidad operacional (*) | Alta: si falla > 4h se detiene la operación. Media: alternativa manual temporal. Baja: no impacta. | Marcar «Alta» por defecto. |
| Cantidad de usuarios activos | Usuarios únicos que usan la solución regularmente. | Confundir con usuarios registrados inactivos. |
| Nivel de cobertura del proceso | Alto (>80%) / Medio (50-80%) / Bajo (<50%) / No Evaluado. | Sobreestimar la cobertura. |
| Clasificación de la información (*) | Pública / De Uso Interno / Reservada / Clasificada (Ley 1712). | Marcar «Pública» por defecto sin análisis. |
| Manejo de datos personales (*) | Sí-Responsable / Sí-Encargado / No (Ley 1581 de 2012). Verificar RNBD. | Marcar «No» sin verificar. |
| Número de registro RNBD | Diligencie si maneja datos personales. Registro ante la SIC. | Omitir el número una vez registrado ante la SIC. |

| ATENCIÓN — Registro Nacional de Bases de Datos (RNBD) — Si la solución gestiona datos personales, verifique el registro ante la Superintendencia de Industria y Comercio. Obligación: Ley 1581 de 2012, Decreto 1074 de 2015. |
| --- |

## 5.5 Sección 5 — Responsabilidad y gobierno de la solución

| Campo | Criterio de diligenciamiento | Error frecuente |
| --- | --- | --- |
| Área responsable técnico (*) | Área de TI responsable de la operación técnica. Generalmente la OTIC. | Indicar persona en vez de área. |
| Nombre responsable técnico (*) | Nombre completo y cargo. Actualizar si la persona rota. | Dejar nombre de quien ya no está. |
| Correo responsable técnico | Correo institucional. No usar correos personales. | Usar correo personal o genérico. |
| Área responsable funcional (*) | Área de negocio dueña de la solución. Coherente con la Sección 1. | Repetir el área técnica. |
| Nombre responsable funcional (*) | Nombre completo y cargo del líder funcional. | Indicar el cargo sin el nombre. |
| Correo responsable funcional | Correo institucional del líder funcional. | Usar correo grupal o genérico. |

| NOTA — Separación de responsabilidades — El Responsable Técnico responde por operación, seguridad y mantenimiento. El Responsable Funcional responde por requerimientos, capacitación y uso adecuado. Ambos firman la Ficha al cierre. |
| --- |

## 5.6 Sección 6 — Calidad y análisis estratégico

### 5.6.1 Análisis DOFA de la solución — obligatorio N1, N2, N5 · recomendado N7

No aplica para componentes, integraciones, servicios técnicos ni herramientas transversales (uso opcional).

| Fortalezas / Debilidades | Oportunidades / Amenazas |
| --- | --- |
| Fortalezas (interno, positivo): ¿qué hace bien la solución? Debilidades (interno, negativo): ¿qué falla con frecuencia? | Oportunidades (externo, positivo): ¿qué mejoras son posibles? Amenazas (externo, negativo): ¿riesgo de obsolescencia? |

### 5.6.2 Indicadores técnicos de calidad

| Campo | Criterio de diligenciamiento | Error frecuente |
| --- | --- | --- |
| Incidentes reportados (12M) (*) | Total de incidentes formalmente reportados en 12 meses. | Estimar sin consultar la mesa de servicio. |
| Riesgos tecnológicos identificados | Obsolescencia de SO, fin de soporte, deuda técnica, dependencias críticas. | Genéricos como «riesgo de fallas». |
| Nivel de madurez | 1 Inicial · 2 Gestionado · 3 Definido · 4 Optimizado. | Marcar nivel 3-4 sin evidencia documental. |
| Monitoreo activo | Sí / No — ¿tiene monitoreo técnico activo (APM, logs, alertas)? | Marcar «Sí» sin verificar herramientas de monitoreo reales. |
| Nivel de satisfacción | Alta (>80%) / Media (50-80%) / Baja (<50%) / No Medida. | Marcar «Alta» sin medición real. |

### 5.6.3 Clasificación en el cuadrante TIME

La clasificación TIME (Tolerar / Invertir / Migrar / Eliminar) resulta del análisis de tres ejes: Valor al negocio, Eficiencia técnica y Costos-Riesgos. Metodología completa en la Sección 6.

| Campo | Criterio de diligenciamiento | Error frecuente |
| --- | --- | --- |
| Eje 1: Valor al negocio (0-3) (*) | 0=sin procesos activos · 1=bajo · 2=apoyo importante · 3=misional crítico. | Calificar sin justificación. |
| Eje 2: Eficiencia técnica (0-3) (*) | 0=crítica · 1=baja (soporte por vencer) · 2=media (deuda técnica) · 3=alta. | Calificar 3 por defecto en sistemas nuevos. |
| Eje 3: Costos y riesgos (0-3) | 0=crítico (sin ANS) · 1=desfavorable · 2=moderado · 3=favorable. | Calificar sin tener el TCO calculado. |
| Clasificación TIME resultante (*) | I / T / M / E según la Matriz de Combinaciones (Sección 6.2). | Marcar I o T por defecto sin aplicar la matriz. |
| Tipo de intervención recomendada | Acción concreta con plazo. Ej.: «Migración a nube en Q2-2026». | Recomendaciones genéricas sin plazos. |

## 5.7 Sección 7 — Dimensión económica: TCO

| NOTA — El Costo Total de Propiedad (TCO) es la suma de todos los costos asociados con una solución durante un período. No requiere contabilidad forense: es un estimado anual razonable para comparar soluciones y justificar decisiones de inversión. |
| --- |

| ATENCIÓN — El área financiera o de contratos es la fuente primaria de los valores. No invente cifras. Use «Estimado pendiente de verificación» si no tiene el dato exacto. |
| --- |

| Concepto | Qué incluye | Fuente del dato |
| --- | --- | --- |
| Licenciamiento anual | Licencias de uso (perpetuas anualizadas o suscripciones). Open Source o desarrollo propio: $0. | Contrato o factura de licencias. |
| Soporte y mantenimiento | Contrato de soporte técnico correctivo anual. | Contrato de mantenimiento. |
| Infraestructura asociada | Servidores, almacenamiento, BD, red y seguridad atribuibles. SaaS: $0. | Área de infraestructura TI. |
| Mantenimiento evolutivo | Desarrollos nuevos o mejoras del año. Si no hay: $0. | Proyectos ejecutados o plan de mantenimiento. |
| Mantenimiento correctivo | Corrección de errores fuera del contrato de soporte base. | Contratos o registros de incidentes. |
| Capacitación y formación | Entrenamiento a usuarios y técnicos. | Registros de capacitación o RRHH. |
| TCO ANUAL TOTAL | Suma de los 6 conceptos. En el Catálogo se calcula automáticamente. | — |
| Ratio TCO/usuario | TCO Total ÷ usuarios activos. Compara eficiencia entre soluciones similares. | — |

## 5.8 Sección 8 — Estado de documentación

| Documento | Rol | Estado a registrar |
| --- | --- | --- |
| Manual técnico | T | Vigente / Desactualizado / No existe. |
| Manual de usuario | F | Vigente / Desactualizado / No existe. |
| Manual de operación | T | Vigente / Desactualizado / No existe. |
| Documentación de requerimientos (SRS) | T | Vigente / Desactualizado / No existe. |
| Arquitectura de solución | T | Vigente / Desactualizado / No existe. Enlace a wiki o repositorio. |
| Plan de pruebas | T | Vigente / Desactualizado / No existe. |
| Plan de mantenimiento | C | Vigente / Desactualizado / No existe. Resultado esperado del ciclo anual. |

## 5.9 Sección 9 — Seguridad, continuidad e insumos para el Plan de Mantenimiento · Nueva en V8

| NOTA — Sección nueva de la versión 8, alineada con el Modelo de Seguridad y Privacidad de la Información (MSPI) de MinTIC, ISO/IEC 27001, la NTC 5854/WCAG de accesibilidad y el lineamiento MGGTI.LI.SI.09 (Plan de mantenimiento). Obligatoria para N1, N2 y N5; recomendada para las demás naturalezas. |
| --- |

| Campo | Criterio de diligenciamiento | Error frecuente |
| --- | --- | --- |
| Valoración de riesgo de seguridad (MSPI/ISO 27001) (*) | Vigente / Desactualizada / No realizada. Consulte con el Oficial de Seguridad de la Información. | Marcar «Vigente» sin evidencia del análisis de riesgo. |
| Nivel de riesgo residual | Alto / Medio / Bajo / No evaluado, tras aplicar los controles existentes. | Confundir riesgo inherente con riesgo residual. |
| Cumple accesibilidad web (NTC 5854/WCAG) | Sí / No / No aplica (uso interno). Obligatorio verificar en soluciones de cara al ciudadano (N1, N2 con canal web). | Marcar «No aplica» en portales ciudadanos. |
| Copia de respaldo (backup) definida (*) | Sí / No / Desconocido. | Asumir que existe backup sin verificar con el equipo de infraestructura. |
| Frecuencia de backup | Ej.: Diaria, Semanal, Mensual. | Dejar en blanco cuando sí existe una política definida. |
| RTO — Tiempo objetivo de recuperación | Horas. Tiempo máximo aceptable para restaurar el servicio tras una falla. | Confundir con el tiempo real del último incidente. |
| RPO — Punto objetivo de recuperación | Horas. Máxima pérdida de datos aceptable. | Dejarlo en blanco por desconocimiento; consulte a infraestructura. |
| Plan de continuidad / contingencia | Vigente / Desactualizado / No existe. | Marcar «Vigente» sin que exista el documento. |
| Tipo de mantenimiento recomendado | Preventivo / Correctivo / Evolutivo / Adaptativo / Ninguno-Evaluar retiro. | Elegir «Preventivo» por defecto sin análisis del estado real. |
| Periodicidad de mantenimiento sugerida | Mensual / Trimestral / Semestral / Anual / No aplica. | Dejarlo vacío cuando la solución es crítica. |
| Próxima fecha de revisión programada | DD/MM/AAAA. | Confundir con la fecha de la última revisión. |

| NOTA — Prioridad de intervención (calculada) — Este campo NO se diligencia en la Ficha. El Catálogo F-A-GTI-02 lo calcula automáticamente sumando puntajes de Criticidad (Alta=3/Media=2/Baja=1) + Clasificación TIME (E=3/M=2/T=1/I=0) + 2 puntos si el soporte está vencido. Resultado ≥6 = Alta, 4-5 = Media, <4 = Baja. Este dato alimenta directamente el futuro Plan de Mantenimiento de Sistemas de Información. |
| --- |

# 6. METODOLOGÍA TIME — CLASIFICACIÓN ESTRATÉGICA

| NOTA — Qué es el análisis TIME — El cuadrante TIME (Tolerar, Invertir, Migrar, Eliminar) es el marco analítico que la guía MGGTI.G.SI 2023 de MinTIC prescribe para tomar decisiones estratégicas sobre el portafolio de soluciones. Es el instrumento de gobernanza TI que responde: «¿qué hacemos con esta solución en el mediano y largo plazo?» |
| --- |

## 6.1 Los tres ejes de evaluación

| Eje | Qué mide | Campos de la Ficha | Escala 0-3 |
| --- | --- | --- | --- |
| Eje 1 — Valor al negocio | Importancia para la misión, procesos críticos y objetivos estratégicos. | Procesos · Criticidad · Cobertura · Objetivos estratégicos · Marco legal · Usuarios activos. | 3 alto: misional crítico, mandato legal. 2 medio: apoyo importante. 1 bajo. 0 ninguno. |
| Eje 2 — Eficiencia técnica | Calidad técnica: estándares, vigencia del soporte, incidentes, sostenibilidad arquitectónica. | Estado · Vencimiento soporte · Madurez · Documentación · Incidentes 12M · Seguridad · Arquitectura. | 3 alta: soporte vigente, arquitectura moderna. 2 media: deuda técnica. 1 baja. 0 crítica. |
| Eje 3 — Costos y riesgos | Justificación de la inversión frente al valor y nivel de riesgo. | TCO anual · Ratio TCO/usuario · Amenazas · Riesgos · ANS · Riesgo de seguridad residual. | 3 favorable: costo justificado, ANS vigente. 2 moderado. 1 desfavorable. 0 crítico. |

## 6.2 Los cuatro cuadrantes TIME

| Cuadrante | Criterio | Descripción y acciones |
| --- | --- | --- |
| I — INVERTIR / INNOVAR | Alto valor (3) + Alta eficiencia (2-3) + Costos justificados (2-3) | Motor de la operación misional. Incluir en el Plan de Mantenimiento Evolutivo con prioridad alta, asignar presupuesto de innovación, ANS exigente. No confundir crítico con bien administrado: revisar anualmente. |
| T — TOLERAR | Valor medio-alto (2-3) + Eficiencia aceptable (2) + Costos razonables (2-3) | Cumple su función sin destacar. Mantenimiento correctivo mínimo, sin inversión significativa. Si el soporte vence en <12 meses sin renovación, reclasificar a M urgente. |
| M — MIGRAR | Valor alto (2-3) + Eficiencia baja (0-1) + Costos desfavorables (1-2) | El proceso lo necesita pero la plataforma está deteriorada. Formular proyecto de migración con cronograma y presupuesto; no invertir en nuevas funcionalidades del sistema a migrar. |
| E — ELIMINAR | Valor bajo o nulo (0-1) + Eficiencia baja (0-1) + Costos no justificados (0-1) | Ya no aporta valor estratégico. Verificar dependencias, migrar datos históricos, desactivar accesos y contratos, documentar el retiro (Estado = Retirado, se conserva la Ficha por trazabilidad). |

## 6.3 Matriz de combinaciones — cómo interpretar los tres ejes juntos

| Valor | Eficiencia | Costos/riesgos | Clasificación | Interpretación |
| --- | --- | --- | --- | --- |
| Alto (3) | Alta (3) | Favorable (3) | I — Invertir | El mejor escenario. Máximo potencial de inversión. |
| Alto (3) | Alta (3) | Desfavorable (1) | I ≫ T | Alto valor y técnica, pero costos elevados. Revisar contratos. |
| Alto (3) | Baja (1) | Desfavorable (1) | M — Migrar | Necesario pero deteriorado. Migración urgente. |
| Medio (2) | Media (2) | Moderado (2) | T — Tolerar | Situación estable. Mantener sin grandes inversiones. |
| Bajo (1) | Alta (3) | Favorable (3) | T ≫ E | Bien construido pero sin uso real. Si no tiene futuro → E. |
| Bajo (1) | Baja (1) | Desfavorable (1) | E — Eliminar | Todos los indicadores apuntan al retiro. |
| Ninguno (0) | Cualquiera | Cualquiera | E — Eliminar | Sin valor para ningún proceso: retirar independientemente del estado técnico. |

# 7. DIMENSIÓN ECONÓMICA — TCO (COSTO TOTAL DE PROPIEDAD)

## 7.1 Conceptos de costo a incluir

| Concepto de costo | Qué incluye y cómo calcularlo |
| --- | --- |
| Licenciamiento | Costo anual de licencias. Suscripciones: valor del contrato vigente. Perpetuas: amortizar a 5 años. |
| Soporte y mantenimiento | Contrato de soporte correctivo con el proveedor. Si incluye ANS, especificarlo. |
| Infraestructura | Servidores, almacenamiento, respaldo, seguridad perimetral atribuibles. SaaS: $0. |
| Mantenimiento evolutivo | Nuevas funcionalidades o mejoras mayores durante el año. |
| Mantenimiento correctivo | Corrección de errores no cubiertos por el contrato de soporte. |
| Capacitación | Cursos, talleres, acompañamiento para usuarios y personal técnico. |

## 7.2 Ratios y métricas de análisis

| Métrica | Cómo calcularla y qué revela |
| --- | --- |
| Ratio TCO / usuario activo | TCO Total ÷ Usuarios activos. Un ratio > $3M/usuario/año merece revisión estratégica salvo funciones muy críticas. |
| % TCO sobre presupuesto de TI | TCO / Presupuesto total de TI × 100. Identifica cuánto concentra cada solución. |
| Tendencia TCO (3 años) | Compara el TCO de los 3 últimos años; costos que suben sin valor proporcional son señal de E. |

# 8. EJEMPLOS PRÁCTICOS POR TIPO DE SOLUCIÓN

Cuatro fichas diligenciadas con datos ilustrativos que muestran cómo varía el llenado según la Naturaleza. Los datos son ejemplos; no corresponden a soluciones reales del Ministerio.

## 8.1 Ejemplo — Sistema de Información (N1): REAA

| Campo | Valor de ejemplo |
| --- | --- |
| Identificación | ID: SYS-0001 · Sigla: REAA · Categoría: Misional · Dependencia: Dirección de Bosques, Biodiversidad y Servicios Ecosistémicos. |
| Descripción | Gestión de las autoridades ambientales para el registro automatizado de ecosistemas y áreas priorizadas para Pago por Servicios Ambientales. |
| Arquitectura | Nube Privada · N-Capas · Ubuntu 22.04 · PHP 7.4 · PostgreSQL 14 · Zona: Transaccional · API REST con SIRH. |
| Ciclo de vida | Activo · v1.0 · Producción 12/03/2022 · A la medida (Heinsohn) · Soporte vence 30/06/2027 · ANS vigente (99%). |
| Valor | Procesos P-07, P-08 · Criticidad Alta · 2.500 usuarios · Uso Interno · Datos personales: Sí-Encargado, RNBD registrado. |
| Seguridad y continuidad | Valoración de riesgo: Vigente · Backup: Sí, diario · RTO 4h · RPO 1h · Plan de continuidad: Vigente. |
| TIME | Valor 3 · Eficiencia 2 (PHP 7.4 fin de soporte) · Costos 2 · Clasificación: T con alerta de migración. |
| TCO anual | Soporte $180M · Infraestructura $60M · Evolutivo $90M · Capacitación $4M · Total $334M. |

## 8.2 Ejemplo — API de Integración (N4): API-AUT

| Campo | Valor de ejemplo |
| --- | --- |
| Identificación | ID: INT-0014 · Sigla: API-AUT · Categoría: Apoyo · Dependencia: OTIC. |
| Descripción | API REST que media la autenticación de ciudadanos contra GOV.CO y emite tokens JWT. |
| Arquitectura | Híbrido (gateway nube, validación on-premises) · Microservicios · Node.js 20 · Redis 7 · Zona: Seguridad. |
| Ciclo de vida | Activo · Producción 15/02/2025 · Desarrollo propio (OTIC) · Soporte interno · ANS: No Aplica. |
| TIME | Valor 3 · Eficiencia 3 (0 incidentes en 9 meses) · Costos 3 · Clasificación: I — Invertir. |
| TCO anual | Soporte interno $25M · Infraestructura $12M · Evolutivo $30M · Total $67M. |

## 8.3 Ejemplo — Solución analítica (N7): DASH-AMB

| Campo | Valor de ejemplo |
| --- | --- |
| Identificación | ID: BI-0007 · Sigla: DASH-AMB · Categoría: Estratégica · Dependencia: Oficina Asesora de Planeación. |
| Descripción | Dashboard de seguimiento del Plan Estratégico Institucional con indicadores ambientales clave. |
| Arquitectura | SaaS (Power BI) · Zona: Almacenamiento — Datos Analíticos · ETL diario desde REAA, RUNAP y SIAC. |
| TIME | Valor 2 (estratégico, no operacional) · Eficiencia 3 (SaaS) · Costos 3 · Clasificación: T — Tolerar. |
| TCO anual | Licenciamiento $30M · Evolutivo $25M · Capacitación $3M · Total $58M. |

## 8.4 Ejemplo — Herramienta transversal (N8): FIRMA-DIG

| Campo | Valor de ejemplo |
| --- | --- |
| Identificación | ID: HT-0003 · Sigla: FIRMA-DIG · Categoría: Apoyo · Dependencia: Secretaría General. |
| Descripción | Firma electrónica certificada para actos administrativos, integrada con gestión documental y contratación. |
| TIME | Valor 3 (mandato legal) · Eficiencia 3 (SaaS) · Costos 2 · Clasificación: I — Invertir / Innovar. |
| TCO anual | Suscripción $95M · Capacitación $4M · Total $99M. |

# 9. GLOSARIO DE LISTAS DESPLEGABLES — DEFINICIÓN DE CADA OPCIÓN

| NOTA — Esta sección es el vocabulario controlado oficial. Cada campo de la Ficha y del Catálogo que tiene lista desplegable tiene su definición aquí. Cuando tenga dudas, consulte primero la columna «Definición» y luego pregunte al Coordinador TI. Nunca use texto libre cuando exista vocabulario controlado. Las subsecciones 9.16 a 9.23 son nuevas de la versión 8. |
| --- |

## 9.1 Naturaleza de la solución (N1-N8)

| Código | Opción | Definición para el diligenciante |
| --- | --- | --- |
| N1 | Sistema de información | Solución que soporta procesos institucionales completos con base de datos propia. Ej.: SIGTRAM, sistema de PQRSD. |
| N2 | Aplicación | Software de funcionalidad acotada orientado a una tarea o canal. Ej.: app de radicación, portal ciudadano. |
| N3 | Componente | Elemento técnico que hace parte de una solución mayor, con ciclo de vida propio. Ej.: microservicio de autenticación. |
| N4 | Integración | Mecanismo para intercambio de datos entre sistemas. Ej.: API REST, ETL, hub de integración. |
| N5 | Plataforma | Ambiente que habilita el desarrollo, despliegue u operación de otras soluciones. Ej.: BPM, CMS, LMS. |
| N6 | Servicio tecnológico | Capacidad consumida como servicio, generalmente transversal. Ej.: correo, VPN, SSO. |
| N7 | Solución analítica | Herramienta para análisis de datos e inteligencia de negocio. Ej.: Dashboard Power BI, Data Warehouse. |
| N8 | Herramienta transversal | Software de productividad de uso generalizado. Ej.: Office 365, firma electrónica. |

## 9.2 Categoría institucional

| Opción | Definición para el diligenciante |
| --- | --- |
| Estratégica | Soporta la formulación de política pública y la toma de decisiones directivas. |
| Misional | Directamente relacionada con la función constitucional del Ministerio. Si su retiro detiene la función misional → Misional. |
| Apoyo | Facilita procesos administrativos internos: RRHH, presupuesto, contratación, gestión documental. |
| Evaluación | Permite medir el desempeño institucional y el cumplimiento de planes. |
| Otros | No clasifica en las categorías anteriores; debe justificarse la excepción. |

## 9.3 Estado de la solución

| Opción | Definición para el diligenciante |
| --- | --- |
| Activo | En producción y en uso normal con soporte vigente o al menos operación estable. |
| En Migración | En proceso formal de migración a nueva plataforma o arquitectura. |
| En Mantenimiento | Activo pero en corrección mayor, mejora o actualización de versión importante. |
| En Desarrollo | Aún no está disponible en producción para los usuarios. |
| Deprecado | Sigue en operación pero su reemplazo ya fue decidido o está en curso. |
| Retirado | Retirado definitivamente del servicio. Se conserva la Ficha y el registro en el Catálogo como histórico (Ley 594/2000). Nunca se elimina la fila del Catálogo. |

## 9.4 Modelo de despliegue

| Opción | Definición para el diligenciante |
| --- | --- |
| On-Premises | Instalado y operado en servidores propios o del Datacenter institucional. |
| Nube pública | En infraestructura de un proveedor de nube (AWS, Azure, GCP), compartida. |
| Nube privada | En infraestructura dedicada exclusivamente al Ministerio, gestionada externamente. |
| Híbrida | Combinación: algunos componentes on-premise y otros en nube. |
| SaaS | Software e infraestructura completamente gestionados por el proveedor. |
| PaaS | El Ministerio opera la aplicación sobre una plataforma gestionada por el proveedor. |

## 9.5 Tipo de licenciamiento

| Opción | Definición para el diligenciante |
| --- | --- |
| Propietario-Perpetuo | Se paga una vez el derecho de uso indefinido. |
| Propietario-Suscripción | Pago periódico por el derecho de uso; si vence el contrato, se pierde el acceso. |
| Open Source (GPL/MIT/Apache) | Uso libre bajo condiciones de la licencia. Sin costo de adquisición. |
| Freeware | Gratuito, sin garantías formales ni SLA del fabricante. |
| Dominio Público | Sin restricciones de uso, modificación o distribución. |

## 9.6 Zona de arquitectura de referencia

| Opción | Definición para el diligenciante |
| --- | --- |
| Canales | Interacción con usuarios internos y externos: portales, apps móviles, formularios, chatbots. |
| Transaccional | Sistemas que procesan y registran operaciones del negocio. |
| Interoperabilidad | Integración entre sistemas internos y externos: APIs, ESB, hubs, ETL. |
| Notificaciones | Comunicación automática con usuarios: alertas, correos, SMS institucionales. |
| Almacenamiento | Bases de datos, repositorios documentales, archivos digitales, respaldo. |
| Seguridad | Autenticación, autorización, cifrado, IAM/SSO, WAF, certificados. |
| Transversal | Servicios compartidos: monitoreo de plataforma, logs centralizados, bus de eventos. |

## 9.7 Nivel de madurez

| Opción | Definición para el diligenciante |
| --- | --- |
| 1 Inicial | Documentación mínima o nula. Dependencia del conocimiento tácito del responsable técnico. |
| 2 Gestionado | Procesos básicos documentados. Avances parciales visibles. |
| 3 Definido | Procesos definidos, documentados y conocidos por el equipo. Operación predecible. |
| 4 Optimizado | Medición continua del desempeño. Mejora formal documentada. |

## 9.8 Estado de documentación

| Opción | Definición para el diligenciante |
| --- | --- |
| Vigente | El documento existe, está actualizado y fue formalmente aprobado (últimos 12 meses). |
| Desactualizado | Existe pero no refleja el estado actual del sistema. |
| No existe | No ha sido elaborado. Incumple MGGTI.LI.SI.08; debe incluirse en el Plan de Mantenimiento del próximo año. |

## 9.9 Clasificación TIME

| Código | Opción | Definición para el diligenciante |
| --- | --- | --- |
| I | Invertir / Innovar | Estratégico y técnicamente sólido. Merece más inversión y nuevas funcionalidades. |
| T | Tolerar | Funciona bien para su propósito actual, sin justificar inversión adicional a corto plazo. |
| M | Migrar | Alto valor pero necesita modernización, cambio de plataforma o migración a nube. |
| E | Eliminar | No genera valor suficiente para justificar su costo. Planificar retiro ordenado. |

## 9.16 Vigencia del registro · Nueva en V8

| Opción | Definición |
| --- | --- |
| Activo en gestión | La solución está en operación. Se gestiona activamente su avance de diligenciamiento en el Catálogo. |
| Histórico - conservar | La solución fue retirada. Se calcula automáticamente en el Catálogo y NUNCA implica eliminar la fila: es el histórico institucional de desarrollos. |

## 9.17 Prioridad de diligenciamiento asignada · Nueva en V8

| Opción | Definición |
| --- | --- |
| 1 - Prioritaria | La OTIC decidió cerrar la brecha de esta solución en el trimestre en curso. |
| 2 - Programada | Programada para el próximo trimestre dentro del plan de cierre por dependencia. |
| 3 - Diferida | Segunda ola: se completará una vez cerradas las prioritarias. |

## 9.18 Valoración de riesgo de seguridad (MSPI/ISO 27001) · Nueva en V8

| Opción | Definición |
| --- | --- |
| Vigente | Existe un análisis de riesgo de seguridad de la solución con menos de 12 meses de antigüedad. |
| Desactualizada | Existe un análisis previo pero desactualizado frente al estado actual de la solución. |
| No realizada | No se ha realizado valoración formal de riesgo de seguridad. |

## 9.19 Nivel de riesgo residual · Nueva en V8

| Opción | Definición |
| --- | --- |
| Alto | Los controles existentes no mitigan suficientemente el riesgo identificado. |
| Medio | Los controles mitigan parcialmente el riesgo; requiere seguimiento. |
| Bajo | El riesgo está adecuadamente controlado. |
| No evaluado | Aún no se ha determinado el nivel de riesgo residual. |

## 9.20 Accesibilidad web (NTC 5854 / WCAG) · Nueva en V8

| Opción | Definición |
| --- | --- |
| Sí | La solución cumple los criterios de accesibilidad web NTC 5854 / WCAG nivel AA. |
| No | La solución tiene canal web de cara al ciudadano y no cumple los criterios de accesibilidad. |
| No aplica (uso interno) | La solución no tiene canal web público, o es exclusivamente de uso interno. |

## 9.21 Copia de respaldo (backup) definida · Nueva en V8

| Opción | Definición |
| --- | --- |
| Sí | Existe una política de copias de respaldo formalmente definida y verificada con infraestructura. |
| No | No existe copia de respaldo para esta solución. |
| Desconocido | El responsable técnico no tiene certeza; debe verificarse con el área de infraestructura antes del cierre de la Ficha. |

## 9.22 Plan de continuidad / contingencia · Nueva en V8

| Opción | Definición |
| --- | --- |
| Vigente | Existe un plan de continuidad documentado y probado en los últimos 12 meses. |
| Desactualizado | Existe un plan pero no ha sido revisado ni probado recientemente. |
| No existe | No se ha elaborado plan de continuidad para esta solución. |

## 9.23 Tipo de mantenimiento recomendado y prioridad de intervención · Nueva en V8

| Opción | Definición |
| --- | --- |
| Preventivo | Mantenimiento programado para evitar fallas futuras en una solución estable. |
| Correctivo | Corrección de fallas o defectos ya identificados. |
| Evolutivo | Mejora funcional o tecnológica que agrega valor sin ser urgente. |
| Adaptativo | Ajuste requerido por cambios en el entorno (normativo, de plataforma o de integración). |
| Ninguno - Evaluar retiro | La solución es candidata a evaluación de retiro (clasificación TIME = E). |
| Prioridad de intervención (calculada) | Alta / Media / Baja. Calculada automáticamente en el Catálogo combinando Criticidad + Clasificación TIME + vencimiento de soporte. No se diligencia manualmente. |

# 10. CHECKLIST DE VALIDACIÓN DE CALIDAD

Antes de firmar una Ficha y consolidarla en el Catálogo, el Coordinador (Líder de TI) verifica los siguientes controles. Una Ficha que no supera este checklist no se consolida.

## Control 1 — Completitud

| ☐ | Todos los campos marcados con (*) están diligenciados con valores del vocabulario controlado. |
| --- | --- |
| ☐ | La Naturaleza está seleccionada y el Tipo detallado es coherente con ella (Sección 3.2). |
| ☐ | Las secciones aplicables según la Naturaleza están completas según la matriz 3.3, incluida la Sección 9. |
| ☐ | Ningún campo aplicable contiene placeholders como «XXXX» o «N/A» sin justificación. |
| ☐ | La «Fase de diligenciamiento» refleja el momento real, no «Completa» por defecto. |

## Control 2 — Identidad y trazabilidad

| ☐ | El ID de la solución sigue el patrón institucional y no está duplicado en el Catálogo. |
| --- | --- |
| ☐ | La Dependencia dueña del proceso es distinta de la Dependencia ejecutora cuando corresponde. |
| ☐ | La Iniciativa / proyecto origen está indicada o se justifica como «Preexistente». |
| ☐ | La «Prioridad de diligenciamiento asignada» está diligenciada por la OTIC. |

## Control 3 — Cumplimiento legal y datos

| ☐ | La Clasificación de la información (Ley 1712) está validada por el Oficial de Seguridad de la Información. |
| --- | --- |
| ☐ | El Manejo de datos personales (Ley 1581) está validado por la Oficina Asesora Jurídica. |
| ☐ | Si maneja datos personales, el número de registro RNBD ante la SIC está consignado. |
| ☐ | El Marco legal aplicable cita la norma con número, año y tema. |

## Control 4 — Soporte, contratos y vencimientos

| ☐ | La fecha de Vencimiento del soporte está en formato DD/MM/AAAA. |
| --- | --- |
| ☐ | Si el vencimiento es < 6 meses, hay registro de la notificación al área de contratos. |
| ☐ | Estado del ANS está validado contra el contrato actual, no asumido. |

## Control 5 — Coherencia técnica

| ☐ | Modelo de despliegue es preciso (SaaS solo si el proveedor opera todo). |
| --- | --- |
| ☐ | Lenguaje de programación y plataforma de base de datos incluyen versión. |
| ☐ | Las integraciones especifican protocolo y dirección. |
| ☐ | La Zona de arquitectura de referencia está identificada según el Blueprint del Ministerio. |

## Control 6 — Seguridad y continuidad · Nuevo en V8

| ☐ | La Valoración de riesgo de seguridad tiene menos de 12 meses de antigüedad. |
| --- | --- |
| ☐ | Si la solución tiene canal web ciudadano, la accesibilidad NTC 5854/WCAG fue verificada. |
| ☐ | El estado del backup no quedó en «Desconocido»: se verificó con el área de infraestructura. |
| ☐ | El Tipo de mantenimiento recomendado y la Periodicidad sugerida están diligenciados. |

# CONTROL DE CAMBIOS DE LA GUÍA

| Ver. | Fecha | Descripción del cambio | Elaboró | Aprobó |
| --- | --- | --- | --- | --- |
| 7 | 24/09/2025 | Versión previa de la guía, alineada con Ficha F-A-GTI-01 V7. | OTIC | OTIC |
| 8 | 01/07/2026 | Rediseño profesional del documento con identidad institucional. Se incorpora la Sección 9 (Seguridad, continuidad e insumos para el Plan de Mantenimiento), se actualiza la matriz 3.3, se amplía el glosario (9.16-9.23) y el checklist (Control 6). Consistente con el Catálogo F-A-GTI-02 V4 y la Ficha F-A-GTI-01 V8. | Carlos Centeno (OTIC) con asistencia de Claude | (pendiente) |
