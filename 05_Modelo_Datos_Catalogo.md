# 05_Modelo_Datos_Catalogo

## 1. Objetivo

Definir el modelo definitivo del libro Excel del **F-A-GTI-02** después de cerrar la taxonomía de la Fase 1.

## 2. Decisiones de diseño que gobiernan el modelo

1. **El libro principal inventaría SI, no “soluciones tecnológicas” heterogéneas.**
2. **Las relaciones repetibles se normalizan**: integraciones e interfaces en una hoja; componentes en otra.
3. **La Ficha es el expediente completo** y el catálogo conserva el subconjunto necesario para identificar, gobernar, comparar, priorizar, alertar y decidir.
4. **Los datos operativos de calidad del diligenciamiento** (avance, prioridad de cierre, hallazgos) salen del catálogo principal y van a la hoja **Calidad**.
5. **La documentación detallada, stack técnico y DevOps** salen del catálogo principal y se conservan en Ficha, Componentes o ambos.

## 3. Estructura lógica definitiva del libro Excel

### 3.1 Hojas que debe contener

| Hoja | Se mantiene / crea | Función concreta |
| --- | --- | --- |
| `Catálogo_SI` | Sí | Inventario consolidado de un registro por SI. |
| `Integraciones_Interfaces` | Sí | Relación normalizada de integraciones, APIs, servicios web e interfaces relevantes. |
| `Componentes` | Sí | Componentes internos o compartidos de los SI cuando ameriten inventario independiente. |
| `Diccionario` | Sí | Definición, obligatoriedad, origen y reglas de cada campo de las hojas operativas. |
| `Listas` | Sí | Vocabularios controlados y tablas auxiliares de validación. |
| `Tablero` | Sí | Indicadores agregados, alertas y semáforos gerenciales. |
| `Calidad` | Sí | Completitud, hallazgos, trazabilidad de correcciones y control de revisión. |

### 3.2 Hojas que no deben existir en el diseño final

| Hoja actual / idea | Decisión | Justificación |
| --- | --- | --- |
| `Instrucciones` | Eliminar | La instrucción estable pertenece a la Guía (`07_Estructura_Guia_Final.md`), no al Excel. |
| `Alertas Caducidad` | Absorber en `Tablero` y `Calidad` | La alerta es una vista calculada, no un artefacto autónomo. |
| `Log de Calidad` | Sustituir por `Calidad` | Se conserva la función, con nombre más amplio y consistente. |
| `Avance por Dependencia` | Absorber en `Tablero` / `Calidad` | Es una vista calculada; no amerita hoja separada si puede construirse con tabla dinámica, segmento o sección de tablero. |
| `Control de Cambios` del libro | Eliminar como hoja | El control de cambios debe mantenerse en gestión documental del instrumento o en encabezado controlado, no como hoja operativa. |
| `Hoja2` | Eliminar tras migración | Es insumo transitorio, no diseño final. |

## 4. Lista exacta y ordenada de columnas del futuro `Catálogo_SI`

| Orden | Campo definitivo |
| --- | --- |
| 1 | ID_SI |
| 2 | Nombre_oficial |
| 3 | Sigla_Acronimo |
| 4 | Tipo_o_patron_de_SI |
| 5 | Categoria_institucional |
| 6 | Descripcion_breve |
| 7 | Procesos_institucionales_soportados |
| 8 | Dependencia_duena_del_proceso |
| 9 | Area_responsable_funcional |
| 10 | Responsable_funcional |
| 11 | Area_responsable_tecnica |
| 12 | Responsable_tecnico |
| 13 | Estado_del_SI |
| 14 | Fecha_salida_produccion |
| 15 | Version_actual |
| 16 | Modelo_de_despliegue |
| 17 | Tipo_de_desarrollo_adquisicion |
| 18 | Fabricante_o_proveedor_principal |
| 19 | Tipo_de_licenciamiento |
| 20 | Soporte_vigente_hasta |
| 21 | Estado_ANS_terceros |
| 22 | Marco_legal_mandatorio |
| 23 | Objetivos_estrategicos_que_apoya |
| 24 | Criticidad_operacional |
| 25 | Usuarios_activos |
| 26 | Cobertura_del_proceso |
| 27 | Clasificacion_de_la_informacion |
| 28 | Manejo_de_datos_personales |
| 29 | Interopera_con_entidades_externas |
| 30 | Numero_integraciones_activas |
| 31 | Numero_componentes_registrados |
| 32 | Valoracion_de_seguridad |
| 33 | Nivel_de_riesgo_residual |
| 34 | Backup_definido |
| 35 | Plan_de_continuidad |
| 36 | Estado_documentacion_minima |
| 37 | Clasificacion_TIME |
| 38 | Tipo_intervencion_recomendada |
| 39 | Prioridad_intervencion |
| 40 | TCO_anual_total_COP |
| 41 | Ratio_TCO_por_usuario_COP |
| 42 | Ultima_revision_anual |
| 43 | Proxima_revision_programada |
| 44 | Vigencia_del_registro |

## 5. Definición de cada campo del modelo final de `Catálogo_SI`

> Convenciones de fuente: **MinTIC** = obligación o recomendación derivada del MGGTI/MAE/MRAE/MSPI; **Institucional** = decisión de diseño OTIC; **Calculado** = valor derivado en el libro.

| Campo definitivo | Definición | Finalidad | Fuente | Obligatoriedad | Responsable del dato | Tipo de dato | Vocabulario controlado | Frecuencia / evento de actualización | Ubicación definitiva |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ID_SI | Código único del SI. | Identificación y trazabilidad. | Institucional | Obligatorio | OTIC | Texto | Patrón `SI-####` o equivalente oficial definido por OTIC | Creación del registro | Catálogo_SI |
| Nombre_oficial | Nombre institucional vigente del SI. | Identificar y comparar. | Institucional | Obligatorio | Responsable funcional | Texto | No aplica | Alta o cambio de nombre | Catálogo_SI |
| Sigla_Acronimo | Sigla o acrónimo usado oficialmente. | Búsqueda y reconocimiento. | Institucional | Recomendado | Responsable funcional | Texto | No aplica | Alta o cambio | Catálogo_SI |
| Tipo_o_patron_de_SI | Clasifica el SI como transaccional, ERP, CRM, BPM, CMS, SGD, GIS, solución analítica u otro. | Segmentación del portafolio. | Institucional basada en Fase 1 | Obligatorio | OTIC + responsables | Lista | Lista controlada | Alta o reclasificación | Catálogo_SI |
| Categoria_institucional | Clasificación institucional misional/estratégica/apoyo/evaluación/otro. | Priorización y análisis. | Institucional existente | Obligatorio | Responsable funcional | Lista | Lista controlada | Alta o cambio organizacional | Catálogo_SI |
| Descripcion_breve | Resumen de propósito y alcance. | Contexto ejecutivo del portafolio. | Institucional | Obligatorio | Responsable funcional | Texto corto | No aplica | Alta o cambio funcional | Catálogo_SI |
| Procesos_institucionales_soportados | Procesos del mapa institucional soportados por el SI. | Trazabilidad con negocio. | MAE/Institucional | Obligatorio | Responsable funcional | Texto / lista | Procesos vigentes | Alta o cambio de proceso | Catálogo_SI |
| Dependencia_duena_del_proceso | Dependencia dueña del proceso soportado. | Gobierno y rendición de cuentas. | Institucional | Obligatorio | Responsable funcional | Lista | Dependencias | Alta o cambio organizacional | Catálogo_SI |
| Area_responsable_funcional | Área que ejerce liderazgo funcional. | Gobierno del SI. | Institucional | Obligatorio | Responsable funcional | Lista | Dependencias | Alta o cambio | Catálogo_SI |
| Responsable_funcional | Nombre del responsable funcional designado. | Escalamiento y validación. | Institucional | Obligatorio | Responsable funcional | Texto | No aplica | Cambio de responsable | Catálogo_SI |
| Area_responsable_tecnica | Área TI responsable de la operación técnica. | Gobierno operativo. | Institucional | Obligatorio | Responsable técnico | Lista | Dependencias / áreas TI | Alta o cambio | Catálogo_SI |
| Responsable_tecnico | Nombre del responsable técnico designado. | Escalamiento técnico. | Institucional | Obligatorio | Responsable técnico | Texto | No aplica | Cambio de responsable | Catálogo_SI |
| Estado_del_SI | Estado actual del ciclo de vida. | Gestión del portafolio. | Institucional alineada con MGGTI | Obligatorio | Responsable técnico | Lista | Activo, En desarrollo, En mantenimiento, En migración, Deprecado, Retirado | Cambio de estado | Catálogo_SI |
| Fecha_salida_produccion | Fecha de primera puesta en producción. | Antigüedad y ciclo de vida. | Institucional | Obligatorio | Responsable técnico | Fecha | DD/MM/AAAA | Alta inicial | Catálogo_SI |
| Version_actual | Versión actualmente operativa. | Gestión de cambios. | Institucional | Recomendado | Responsable técnico | Texto | No aplica | Cada liberación mayor | Catálogo_SI |
| Modelo_de_despliegue | Modalidad principal de operación. | Arquitectura y riesgos. | Institucional / NIST complementario | Obligatorio | Responsable técnico | Lista | On-premises, nube pública, nube privada, híbrida, SaaS, PaaS | Cambio de despliegue | Catálogo_SI |
| Tipo_de_desarrollo_adquisicion | Forma de obtención del SI. | Gestión contractual y técnica. | Institucional | Obligatorio | Responsable técnico | Lista | Propio, a la medida, COTS, open source, SaaS, híbrido, legado | Alta o cambio | Catálogo_SI |
| Fabricante_o_proveedor_principal | Proveedor principal del producto o servicio. | Gestión contractual y soporte. | Institucional | Recomendado | Técnico / contratación | Texto | No aplica | Cambio contractual | Catálogo_SI |
| Tipo_de_licenciamiento | Modalidad principal de licenciamiento. | Riesgo contractual y costo. | Institucional | Recomendado | Técnico / contratación | Lista | Lista controlada | Cambio contractual | Catálogo_SI |
| Soporte_vigente_hasta | Fecha de vencimiento de soporte o mantenimiento principal. | Alertas y continuidad. | MGGTI.LI.SI.10 + institucional | Obligatorio | Técnico / contratación | Fecha | DD/MM/AAAA | Cada renovación | Catálogo_SI |
| Estado_ANS_terceros | Estado del ANS si el soporte es tercerizado. | Control de soporte. | MGGTI.LI.SI.10 | Condicional | Técnico / contratación | Lista | Vigente, Vencido, No aplica, En negociación | Cambio contractual | Catálogo_SI |
| Marco_legal_mandatorio | Norma principal que obliga o condiciona el SI. | Decisiones de permanencia y cumplimiento. | Institucional apoyada en marco legal | Recomendado | Responsable funcional | Texto corto | No aplica | Cambio normativo | Catálogo_SI |
| Objetivos_estrategicos_que_apoya | Objetivos institucionales o sectoriales soportados. | Priorización TIME y valor. | Institucional | Recomendado | Responsable funcional | Texto / lista | PEI/planeación vigente | Revisión anual | Catálogo_SI |
| Criticidad_operacional | Impacto por indisponibilidad del SI. | Priorización y continuidad. | Institucional / MSPI | Obligatorio | Responsable funcional + técnico | Lista | Alta, Media, Baja | Revisión anual o incidente relevante | Catálogo_SI |
| Usuarios_activos | Número de usuarios activos o recurrentes. | Comparación y costo relativo. | Institucional | Recomendado | Responsable funcional | Número entero | `>=0` | Revisión anual | Catálogo_SI |
| Cobertura_del_proceso | Grado de cobertura del proceso soportado. | Priorización y madurez funcional. | Institucional | Recomendado | Responsable funcional | Lista | Alto, Medio, Bajo, No evaluado | Revisión anual | Catálogo_SI |
| Clasificacion_de_la_informacion | Nivel de clasificación de la información tratada. | Cumplimiento y riesgo. | Ley 1712 + institucional | Obligatorio | Responsable funcional | Lista | Pública, Uso interno, Reservada, Clasificada | Cambio de tratamiento | Catálogo_SI |
| Manejo_de_datos_personales | Indica si el SI trata datos personales y en qué rol. | Cumplimiento y privacidad. | Ley 1581/Decreto 1074 + institucional | Obligatorio | Responsable funcional | Lista | Sí-responsable, Sí-encargado, No | Cambio de tratamiento | Catálogo_SI |
| Interopera_con_entidades_externas | Indica si hay interoperabilidad con terceros externos. | Riesgo e integración externa. | Institucional | Obligatorio | Responsable técnico | Lista | Sí / No | Alta o cambio de integración | Catálogo_SI |
| Numero_integraciones_activas | Conteo de integraciones/interfaces vigentes asociadas al SI. | Complejidad y trazabilidad. | Calculado | Obligatorio | Calculado desde hoja integraciones | Número entero | `>=0` | Automático | Catálogo_SI |
| Numero_componentes_registrados | Conteo de componentes registrados para el SI. | Complejidad tecnológica. | Calculado | Obligatorio | Calculado desde hoja componentes | Número entero | `>=0` | Automático | Catálogo_SI |
| Valoracion_de_seguridad | Vigencia de valoración MSPI/seguridad. | Gobierno de seguridad. | MSPI / institucional | Obligatorio | Responsable técnico / seguridad | Lista | Vigente, Desactualizada, No realizada | Revisión anual o incidente | Catálogo_SI |
| Nivel_de_riesgo_residual | Riesgo residual más reciente del SI. | Priorización y tratamiento. | MSPI / institucional | Recomendado | Seguridad / técnico | Lista | Alto, Medio, Bajo, No evaluado | Revisión anual | Catálogo_SI |
| Backup_definido | Indica si existe respaldo definido. | Continuidad. | Institucional / continuidad | Obligatorio | Responsable técnico | Lista | Sí, No, Desconocido | Revisión anual | Catálogo_SI |
| Plan_de_continuidad | Estado del plan de continuidad/contingencia. | Continuidad y auditoría. | Institucional / MSPI | Recomendado | Responsable técnico | Lista | Vigente, Desactualizado, No existe | Revisión anual | Catálogo_SI |
| Estado_documentacion_minima | Resultado agregado del estado de documentación mínima exigible. | Riesgo operativo y de conocimiento. | MGGTI.LI.SI.08 + calculado | Obligatorio | Calculado desde Ficha/Calidad | Lista | Completa, Parcial, Crítica, No evaluada | Revisión anual | Catálogo_SI |
| Clasificacion_TIME | Clasificación estratégica final del SI. | Decisión de portafolio. | MGGTI.G.SI + institucional | Obligatorio | OTIC / comité | Lista | I, T, M, E | Revisión anual o evento disparador | Catálogo_SI |
| Tipo_intervencion_recomendada | Acción principal sugerida. | Gestión de plan de acción. | Institucional | Obligatorio | OTIC | Texto corto / lista | Modernizar, migrar, retirar, sostener, optimizar | Revisión anual | Catálogo_SI |
| Prioridad_intervencion | Nivel de prioridad resultante. | Secuenciación del plan de mantenimiento/modernización. | Institucional / calculado | Obligatorio | OTIC | Lista | Alta, Media, Baja | Revisión anual | Catálogo_SI |
| TCO_anual_total_COP | Estimado o valor anual consolidado del TCO. | Comparación y decisión. | MGGTI.LI.SI.09 + institucional | Recomendado | Financiero / técnico | Número moneda | `>=0` | Revisión anual presupuestal | Catálogo_SI |
| Ratio_TCO_por_usuario_COP | TCO total dividido por usuarios activos. | Comparación relativa. | Calculado | Recomendado | Calculado | Número moneda | `>=0` | Automático | Catálogo_SI |
| Ultima_revision_anual | Fecha de última revisión integral del SI. | Control de vigencia. | Institucional | Obligatorio | OTIC | Fecha | DD/MM/AAAA | Revisión anual | Catálogo_SI |
| Proxima_revision_programada | Fecha programada de la próxima revisión. | Planeación y alertas. | Institucional | Recomendado | OTIC | Fecha | DD/MM/AAAA | Cada revisión | Catálogo_SI |
| Vigencia_del_registro | Señala si el registro sigue activo o se conserva históricamente. | Preservación del histórico. | Institucional | Obligatorio | OTIC / calculado | Lista | Vigente, Histórico | Cambio de retiro/archivo | Catálogo_SI |

## 6. Modelo mínimo de las hojas normalizadas complementarias

### 6.1 `Integraciones_Interfaces`

**Una fila por integración o interfaz relevante.**

| Orden | Campo |
| --- | --- |
| 1 | ID_Integracion |
| 2 | ID_SI_Origen |
| 3 | Nombre_SI_Origen |
| 4 | ID_SI_Destino_o_Activo_Destino |
| 5 | Nombre_Destino |
| 6 | Tipo_de_registro |
| 7 | Tipo_de_interfaz_o_mecanismo |
| 8 | Proposito |
| 9 | Direccion_del_flujo |
| 10 | Entidad_externa_relacionada |
| 11 | Criticidad |
| 12 | Frecuencia |
| 13 | Responsable_tecnico |
| 14 | Estado |
| 15 | Observaciones |

### 6.2 `Componentes`

**Una fila por componente que merezca inventario independiente.**

| Orden | Campo |
| --- | --- |
| 1 | ID_Componente |
| 2 | ID_SI_Padre |
| 3 | Nombre_Componente |
| 4 | Tipo_de_Componente |
| 5 | Función |
| 6 | Compartido_con_otro_SI |
| 7 | Estado |
| 8 | Version |
| 9 | Modelo_de_Despliegue |
| 10 | Tecnologia_principal |
| 11 | Base_de_datos_asociada |
| 12 | Proveedor_o_Fabricante |
| 13 | Soporte_vigente_hasta |
| 14 | Criticidad |
| 15 | Observaciones |

### 6.3 `Diccionario`

Debe contener al menos: hoja, campo, definición, fuente, obligatoriedad, responsable, tipo de dato, vocabulario, regla de validación, fórmula si aplica, origen (Catálogo / Ficha / Calculado).

### 6.4 `Listas`

Debe contener listas separadas para:

- Tipo_o_patron_de_SI
- Categoria_institucional
- Estado_del_SI
- Modelo_de_despliegue
- Tipo_de_desarrollo_adquisicion
- Tipo_de_licenciamiento
- Estado_ANS_terceros
- Criticidad_operacional
- Cobertura_del_proceso
- Clasificacion_de_la_informacion
- Manejo_de_datos_personales
- Valoracion_de_seguridad
- Nivel_de_riesgo_residual
- Estado_documentacion_minima
- Clasificacion_TIME
- Prioridad_intervencion
- Dependencias institucionales
- Tipo_de_registro en Integraciones_Interfaces
- Tipo_de_Componente

### 6.5 `Tablero`

Debe consolidar, como mínimo:

1. número total de SI vigentes e históricos;
2. SI por categoría institucional;
3. SI por tipo o patrón;
4. TIME del portafolio;
5. soporte vencido / por vencer;
6. TCO total y promedio;
7. SI con valoración de seguridad desactualizada o no realizada;
8. SI sin plan de continuidad vigente;
9. SI con documentación crítica;
10. próximas revisiones programadas.

### 6.6 `Calidad`

Debe incluir:

- completitud del registro por SI;
- campos obligatorios faltantes;
- inconsistencias de vocabulario;
- fecha de detección;
- responsable de corrección;
- fecha de cierre;
- trazabilidad de reclasificaciones;
- observaciones de migración desde el inventario actual.

## 7. Auditoría de las 99 columnas actuales

| Col. | Campo actual | Decisión | Ubicación definitiva | Justificación resumida |
| --- | --- | --- | --- | --- |
| A | ID Solución | MODIFICAR | Catálogo_SI → ID_SI | Conservar el identificador, ajustando patrón a SI. |
| B | Nombre oficial de la solución | MODIFICAR | Catálogo_SI → Nombre_oficial | Se conserva con foco exclusivo en SI. |
| C | Sigla / Acrónimo | MANTENER | Catálogo_SI | Sigue siendo útil para identificación. |
| D | Naturaleza (N1-N8) | ELIMINAR | No va como columna final | La hoja ya será exclusiva de SI; N1-N8 se sustituye por clasificación previa de inventario. |
| E | Tipo detallado | MODIFICAR | Catálogo_SI → Tipo_o_patron_de_SI | Se conserva la idea, pero restringida a patrones de SI. |
| F | Categoría institucional | MANTENER | Catálogo_SI | Permite comparar y priorizar. |
| G | Descripción de la solución | MODIFICAR | Catálogo_SI → Descripcion_breve | Se mantiene en formato ejecutivo. |
| H | Funcionalidades principales | MOVER_A_FICHA | Ficha | Demasiado detallado para la vista consolidada. |
| I | Dependencia dueña del proceso | MANTENER | Catálogo_SI | Dato de gobierno esencial. |
| J | No. iniciativa / proyecto origen | MOVER_A_FICHA | Ficha | Útil para trazabilidad histórica, no para la vista principal. |
| K | Fase de diligenciamiento de la ficha | MOVER_A_OTRO_ARTEFACTO | Calidad | Gestiona avance documental, no el inventario del SI. |
| L | Procesos que soporta del mapa institucional | MODIFICAR | Catálogo_SI → Procesos_institucionales_soportados | Debe quedar como referencia al proceso institucional. |
| M | Módulos / Componentes | MOVER_A_COMPONENTES | Componentes / Ficha | Relación repetible que debe normalizarse. |
| N | Entradas (Inputs) | MOVER_A_FICHA | Ficha | Detalle funcional amplio, no de portafolio. |
| O | Salidas (Outputs) | MOVER_A_FICHA | Ficha | Ídem anterior. |
| P | Sistemas con los que se integra | MOVER_A_INTEGRACIONES | Integraciones_Interfaces | Relación repetible. |
| Q | Tipo de integración | MOVER_A_INTEGRACIONES | Integraciones_Interfaces | Debe describirse por integración, no como texto agregado. |
| R | Interopera con entidades externas | MODIFICAR | Catálogo_SI → Interopera_con_entidades_externas | Se conserva solo el resumen Sí/No. |
| S | Entidades externas integradas | MOVER_A_INTEGRACIONES | Integraciones_Interfaces | Relación repetible por contraparte externa. |
| T | Zona de arquitectura de referencia | MOVER_A_FICHA | Ficha | Dato útil de arquitectura, pero no imprescindible en portafolio. |
| U | Modelo de despliegue | MANTENER | Catálogo_SI | Resume riesgo/operación. |
| V | Tipo de arquitectura | MOVER_A_FICHA | Ficha | Importa al expediente técnico más que al catálogo. |
| W | Sistema operativo | MOVER_A_FICHA | Ficha / Componentes | Demasiado técnico para el catálogo principal. |
| X | Lenguaje de programación | MOVER_A_FICHA | Ficha / Componentes | Ídem anterior. |
| Y | Plataforma de base de datos | MOVER_A_COMPONENTES | Componentes / Ficha | Debe quedar como componente o detalle técnico. |
| Z | Está contenerizado? | MOVER_A_COMPONENTES | Componentes / Ficha | Dato de implementación, no de portafolio. |
| AA | Tecnología de Contenedores | MOVER_A_COMPONENTES | Componentes / Ficha | Detalle técnico. |
| AB | Ruta al Dockerfile | ELIMINAR | No aplica | Ruta operativa demasiado específica para el instrumento. |
| AC | ¿Tiene despliegue continuo? | MOVER_A_FICHA | Ficha | Relevante para operación técnica, no para inventario consolidado. |
| AD | Herramienta de CI/CD | MOVER_A_FICHA | Ficha | Detalle DevOps. |
| AE | Ruta al pipeline | ELIMINAR | No aplica | Demasiado específica y volátil. |
| AF | Estado actual de la solución | MODIFICAR | Catálogo_SI → Estado_del_SI | Se conserva con nombre preciso. |
| AG | Versión actual | MANTENER | Catálogo_SI | Sigue siendo útil para seguimiento. |
| AH | Fecha de salida a producción | MANTENER | Catálogo_SI | Dato de ciclo de vida clave. |
| AI | Fecha de última actualización | MOVER_A_FICHA | Ficha | Detalle de operación; no imprescindible en la vista consolidada. |
| AJ | Tipo de desarrollo | MODIFICAR | Catálogo_SI → Tipo_de_desarrollo_adquisicion | Se conserva con mejor precisión conceptual. |
| AK | Fabricante / Proveedor | MODIFICAR | Catálogo_SI → Fabricante_o_proveedor_principal | Dato contractual resumido útil. |
| AL | Soporte técnico: ¿con quién? | MOVER_A_FICHA | Ficha | El detalle del soporte va en Ficha; el catálogo retiene fecha/estado. |
| AM | Soporte vence en | MODIFICAR | Catálogo_SI → Soporte_vigente_hasta | Campo crítico para alertas. |
| AN | Tipo de licenciamiento | MANTENER | Catálogo_SI | Aporta a decisiones de costo y riesgo. |
| AO | Estado de los ANS (Acuerdo de Nivel de Servicio) | MODIFICAR | Catálogo_SI → Estado_ANS_terceros | Solo aplica cuando hay terceros. |
| AP | Objetivos estratégicos que apoya | MANTENER | Catálogo_SI | Útil para valorar el SI. |
| AQ | Marco legal mandatorio | MODIFICAR | Catálogo_SI → Marco_legal_mandatorio | Mantener solo la referencia principal. |
| AR | Nivel de criticidad operacional | MANTENER | Catálogo_SI | Clave para priorización. |
| AS | Cantidad de usuarios activos | MANTENER | Catálogo_SI | Útil para cobertura y costo relativo. |
| AT | Nivel de cobertura del proceso | MANTENER | Catálogo_SI | Útil para análisis del portafolio. |
| AU | Clasificación de la información | MANTENER | Catálogo_SI | Requisito de cumplimiento. |
| AV | Manejo de datos personales | MANTENER | Catálogo_SI | Requisito de cumplimiento. |
| AW | Área responsable técnico | MODIFICAR | Catálogo_SI → Area_responsable_tecnica | Se conserva. |
| AX | Nombre responsable técnico | MODIFICAR | Catálogo_SI → Responsable_tecnico | Se conserva. |
| AY | Correo responsable técnico | MOVER_A_FICHA | Ficha | Dato de contacto, no necesario en tablero principal. |
| AZ | Área responsable funcional | MODIFICAR | Catálogo_SI → Area_responsable_funcional | Se conserva. |
| BA | Nombre responsable funcional | MODIFICAR | Catálogo_SI → Responsable_funcional | Se conserva. |
| BB | Correo responsable funcional | MOVER_A_FICHA | Ficha | Dato de contacto, no de comparación. |
| BC | Fortalezas | MOVER_A_FICHA | Ficha | El DOFA pertenece al expediente analítico. |
| BD | Debilidades | MOVER_A_FICHA | Ficha | Ídem anterior. |
| BE | Oportunidades de mejora | MOVER_A_FICHA | Ficha | Ídem anterior. |
| BF | Amenazas | MOVER_A_FICHA | Ficha | Ídem anterior. |
| BG | Incidentes reportados (12M) | MOVER_A_FICHA | Ficha | Importa al análisis detallado; el catálogo final ya resume por TIME/riesgo. |
| BH | Riesgos tecnológicos identificados | MOVER_A_FICHA | Ficha | Debe tratarse en el expediente técnico. |
| BI | Nivel de madurez | MOVER_A_FICHA | Ficha | Mejor como análisis detallado. |
| BJ | Nivel de satisfacción | MOVER_A_FICHA | Ficha | Detalle evaluativo, no imprescindible en portafolio. |
| BK | TIME - Eje Valor al negocio (0-3) | MOVER_A_FICHA | Ficha | Conservar método, no saturar catálogo. |
| BL | TIME - Eje Eficiencia técnica (0-3) | MOVER_A_FICHA | Ficha | Ídem anterior. |
| BM | TIME - Eje Costos y riesgos (0-3) | MOVER_A_FICHA | Ficha | Ídem anterior. |
| BN | Clasificación TIME | MANTENER | Catálogo_SI | Síntesis estratégica indispensable. |
| BO | Tipo de intervención recomendada | MANTENER | Catálogo_SI | Convierte TIME en acción. |
| BP | Evolución prevista | MOVER_A_FICHA | Ficha | Planeación detallada mejor en expediente. |
| BQ | TCO Licenciamiento anual (COP) | MOVER_A_FICHA | Ficha | Insumo detallado del TCO. |
| BR | TCO Soporte y mantenimiento (COP) | MOVER_A_FICHA | Ficha | Insumo detallado del TCO. |
| BS | TCO Infraestructura asociada (COP) | MOVER_A_FICHA | Ficha | Insumo detallado del TCO. |
| BT | TCO Mantenimiento evolutivo (COP) | MOVER_A_FICHA | Ficha | Insumo detallado del TCO. |
| BU | TCO Mantenimiento correctivo (COP) | MOVER_A_FICHA | Ficha | Insumo detallado del TCO. |
| BV | TCO TOTAL ANUAL(COP) | MODIFICAR | Catálogo_SI → TCO_anual_total_COP | Se conserva solo el total consolidado. |
| BW | Ratio TCO por usuario (COP) | CALCULAR | Catálogo_SI → Ratio_TCO_por_usuario_COP | Debe derivarse del total y usuarios. |
| BX | Doc - Manual técnico | MOVER_A_FICHA | Ficha | Mantener el estado detallado por documento en Ficha. |
| BY | Ubicación repositorio | MOVER_A_FICHA | Ficha | Ubicaciones documentales detalladas van en Ficha. |
| BZ | Doc - Manual de usuario | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CA | Ubicación repositorio2 | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CB | Doc - Manual de operación | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CC | Ubicación repositorio3 | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CD | Doc - Requerimientos (SRS) | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CE | Ubicación repositorio4 | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CF | Doc - Arquitectura de solución | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CG | Ubicación repositorio5 | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CH | Doc - Plan de pruebas | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CI | Ubicación repositorio6 | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CJ | Doc - Plan de mantenimiento | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CK | Fecha de cargue al catálogo | MOVER_A_OTRO_ARTEFACTO | Calidad | Trazabilidad operativa del libro. |
| CL | Versión de la Ficha origen | MOVER_A_OTRO_ARTEFACTO | Calidad | Dato de control documental, no del SI. |
| CM | Última revisión anual | MANTENER | Catálogo_SI | Sirve para vigencia y alertas. |
| CN | Observaciones | MOVER_A_OTRO_ARTEFACTO | Calidad / Ficha | Las observaciones generales deben quedar donde se gestionan. |
| CO | Vigencia del registro | MANTENER | Catálogo_SI | Preserva histórico sin borrar. |
| CP | Prioridad de diligenciamiento asignada | MOVER_A_OTRO_ARTEFACTO | Calidad | Gestiona cierre documental, no portafolio. |
| CQ | % Avance campos obligatorios (P1) | MOVER_A_OTRO_ARTEFACTO | Calidad | Indicador de calidad de diligenciamiento. |
| CR | Tipo de mantenimiento recomendado | MOVER_A_FICHA | Ficha | Insumo detallado del plan de mantenimiento. |
| CS | Periodicidad de mantenimiento sugerida | MOVER_A_FICHA | Ficha | Ídem anterior. |
| CT | Próxima fecha de revisión programada | MODIFICAR | Catálogo_SI → Proxima_revision_programada | Mantener solo la próxima revisión ejecutiva. |
| CU | Prioridad de intervención (calculada) | MODIFICAR | Catálogo_SI → Prioridad_intervencion | Resumen útil para portafolio. |

## 8. Resultado de la Fase 2

Se cierra que el futuro F-A-GTI-02 debe ser un libro de **7 hojas** con un **Catálogo_SI de 44 columnas** y dos hojas normalizadas de apoyo (`Integraciones_Interfaces` y `Componentes`).
