---
title: "F-A-GTI-02 V4 — Catálogo Institucional de Sistemas de Información y Soluciones Tecnológicas"
source_file: "F-A-GTI-02_V4_Propuesta_Catalogo_Soluciones_Tecnologicas.xlsx"
conversion: semantic-markdown
note: "Exportación optimizada para IA: conserva estructura, campos, vocabularios, fórmulas relevantes, hallazgos y datos visibles; omite formato visual y repeticiones vacías."
---

# 1. Resumen estructural

| # | Hoja |
| --- | --- |
| 1 | Instrucciones |
| 2 | Catálogo |
| 3 | Diccionario |
| 4 | Listas |
| 5 | Tablero |
| 6 | Alertas Caducidad |
| 7 | Log de Calidad |
| 8 | Control de Cambios |
| 9 | Hoja2 |
| 10 | Avance por Dependencia |

# 2. Hoja: Instrucciones

## CATÁLOGO INSTITUCIONAL DE SOLUCIONES TECNOLÓGICAS

F-A-GTI-02 · Versión 3 · Ministerio de Ambiente y Desarrollo Sostenible — OTIC

Propósito de este catálogo

Este libro consolida la caracterización de todas las soluciones tecnológicas del Ministerio. Es la fuente única de verdad del portafolio de TI y se alimenta de las Fichas F-A-GTI-01 firmadas. Cumple con el lineamiento MGGTI.LI.SI.02 de MinTIC (Marco de Gestión y Gobierno de TI, 2023).

Estructura del libro (8 hojas)

## 1. Instrucciones — esta hoja.

## 2. Catálogo — registro consolidado de soluciones (una fila por solución).

## 3. Diccionario — definición de cada columna del Catálogo, con tipo y vocabulario.

## 4. Listas — vocabularios controlados que alimentan las listas desplegables del Catálogo.

## 5. Tablero — indicadores agregados del portafolio (TIME, TCO, vencimientos).

## 6. Alertas Caducidad — semáforo de vencimientos de soporte con lógica robusta.

## 7. Log de Calidad — registro de inconsistencias detectadas y su trazabilidad.

## 8. Control de Cambios — historial de versiones del catálogo.

Cómo registrar una nueva solución

Paso 1. Asegúrese de que la Ficha F-A-GTI-01 V7 esté diligenciada, firmada y archivada.

Paso 2. Asigne un ID siguiendo el patrón institucional: SYS-NNNN sistemas · APP-NNNN aplicaciones · INT-NNNN integraciones · BI-NNNN analíticas · PLT-NNNN plataformas · SRV-NNNN servicios · HT-NNNN herramientas transversales · CMP-NNNN componentes.

Paso 3. En la hoja Catálogo, agregue una nueva fila al final con el ID y vaya completando las columnas. Las celdas con lista desplegable bloquean valores fuera del vocabulario.

Paso 4. Diligencie primero G1-Naturaleza; la lista de Tipo Detallado se filtra automáticamente.

Paso 5. Las fechas SIEMPRE en formato fecha real (DD/MM/AAAA). Nunca como número serial ni como texto.

Paso 6. Para el TCO use pesos colombianos sin separadores ni decimales (ej. 45000000).

Paso 7. Revise la hoja Log de Calidad: si su fila tiene marca roja, corrija antes de cerrar.

Reglas de calidad — qué NO hacer

✗ No use placeholders como «XXXX», «xxxx», «N/A» sin justificación. Use «Pendiente de verificación».

✗ No deje fechas en blanco si la fase de diligenciamiento es «Completa».

✗ No escriba texto libre en columnas con vocabulario controlado: el catálogo lo rechaza.

✗ No marque «Completa» como fase si faltan campos obligatorios; eso confunde el tablero.

✗ No edite la hoja Listas sin validar con la OTIC: cambia el vocabulario para todas las fichas.

Trazabilidad

Cada columna de este Catálogo tiene correspondencia 1:1 con un campo de la Ficha F-A-GTI-01. La tabla maestra de correspondencia está en la Sección 9 de la Guía G-A-GTI-01 y replicada en la hoja Diccionario de este libro. Si hay diferencia entre la Ficha firmada y el Catálogo, prevalece la Ficha y se levanta un hallazgo en el Log de Calidad.

NOVEDADES DE LA VERSIÓN 4 (Propuesta)

Esta versión ajusta la ejecución del catálogo, no su diseño: la V3 ya cumplía y superaba el lineamiento LI.SIS.02 de MinTIC. Los cambios de la V4 son los siguientes.

## 1. Corrección de un defecto crítico

Las hojas Tablero y Alertas Caducidad solo cubrían las filas 6 a 55 del Catálogo (50 soluciones). Con 129 soluciones ya registradas, el 61% del portafolio no aparecía en los indicadores ni en el semáforo de vencimientos. Se extendieron todos los rangos hasta la fila 305 (con margen para crecimiento futuro).

## 2. Priorización visual de campos (P1 / P2 / Automático)

Los encabezados de columna del Catálogo ahora tienen color: verde = campo obligatorio prioritario (P1, diligéncielo primero para las 129 soluciones existentes); durazno = campo recomendado o condicional de segunda ola (P2, se completa después, ligado a los hitos del procedimiento P-A-GTI-03); azul = campo automático/calculado, no se diligencia manualmente.

## 3. Vigencia del registro — preservación del histórico

REGLA DE ORO: nunca elimine filas de soluciones con Estado «Retirado». Son el histórico institucional de desarrollos y deben conservarse para trazabilidad. La nueva columna «Vigencia del registro» (G11) clasifica automáticamente cada fila como «Activo en gestión» o «Histórico - conservar» según el Estado actual, para poder filtrar las vistas operativas sin borrar nada.

## 4. Gestión del diligenciamiento por dependencia

La nueva columna «Prioridad de diligenciamiento asignada» (G11) permite marcar cada solución como 1-Prioritaria, 2-Programada o 3-Diferida, para organizar el cierre de brechas dependencia por dependencia. La nueva hoja «Avance por Dependencia» resume el avance agregado por cada área, para hacer seguimiento del antes y el después.

## 5. % de avance en vez de estado binario

La columna «% Avance campos obligatorios (P1)» calcula automáticamente qué porcentaje de los 45 campos obligatorios (P1) tiene diligenciados cada solución. Reemplaza la lógica de todo-o-nada de «Fase de diligenciamiento» con una medida de progreso real.

## 6. Grupo G12 — Seguridad y Continuidad (campo nuevo)

Se agregó valoración de riesgo de seguridad (MSPI/ISO 27001), accesibilidad web (NTC 5854/WCAG) para sistemas de cara al ciudadano, y continuidad (backup, RTO, RPO, plan de contingencia). Estos aspectos no estaban cubiertos en la V3 pese a existir la sección de ANS.

## 7. Grupo G13 — Insumos para el Plan de Mantenimiento de Sistemas de Información

Estos 4 campos son el puente hacia el futuro Plan de Mantenimiento: tipo de mantenimiento recomendado, periodicidad sugerida, próxima fecha de revisión, y una «Prioridad de intervención» calculada automáticamente combinando Criticidad + Clasificación TIME + vencimiento de soporte. Recomendación: inicie la construcción del Plan de Mantenimiento cuando el portafolio ACTIVO alcance ≥80% de avance promedio en campos P1 (ver hoja Tablero, sección 6).

## 8. Campos recuperados del Diccionario original (G10)

«Dependencia ejecutora», «Número de registro RNBD» y «Monitoreo activo» estaban documentados en el Diccionario de la V3 pero no existían como columnas en el Catálogo. Se restauraron al final del libro para no alterar el orden de las 129 filas ya diligenciadas.

## 9. Corrección de encabezado

El encabezado de la hoja Catálogo mostraba «Versión: 2» y «Código: F-A-GTI-15» (residuo de una versión anterior) en lugar de «Versión: 3/4» y «Código: F-A-GTI-02». Corregido.

# 3. Hoja: Catálogo

Versión: 4. Vigencia: 01/07/2026.
La hoja principal contiene 99 columnas (A:CU). En esta V4 el rango usado llega a la fila 5; no hay registros cargados debajo de los encabezados en la hoja principal.

## 3.1 Campos del Catálogo

| Columna | Grupo | Campo |
| --- | --- | --- |
| A | G1 — IDENTIFICACIÓN | ID Solución |
| B | G1 — IDENTIFICACIÓN | Nombre oficial de la solución |
| C | G1 — IDENTIFICACIÓN | Sigla / Acrónimo |
| D | G1 — IDENTIFICACIÓN | Naturaleza (N1-N8) |
| E | G1 — IDENTIFICACIÓN | Tipo detallado |
| F | G1 — IDENTIFICACIÓN | Categoría institucional |
| G | G1 — IDENTIFICACIÓN | Descripción de la solución |
| H | G1 — IDENTIFICACIÓN | Funcionalidades principales |
| I | G1 — IDENTIFICACIÓN | Dependencia dueña del proceso |
| J | G1 — IDENTIFICACIÓN | No. iniciativa / proyecto origen |
| K | G1 — IDENTIFICACIÓN | Fase de diligenciamiento de la ficha |
| L | G2 — ARQUITECTURA Y DESPLIEGUE | Procesos que soporta del mapa institucional |
| M | G2 — ARQUITECTURA Y DESPLIEGUE | Módulos / Componentes |
| N | G2 — ARQUITECTURA Y DESPLIEGUE | Entradas (Inputs) |
| O | G2 — ARQUITECTURA Y DESPLIEGUE | Salidas (Outputs) |
| P | G2 — ARQUITECTURA Y DESPLIEGUE | Sistemas con los que se integra |
| Q | G2 — ARQUITECTURA Y DESPLIEGUE | Tipo de integración |
| R | G2 — ARQUITECTURA Y DESPLIEGUE | Interopera con entidades externas |
| S | G2 — ARQUITECTURA Y DESPLIEGUE | Entidades externas integradas |
| T | G2 — ARQUITECTURA Y DESPLIEGUE | Zona de arquitectura de referencia |
| U | G2 — ARQUITECTURA Y DESPLIEGUE | Modelo de despliegue |
| V | G2 — ARQUITECTURA Y DESPLIEGUE | Tipo de arquitectura |
| W | G2 — ARQUITECTURA Y DESPLIEGUE | Sistema operativo |
| X | G2 — ARQUITECTURA Y DESPLIEGUE | Lenguaje de programación |
| Y | G2 — ARQUITECTURA Y DESPLIEGUE | Plataforma de base de datos |
| Z | G2 — ARQUITECTURA Y DESPLIEGUE | Está contenerizado? |
| AA | G2 — ARQUITECTURA Y DESPLIEGUE | Tecnología de Contenedores |
| AB | G2 — ARQUITECTURA Y DESPLIEGUE | Ruta al Dockerfile |
| AC | G2 — ARQUITECTURA Y DESPLIEGUE | ¿Tiene despliegue continuo? |
| AD | G2 — ARQUITECTURA Y DESPLIEGUE | Herramienta de CI/CD |
| AE | G2 — ARQUITECTURA Y DESPLIEGUE | Ruta al pipeline |
| AF | G3 — CICLO DE VIDA Y SOPORTE | Estado actual de la solución |
| AG | G3 — CICLO DE VIDA Y SOPORTE | Versión actual |
| AH | G3 — CICLO DE VIDA Y SOPORTE | Fecha de salida a producción |
| AI | G3 — CICLO DE VIDA Y SOPORTE | Fecha de última actualización |
| AJ | G3 — CICLO DE VIDA Y SOPORTE | Tipo de desarrollo |
| AK | G3 — CICLO DE VIDA Y SOPORTE | Fabricante / Proveedor |
| AL | G3 — CICLO DE VIDA Y SOPORTE | Soporte técnico: ¿con quién? |
| AM | G3 — CICLO DE VIDA Y SOPORTE | Soporte vence en |
| AN | G3 — CICLO DE VIDA Y SOPORTE | Tipo de licenciamiento |
| AO | G3 — CICLO DE VIDA Y SOPORTE | Estado de los ANS (Acuerdo de Nivel de Servicio) |
| AP | G4 — VALOR Y GOBIERNO DE DATOS | Objetivos estratégicos que apoya |
| AQ | G4 — VALOR Y GOBIERNO DE DATOS | Marco legal mandatorio |
| AR | G4 — VALOR Y GOBIERNO DE DATOS | Nivel de criticidad operacional |
| AS | G4 — VALOR Y GOBIERNO DE DATOS | Cantidad de usuarios activos |
| AT | G4 — VALOR Y GOBIERNO DE DATOS | Nivel de cobertura del proceso |
| AU | G4 — VALOR Y GOBIERNO DE DATOS | Clasificación de la información |
| AV | G4 — VALOR Y GOBIERNO DE DATOS | Manejo de datos personales |
| AW | G5 — RESPONSABILIDAD | Área responsable técnico |
| AX | G5 — RESPONSABILIDAD | Nombre responsable técnico |
| AY | G5 — RESPONSABILIDAD | Correo responsable técnico |
| AZ | G5 — RESPONSABILIDAD | Área responsable funcional |
| BA | G5 — RESPONSABILIDAD | Nombre responsable funcional |
| BB | G5 — RESPONSABILIDAD | Correo responsable funcional |
| BC | G6 — CALIDAD Y TIME | Fortalezas |
| BD | G6 — CALIDAD Y TIME | Debilidades |
| BE | G6 — CALIDAD Y TIME | Oportunidades de mejora |
| BF | G6 — CALIDAD Y TIME | Amenazas |
| BG | G6 — CALIDAD Y TIME | Incidentes reportados (12M) |
| BH | G6 — CALIDAD Y TIME | Riesgos tecnológicos identificados |
| BI | G6 — CALIDAD Y TIME | Nivel de madurez |
| BJ | G6 — CALIDAD Y TIME | Nivel de satisfacción |
| BK | G6 — CALIDAD Y TIME | TIME - Eje Valor al negocio (0-3) |
| BL | G6 — CALIDAD Y TIME | TIME - Eje Eficiencia técnica (0-3) |
| BM | G6 — CALIDAD Y TIME | TIME - Eje Costos y riesgos (0-3) |
| BN | G6 — CALIDAD Y TIME | Clasificación TIME |
| BO | G6 — CALIDAD Y TIME | Tipo de intervención recomendada |
| BP | G6 — CALIDAD Y TIME | Evolución prevista |
| BQ | G7 — DIMENSIÓN ECONÓMICA (TCO) | TCO Licenciamiento anual (COP) |
| BR | G7 — DIMENSIÓN ECONÓMICA (TCO) | TCO Soporte y mantenimiento (COP) |
| BS | G7 — DIMENSIÓN ECONÓMICA (TCO) | TCO Infraestructura asociada (COP) |
| BT | G7 — DIMENSIÓN ECONÓMICA (TCO) | TCO Mantenimiento evolutivo (COP) |
| BU | G7 — DIMENSIÓN ECONÓMICA (TCO) | TCO Mantenimiento correctivo (COP) |
| BV | G7 — DIMENSIÓN ECONÓMICA (TCO) | TCO TOTAL ANUAL(COP) |
| BW | G7 — DIMENSIÓN ECONÓMICA (TCO) | Ratio TCO por usuario (COP) |
| BX | G8 — DOCUMENTACIÓN | Doc - Manual técnico |
| BY | G8 — DOCUMENTACIÓN | Ubicación repositorio |
| BZ | G8 — DOCUMENTACIÓN | Doc - Manual de usuario |
| CA | G8 — DOCUMENTACIÓN | Ubicación repositorio2 |
| CB | G8 — DOCUMENTACIÓN | Doc - Manual de operación |
| CC | G8 — DOCUMENTACIÓN | Ubicación repositorio3 |
| CD | G8 — DOCUMENTACIÓN | Doc - Requerimientos (SRS) |
| CE | G8 — DOCUMENTACIÓN | Ubicación repositorio4 |
| CF | G8 — DOCUMENTACIÓN | Doc - Arquitectura de solución |
| CG | G8 — DOCUMENTACIÓN | Ubicación repositorio5 |
| CH | G8 — DOCUMENTACIÓN | Doc - Plan de pruebas |
| CI | G8 — DOCUMENTACIÓN | Ubicación repositorio6 |
| CJ | G8 — DOCUMENTACIÓN | Doc - Plan de mantenimiento |
| CK | G9 — AUDITORÍA | Fecha de cargue al catálogo |
| CL | G9 — AUDITORÍA | Versión de la Ficha origen |
| CM | G9 — AUDITORÍA | Última revisión anual |
| CN | G9 — AUDITORÍA | Observaciones |
| CO | G11 — AVANCE Y VIGENCIA DEL REGISTRO | Vigencia del registro |
| CP | G11 — AVANCE Y VIGENCIA DEL REGISTRO | Prioridad de diligenciamiento asignada |
| CQ | G11 — AVANCE Y VIGENCIA DEL REGISTRO | % Avance campos obligatorios (P1) |
| CR | G13 — INSUMOS PARA PLAN DE MANTENIMIENTO | Tipo de mantenimiento recomendado |
| CS | G13 — INSUMOS PARA PLAN DE MANTENIMIENTO | Periodicidad de mantenimiento sugerida |
| CT | G13 — INSUMOS PARA PLAN DE MANTENIMIENTO | Próxima fecha de revisión programada |
| CU | G13 — INSUMOS PARA PLAN DE MANTENIMIENTO | Prioridad de intervención (calculada) |

# 4. Hoja: Diccionario

El diccionario declara trazabilidad Ficha ↔ Catálogo y documenta columnas hasta DA, aunque la hoja Catálogo física termina en CU.

| Col | Grupo | Columna en Catálogo | Tipo de dato | Vocabulario / Formato | Sección Ficha | Obligatoriedad | Origen |
| --- | --- | --- | --- | --- | --- | --- | --- |
| A | G1 | ID Solución | Texto | Patrón [PFX]-NNNN | 1 | Sí | C |
| B | G1 | Nombre oficial | Texto | Texto libre | 1 | Sí | F |
| C | G1 | Sigla / Acrónimo | Texto | Sin puntos | 1 | Sí | F |
| D | G1 | Naturaleza (N1-N8) | Lista | 8 valores controlados | 1 | Sí | C |
| E | G1 | Tipo detallado | Lista | Filtrada por Naturaleza | 1 | Sí | T |
| F | G1 | Categoría institucional | Lista | 5 valores | 1 | Sí | F |
| G | G1 | Descripción | Texto | ≤ 10 líneas | 1 | Sí | F |
| H | G1 | Dependencia dueña del proceso | Lista | Lista de dependencias | 1 | Sí | F |
| I | G1 | Dependencia ejecutora | Lista | Lista de dependencias | 1 | Reco | C |
| J | G1 | No. iniciativa / proyecto origen | Texto | Código o «Preexistente» | 1 | Reco | C |
| K | G1 | Fase de diligenciamiento | Lista | 4 valores controlados | 1 | Sí | C |
| L | G2 | Procesos del mapa institucional | Texto | Códigos P-NN separados por ; | 2 | Sí | F |
| M | G2 | Módulos / Componentes | Texto | Texto libre | 2 | Reco | T |
| N | G2 | Entradas (Inputs) | Texto | Texto libre | 2 | Sí | T |
| O | G2 | Salidas (Outputs) | Texto | Texto libre | 2 | Sí | T |
| P | G2 | Sistemas con los que se integra | Texto | Lista de IDs | 2 | Reco | T |
| Q | G2 | Tipo de integración | Texto | Protocolo + dirección | 2 | Reco | T |
| R | G2 | Interopera con entidades externas | Lista | Sí / No | 2 | Sí | T |
| S | G2 | Entidades externas integradas | Texto | Lista de entidades | 2 | Cond. | T |
| T | G2 | Zona de arquitectura de referencia | Lista | 7 zonas Blueprint | 2 | Reco | T |
| U | G2 | Modelo de despliegue | Lista | 7 valores | 2 | Sí | T |
| V | G2 | Tipo de arquitectura | Lista | 7 valores | 2 | Reco | T |
| W | G2 | Sistema operativo | Texto | SO + versión | 2 | Reco | T |
| X | G2 | Lenguaje de programación | Texto | Lenguaje + versión | 2 | Reco | T |
| Y | G2 | Plataforma de base de datos | Texto | Motor + versión | 2 | Reco | T |
| Z | G3 | Estado actual | Lista | 6 valores controlados | 3 | Sí | T |
| AA | G3 | Versión actual | Texto | Mayor.Menor.Parche | 3 | Reco | T |
| AB | G3 | Fecha puesta en producción | Fecha | DD/MM/AAAA | 3 | Sí | T |
| AC | G3 | Fecha última actualización | Fecha | DD/MM/AAAA | 3 | Reco | T |
| AD | G3 | Tipo de desarrollo | Lista | 6 valores | 3 | Sí | T |
| AE | G3 | Fabricante | Texto | Texto libre | 3 | Sí | T |
| AF | G3 | Proveedor de soporte | Texto | Texto libre | 3 | Sí | $ |
| AG | G3 | Vencimiento del soporte | Fecha | DD/MM/AAAA | 3 | Sí | $ |
| AH | G3 | Licenciamiento | Lista | 8 valores | 3 | Sí | $ |
| AI | G3 | Estado del ANS | Lista | 4 valores | 3 | Sí | $ |
| AJ | G3 | Indicadores del ANS | Texto | Métricas estructuradas | 3 | Reco | $ |
| AK | G4 | Objetivos estratégicos que soporta | Texto | Códigos PEI | 4 | Reco | F |
| AL | G4 | Marco legal aplicable | Texto | Norma + año + tema | 4 | Reco | F |
| AM | G4 | Nivel de criticidad operacional | Lista | Alta / Media / Baja | 4 | Sí | F |
| AN | G4 | Cantidad de usuarios activos | Número | Entero ≥ 0 | 4 | Reco | F |
| AO | G4 | Nivel de cobertura del proceso | Lista | 4 valores | 4 | Cond. | F |
| AP | G4 | Clasificación de la información | Lista | 4 valores Ley 1712 | 4 | Sí | F |
| AQ | G4 | Manejo de datos personales | Lista | 3 valores Ley 1581 | 4 | Sí | F |
| AR | G4 | Número de registro RNBD | Texto | Si maneja datos personales | 4 | Cond. | F |
| AS | G5 | Área responsable técnico | Lista | Lista de dependencias | 5 | Sí | T |
| AT | G5 | Nombre responsable técnico | Texto | Nombre + cargo | 5 | Sí | T |
| AU | G5 | Correo responsable técnico | Texto | @minambiente.gov.co | 5 | Reco | T |
| AV | G5 | Área responsable funcional | Lista | Lista de dependencias | 5 | Sí | F |
| AW | G5 | Nombre responsable funcional | Texto | Nombre + cargo | 5 | Sí | F |
| AX | G5 | Correo responsable funcional | Texto | @minambiente.gov.co | 5 | Reco | F |
| AY | G6 | Fortalezas | Texto | DOFA — condicional N1/N2/N5/N7 | 6 | Cond. | F |
| AZ | G6 | Debilidades | Texto | DOFA — condicional | 6 | Cond. | F |
| BA | G6 | Oportunidades de mejora | Texto | DOFA — condicional | 6 | Cond. | F |
| BB | G6 | Amenazas | Texto | DOFA — condicional | 6 | Cond. | T |
| BC | G6 | Incidentes reportados (12M) | Número | Entero ≥ 0 | 6 | Sí | T |
| BD | G6 | Riesgos tecnológicos | Texto | Texto libre | 6 | Sí | T |
| BE | G6 | Nivel de madurez | Lista | 4 valores | 6 | Reco | C |
| BF | G6 | Nivel de satisfacción | Lista | 4 valores | 6 | Reco | F |
| BG | G6 | Monitoreo activo | Lista | Sí / No | 6 | Reco | T |
| BH | G6 | TIME — Eje Valor (0-3) | Número | 0 a 3 | 6 | Sí | C |
| BI | G6 | TIME — Eje Eficiencia (0-3) | Número | 0 a 3 | 6 | Sí | C |
| BJ | G6 | TIME — Eje Costos (0-3) | Número | 0 a 3 | 6 | Sí | C |
| BK | G6 | Clasificación TIME | Lista | I / T / M / E | 6 | Sí | C |
| BL | G6 | Tipo de intervención recomendada | Texto | Acción + plazo | 6 | Sí | C |
| BM | G6 | Evolución prevista | Texto | 1-3 años | 6 | Reco | C |
| BN | G7 | TCO Licenciamiento (COP) | Número | Entero, sin separadores | 7 | Reco | $ |
| BO | G7 | TCO Soporte (COP) | Número | Entero | 7 | Reco | $ |
| BP | G7 | TCO Infraestructura (COP) | Número | Entero | 7 | Reco | $ |
| BQ | G7 | TCO Evolutivo (COP) | Número | Entero | 7 | Reco | $ |
| BR | G7 | TCO Correctivo (COP) | Número | Entero | 7 | Reco | $ |
| BU | G7 | TCO ANUAL TOTAL (COP) | Fórmula | Calculada: SUMA(BN:BT) | 7 | Sí | Calc |
| BV | G7 | TCO por usuario (COP) | Fórmula | Calculada: BU / AN | 7 | Reco | Calc |
| BW | G8 | Doc — Manual técnico | Lista | Vigente/Desactualizado/No Existe | 8 | Sí | T |
| BX | G8 | Doc — Manual de usuario | Lista | 3 valores | 8 | Sí | F |
| BY | G8 | Doc — Manual de operación | Lista | 3 valores | 8 | Sí | T |
| BZ | G8 | Doc — Requerimientos (SRS) | Lista | 3 valores | 8 | Reco | T |
| CA | G8 | Doc — Arquitectura de solución | Lista | 3 valores | 8 | Reco | T |
| CB | G8 | Doc — Plan de pruebas | Lista | 3 valores | 8 | Reco | T |
| CC | G8 | Doc — Plan de mantenimiento | Lista | 3 valores | 8 | Reco | T |
| CD | G9 | Fecha de cargue al catálogo | Fecha | DD/MM/AAAA | 9 | Sí | C |
| CE | G9 | Versión de la Ficha origen | Texto | Ej.: 1.2 | 9 | Sí | C |
| CF | G9 | Última revisión anual | Fecha | DD/MM/AAAA | 9 | Reco | C |
| CAMPOS AÑADIDOS EN LA PROPUESTA V4 (grupos G10-G13) |  |  |  |  |  |  |  |
| Col | Grupo | Columna en Catálogo | Tipo de dato | Vocabulario / Formato | Sección Ficha | Obligatoriedad | Origen |
| CJ | G10 | Dependencia ejecutora | Lista | Lista de dependencias | Nuevo V4 | Reco | F |
| CK | G10 | Número de registro RNBD | Texto | Solo si maneja datos personales | Nuevo V4 | Cond. | F |
| CL | G10 | Monitoreo activo | Lista | Sí / No | Nuevo V4 | Reco | T |
| CM | G11 | Vigencia del registro | Fórmula | Auto: Activo en gestión / Histórico - conservar | Nuevo V4 | Calc | Calc |
| CN | G11 | Prioridad de diligenciamiento asignada | Lista | 1-Prioritaria / 2-Programada / 3-Diferida | Nuevo V4 | Sí | C |
| CO | G11 | % Avance campos obligatorios (P1) | Fórmula | Auto: % de campos P1 diligenciados | Nuevo V4 | Calc | Calc |
| CP | G12 | Valoración de riesgo de seguridad (MSPI/ISO 27001) | Lista | Vigente/Desactualizada/No realizada | Nuevo V4 | Sí | T |
| CQ | G12 | Nivel de riesgo residual | Lista | Alto/Medio/Bajo/No evaluado | Nuevo V4 | Reco | T |
| CR | G12 | Cumple accesibilidad web (NTC 5854/WCAG) | Lista | Sí/No/No aplica (uso interno) | Nuevo V4 | Cond. | F |
| CS | G12 | Copia de respaldo (backup) definida | Lista | Sí/No/Desconocido | Nuevo V4 | Sí | T |
| CT | G12 | Frecuencia de backup | Texto | Texto libre (ej. Diaria, Semanal) | Nuevo V4 | Reco | T |
| CU | G12 | RTO - Tiempo objetivo de recuperación (horas) | Número | Entero, horas | Nuevo V4 | Reco | T |
| CV | G12 | RPO - Punto objetivo de recuperación (horas) | Número | Entero, horas | Nuevo V4 | Reco | T |
| CW | G12 | Plan de continuidad / contingencia | Lista | Vigente/Desactualizado/No existe | Nuevo V4 | Reco | T |
| CX | G13 | Tipo de mantenimiento recomendado | Lista | Preventivo/Correctivo/Evolutivo/Adaptativo/Ninguno-Evaluar retiro | Nuevo V4 | Reco | C |
| CY | G13 | Periodicidad de mantenimiento sugerida | Lista | Mensual/Trimestral/Semestral/Anual/No aplica | Nuevo V4 | Reco | C |
| CZ | G13 | Próxima fecha de revisión programada | Fecha | DD/MM/AAAA | Nuevo V4 | Reco | C |
| DA | G13 | Prioridad de intervención (calculada) | Fórmula | Auto: Alta/Media/Baja según Criticidad+TIME+Soporte | Nuevo V4 | Calc | Calc |

# 5. Hoja: Listas — vocabularios controlados

Esta hoja contiene las listas que alimentan las validaciones del Catálogo. NO modificar sin autorización OTIC. Cada cambio afecta a todas las fichas.

## Naturaleza

N1 Sistema de información; N2 Aplicación; N3 Componente; N4 Integración; N5 Plataforma; N6 Servicio tecnológico; N7 Solución analítica; N8 Herramienta transversal; Naturaleza; N1 Sistema de información; N1 Sistema de información; N2 Aplicación; N2 Aplicación; N2 Aplicación; N2 Aplicación; N2 Aplicación; N2 Aplicación; N2 Aplicación; N3 Componente; N3 Componente; N3 Componente; N3 Componente; N4 Integración; N4 Integración; N4 Integración; N4 Integración; N4 Integración; N5 Plataforma; N5 Plataforma; N5 Plataforma; N5 Plataforma; N5 Plataforma; N5 Plataforma; N5 Plataforma; N5 Plataforma; N5 Plataforma; N6 Servicio tecnológico; N6 Servicio tecnológico; N7 Solución analítica; N7 Solución analítica; N7 Solución analítica; N7 Solución analítica; N7 Solución analítica; N7 Solución analítica; N8 Herramienta transversal; N8 Herramienta transversal; N8 Herramienta transversal; N8 Herramienta transversal; N8 Herramienta transversal; N8 Herramienta transversal; N8 Herramienta transversal; N8 Herramienta transversal

## Categoria

Estratégica; Misional; Apoyo; Evaluación; Otros; Tipo Detallado; Sistema de Información; Sistema Transaccional; Aplicativo; Portal; Aplicación Web; Aplicación Móvil; Aplicación de Escritorio; Página Web; Micrositio; Base de Datos; Microservicio; Motor de Autenticación; Motor de Reportes; Hub de Integración; Bus de Servicios (ESB); API; Servicio Web; Middleware; Herramientas de Colaboración / Ofimática; Sistema Misional / Core de Negocio; ERP; CRM; Motor de Procesos (BPM); Plataforma de Integración (iPaaS); Repositorio Documental; Gestor de Contenido (CMS); Gestor de Identidad (IAM); SaaS; Herramienta DevOps; Data Warehouse; Data Lake; DataMart; ETL / ELT; Solución BI; Dashboard; Firma Electrónica; Herramienta de Seguridad; Sistema de Monitoreo; Inteligencia Artificial; Chatbot / Asistente Virtual; RPA; Blockchain; IoT

## FaseDiligenciamiento

Preliminar (iniciativa aprobada, sistema aún no en producción); En Diligenciamiento (levantamiento en curso); Completa (sistema en producción, ficha firmada); En Revisión Anual; Desactualizada (requiere actualización urgente)

## EstadoSolucion

Activo; En Migración; En Mantenimiento; En Desarrollo; Deprecado; Retirado; Preproducción; Actualización; N1_Sistema_de_información; Sistema de Información; Sistema Transaccional

## TipoDesarrollo

Desarrollo Propio (In-house); A la Medida (Tercero); COTS; Open Source; SaaS / Cloud Nativo; Híbrido; Desarrollo Propio (In-house) - Dependencias; Desarrollo Propio (In-house) - OTIC - Dependencias; Legado; N2_Aplicación; Aplicativo; Portal; Aplicación Web; Aplicación Móvil; Aplicación de Escritorio; Página Web

## ModeloDespliegue

On-Premises; Nube Pública; Nube Privada; Híbrida; SaaS; PaaS; No Definido; N3_Componente; Base de Datos; Microservicio; Motor de Autenticación; Motor de Reportes

## TipoArquitectura

Monolítico; Microservicios; SOA; Cliente-Servidor; N-Capas; Serverless; No Documentado; N4_Integración; Hub de Integración; Bus de Servicios (ESB); API; Servicio Web; Middleware

## Licenciamiento

Propietario-Perpetuo; Propietario-Suscripción; Open Source-GPL; Open Source-MIT; Open Source-Apache; Freeware; Dominio Público; Sin Definir; N5_Plataforma; ERP; CRM; Motor de Procesos (BPM); Plataforma de Integración (iPaaS); Repositorio Documental; Gestor de Contenido (CMS); Gestor de Identidad (IAM)

## EstadoANS

Vigente; Vencido; No Aplica; En Negociación; N6_Servicio_tecnológico; SaaS; Servicio Cloud; Herramienta DevOps

## Criticidad

Alta; Media; Baja; N7_Solución_analítica; Data Warehouse; Data Lake; DataMart; ETL / ELT; Solución BI; Dashboard; GIS / Georreferenciación

## Cobertura

Alto (>80%); Medio (50-80%); Bajo (<50%); No Evaluado; N8_Herramienta_transversal; Firma Electrónica; Herramienta de Seguridad; Sistema de Monitoreo; Inteligencia Artificial; Chatbot / Asistente Virtual; RPA; Blockchain; IoT

## ClasificacionInfo

Pública; De Uso Interno; Reservada; Clasificada

## DatosPersonales

Sí - Responsable; Sí - Encargado; No

## Madurez

1 Inicial; 2 Gestionado; 3 Definido; 4 Optimizado

## Satisfaccion

Alta (>80%); Media (50-80%); Baja (<50%); No Medida

## TIME

I Invertir; T Tolerar; M Migrar; E Eliminar

## ZonaAR

Canales; Transaccional; Interoperabilidad; Notificaciones; Almacenamiento; Seguridad; Transversal

## InteropExterna

Sí; No

## EstadoDoc

Vigente; Desactualizado; No Existe

## EstadoCosto

C Confirmado; E Estimado

## MonitoreoActivo

Sí; No

## Dependencia

Despacho del Ministro; Grupo de Comunicaciones; Oficina de Negocios Verdes Sostenbiles; Grupo de Análisis Económicos para la Sostenibilidad; Grupo de Competitividad y Promoción de Negocios Sostenibles; Oficina Asesora de Planeación; Grupo de Apoyo Técnico, Evaluación y Seguimiento a Proyectos de Inversión del Sector Ambiental; Grupo de Gestión de Proyectos; Grupo de Gestión y Desempeño Institucional; Grupo de Políticas, Planeación y Seguimiento; Grupo de Programación y Gestión Presupuestal; Oficina Asesora Jurídica; Grupo de Conceptos y Normatividad en Biodiversidad; Grupo de Conceptos y Normatividad en Políticas Sectoriales; Grupo de Procesos Judiciales; Oficina de Asuntos Internacionales; Oficina de Tecnologías de la Información y las Comunicaciones; Oficina de Control Interno; Viceministerio de Politicas y Normalización Ambiental; Dirección de Bosques, Biodiversidad y Servicios Ecosistémicos; Dirección de Asuntos Marinos, Costeros y Recursos Acuáticos; Dirección de Gestión Integral del Recurso Hídrico; Dirección de Asuntos Ambientales, Sectorial y Urbana; Grupo de Gestión Integral de Bosques y Reservas Forestales Nacionales; Grupo de Gestión en Biodiversidad; Grupo de Recursos Genéticos; Dirección de Asuntos Marinos Costeros y Recursos Acuáticos; Grupo de Gestión del Riesgo Información y Participación Comunitaria Marino Costera; Grupo de Ordenamiento Ambiental del Territorio y Gestión Sostenible de la Biodiversidad Costera y Marina; Dirección de Gestión Integral del Recurso Hídrico; Grupo de Administración del Recurso Hídrico; Grupo de Fortalecimiento y Gobernanza del Agua; Grupo de Planificación de Cuencas; DireccióndeAsuntosAmbientalesSectorialyUrbana; Grupo de Gestión Ambiental Urbana; Grupo de Gestión Integral de Residuos y Pasivos Ambientales; Grupo de Producción y Consumo Responsable y Sector Agropecuario; Grupo de Sector Hidrocarburos, Minería y Energéticos; Grupo de Sustancias Químicas, Desechos Peligrosos y Unidad Técnica de Ozono (UTO); Viceministerio de Ordenamiento Ambiental del territorio.; Dirección de Cambio Climático y Gestión del Riesgo; Dirección de Ordenamiento Ambiental Territorial y Sistema Nacional Ambiental SINA; Grupo de Manejo de Información Ambiental Geográfica; Grupo de Ordenamiento Ambiental; Grupo SINA; Subdirección de Educación y Participación; Grupo de Divulgación de Conocimiento y Cultura Ambiental; Grupo de Educación; Grupo de Participación; Grupo Adaptación al Cambio Climático; Grupo de Gestión Integral del Riesgo; Grupo de Mitigación del Cambio Climático; Secretaría General; Grupo de Contratos; Grupo de Control Interno Disciplinario; Grupo de Talento Humano; Unidad Coordinadora para el Gobierno Abierto y Servicio al Ciudadano; Subdirección Administrativa y Financiera; Grupo de Servicios Administrativos; Grupo Central de Cuentas y Contabilidad; Grupo de Comisiones y Apoyo Logístico; Grupo de Gestión Documental; Grupo de Presupuesto; Grupo de Tesorería

## EstáContenerizado?

Sí; No; Desconocido; No aplica (uso interno)

## DespliegueContinuo

Sí; No; Desconocido; No aplica (uso interno)

## PrioridadDiligenciamiento

1 - Prioritaria; 2 - Programada; 3 - Diferida

## ValoracionSeguridad

Vigente; Desactualizada; No realizada

## RiesgoResidual

Alto; Medio; Bajo; No evaluado

## Accesibilidad

Sí; No; No aplica (uso interno)

## BackupDefinido

Sí; No; Desconocido

## PlanContinuidad

Vigente; Desactualizado; No existe

## TipoMantenimiento

Preventivo; Correctivo; Evolutivo; Adaptativo; Ninguno - Evaluar retiro

## PeriodicidadMantenimiento

Mensual; Trimestral; Semestral; Anual; No aplica

# 6. Hoja: Tablero

Se conserva la lógica de fórmulas; las referencias rotas quedan visibles.

| Indicador | Fórmula / valor |
| --- | --- |
| TABLERO DEL PORTAFOLIO DE SOLUCIONES |  |
| Indicadores agregados calculados desde el Catálogo. Se actualizan automáticamente. |  |
| 1. CONTEO GENERAL |  |
| Soluciones registradas | =COUNTA(Catálogo!A6:A304) |
| Soluciones activas | =COUNTIF(Catálogo!AF6:AF304,"Activo") |
| Soluciones retiradas | =COUNTIF(Catálogo!AF6:AF304,"Retirado") |
| En migración | =COUNTIF(Catálogo!AF6:AF304,"En Migración") |
| 2. CLASIFICACIÓN TIME DEL PORTAFOLIO |  |
| I — Invertir | =COUNTIF(Catálogo!BN6:BN304,"I*") |
| T — Tolerar | =COUNTIF(Catálogo!BN6:BN304,"T*") |
| M — Migrar | =COUNTIF(Catálogo!BN6:BN304,"M*") |
| E — Eliminar | =COUNTIF(Catálogo!BN6:BN304,"E*") |
| 3. DIMENSIÓN ECONÓMICA (TCO) |  |
| TCO total anual del portafolio (COP) | =SUM(Catálogo!BV6:BV304) |
| TCO promedio por solución (COP) | =IFERROR(AVERAGEIF(Catálogo!BV6:BV304,">0",Catálogo!BV6:BV304),0) |
| Solución de mayor TCO (COP) | =IFERROR(MAX(Catálogo!BV6:BV304),0) |
| 4. SOPORTE Y VENCIMIENTOS |  |
| Soluciones con soporte VENCIDO | =COUNTIF('Alertas Caducidad'!F5:F304,"VENCIDO") |
| Por vencer en ≤ 6 meses | =COUNTIF('Alertas Caducidad'!F5:F304,"Por vencer (≤6 meses)") |
| Sin fecha registrada | =COUNTIF('Alertas Caducidad'!F5:F304,"Sin fecha registrada") |
| ANS vencidos | =COUNTIF(Catálogo!AO6:AO304,"Vencido") |
| 5. CALIDAD DEL CATÁLOGO |  |
| Fichas «Completas» | =COUNTIF(Catálogo!K6:K304,"Completa") |
| Fichas «En Levantamiento» | =COUNTIF(Catálogo!K6:K304,"En Levantamiento") |
| Soluciones sin Naturaleza | =SUMPRODUCT((Catálogo!A6:A304<>"")*(Catálogo!D6:D304="")) |
| Hallazgos en Log de Calidad | =COUNTA('Log de Calidad'!A5:A200) |
| 6. AVANCE Y PRIORIZACIÓN (V4) |  |
| % Avance promedio del portafolio ACTIVO (P1) | =IFERROR(AVERAGEIFS(Catálogo!$CQ$6:$CQ$304,Catálogo!$AF$6:$AF$304,"<>Retirado"),"") |
| Soluciones con Prioridad 1 (Prioritaria) asignada | =COUNTIF(Catálogo!$CP$6:$CP$304,"1 - Prioritaria") |
| Soluciones activas sin prioridad de diligenciamiento asignada | =COUNTIFS(Catálogo!$A$6:$A$304,"<>",Catálogo!$AF$6:$AF$304,"<>Retirado",Catálogo!$CP$6:$CP$304,"") |
| 7. SEGURIDAD Y CONTINUIDAD (V4) |  |
| Soluciones con valoración de seguridad Vigente | =COUNTIF(Catálogo!#REF!,"Vigente") |
| Soluciones sin backup definido o desconocido | =COUNTIF(Catálogo!#REF!,"No")+COUNTIF(Catálogo!#REF!,"Desconocido") |
| 8. INSUMOS PARA PLAN DE MANTENIMIENTO (V4) |  |
| Soluciones con Prioridad de intervención ALTA | =COUNTIF(Catálogo!$CU$6:$CU$304,"Alta") |
| Soluciones con próxima revisión ya programada | =SUMPRODUCT(--ISNUMBER(Catálogo!$CT$6:$CT$304)) |

# 7. Hoja: Alertas Caducidad

Solo se evalúan filas del Catálogo con ID diligenciado. Si la fecha de vencimiento está vacía, el estado es «Sin fecha registrada» (no se reporta como vencido).

Columnas: ID Solución, Nombre, Proveedor, Vencimiento, Días restantes, Estado, Recomendación, Estado ANS.

## Patrón de fórmula de la primera fila operativa

| Columna | Fórmula |
| --- | --- |
| A | =IF(Catálogo!A6="","",Catálogo!A6) |
| B | =IF(Catálogo!A6="","",Catálogo!B6) |
| C | =IF(Catálogo!A6="","",Catálogo!AL6) |
| D | =IF(Catálogo!A6="","",Catálogo!AM6) |
| E | =IF(Catálogo!A6="","",IF(NOT(ISNUMBER(Catálogo!AM6)),"",Catálogo!AM6-TODAY())) |
| F | =IF(Catálogo!A6="","",IF(NOT(ISNUMBER(Catálogo!AM6)),"Sin fecha registrada",IF(Catálogo!AM6-TODAY()<0,"VENCIDO",IF(Catálogo!AM6-TODAY()<=180,"Por vencer (≤6 meses)",IF(Catálogo!AM6-TODAY()<=365,"Próximo (≤12 meses)","Vigente"))))) |
| G | =IF(F5="","",IF(F5="VENCIDO","Renovación URGENTE / reclasificar TIME a M",IF(F5="Por vencer (≤6 meses)","Iniciar proceso contractual",IF(F5="Próximo (≤12 meses)","Planificar renovación",IF(F5="Sin fecha registrada","Diligenciar fecha en la Ficha","OK"))))) |
| H | =IF(Catálogo!A6="","",Catálogo!AO6) |

## Defecto visible

La fila 9 contiene referencias `#REF!` en fórmulas del semáforo.

# 8. Hoja: Log de Calidad

Registre aquí las inconsistencias detectadas entre las Fichas firmadas y el Catálogo, así como los campos vacíos en filas con fase «Completa». Cada hallazgo debe tener responsable y fecha de cierre.

| Fecha detección | ID Solución | Campo afectado | Tipo de hallazgo | Descripción del hallazgo | Responsable | Estado / fecha cierre |
| --- | --- | --- | --- | --- | --- | --- |
| 01/07/2026 | APP-0005 | Dependencia dueña del proceso | Valor fuera de vocabulario | "DESPACHO DEL VICEMINISTRO" no coincide exactamente con ninguno de los 2 despachos de viceministro de la lista controlada (Políticas y Normalización / Ordenamiento Territorial). Debe precisarse a cuál corresponde. | OTIC / Dependencia dueña | Abierto |
| 01/07/2026 | APP-0006 | Dependencia dueña del proceso | Valor fuera de vocabulario | Mismo hallazgo que APP-0005. | OTIC / Dependencia dueña | Abierto |
| 01/07/2026 | APP-0007 | Dependencia dueña del proceso | Valor fuera de vocabulario | Mismo hallazgo que APP-0005. | OTIC / Dependencia dueña | Abierto |
| 01/07/2026 | APP-0016 | Dependencia dueña del proceso | Texto duplicado | Valor "Oficina de Tecnologías de la Información y la Comunicación — OTIC — OTIC" tiene el sufijo "OTIC" repetido, probablemente por error de copiado. | OTIC / Dependencia dueña | Abierto |
| 01/07/2026 | APP-0018 | Dependencia dueña del proceso | Dependencia no está en la lista controlada | "UNIDAD TECNICA DE OZONO" no existe en la hoja Listas. Verificar si es una dependencia vigente que deba agregarse al vocabulario, o si corresponde a otra área ya listada. | OTIC / Dependencia dueña | Abierto |
| 01/07/2026 | APP-0040 | Dependencia dueña del proceso | Dependencia no está en la lista controlada | Mismo hallazgo que APP-0018. | OTIC / Dependencia dueña | Abierto |
| 01/07/2026 | APP-0042 | Dependencia dueña del proceso | Campo vacío | La solución no tiene Dependencia dueña del proceso registrada. | OTIC / Dependencia dueña | Abierto |
| 01/07/2026 | APP-0083 | Dependencia dueña del proceso | Valor fuera de vocabulario | Mismo hallazgo que APP-0005. | OTIC / Dependencia dueña | Abierto |

# 9. Hoja: Control de Cambios

| Versión | Fecha | Descripción del cambio | Elaboró | Aprobó |
| --- | --- | --- | --- | --- |
| 1 | (históricas) | Versiones iniciales del catálogo bajo gestión previa. | OTIC | OTIC |
| 2 | 24/09/2025 | Versión 2 del catálogo de Soluciones Tecnológicas. | OTIC | OTIC |
| 3 |  | Reestructuración integral V3: alineación con Ficha F-A-GTI-01 V7 y Guía G-A-GTI-01 V7. Incorporación de taxonomía de 2 niveles (Naturaleza N1-N8 con lista en cascada para Tipo Detallado, 41 valores). Adición de Grupo G7 TCO (7 conceptos de costo + total calculado + ratio TCO/usuario) y Grupo G8 Documentación (7 tipos). Corrección de la lógica de Alertas: fechas como fecha real, semáforo de 5 estados sin falsos positivos en filas vacías. Validaciones de datos en TODAS las columnas con vocabulario controlado. Formato condicional en TIME, Estado, ANS y Documentación. Nuevas hojas: Diccionario, Tablero, Log de Calidad, Instrucciones. Comentarios por columna con definición y vocabulario. | OTIC | Director OTIC |
| 4 | 01/07/2026 | Propuesta V4: corrección de rangos truncados en Tablero/Alertas Caducidad (cubrían solo 50 de 129 soluciones); priorización visual de campos P1/P2/Automático; nueva columna de Vigencia del registro (preserva histórico de soluciones retiradas sin eliminarlas); % de avance por solución; gestión de diligenciamiento por dependencia (nueva hoja Avance por Dependencia); nuevo grupo G12 Seguridad y Continuidad; nuevo grupo G13 Insumos para Plan de Mantenimiento de Sistemas de Información; recuperación de 3 campos documentados en el Diccionario pero ausentes del Catálogo V3; corrección de encabezado (Versión/Código). | Carlos Centeno (OTIC) con asistencia de Claude | (pendiente de aprobación) |

# 10. Hoja: Hoja2

Contiene registros visibles de sistemas y filas pendientes de clasificación; se conserva como insumo del inventario.

| ID Solución | Nombre oficial de la solución | Sigla / Acrónimo | Naturaleza (N1-N8) | Categoría institucional | Descripción de la solución | Dependencia dueña del proceso | Modelo de despliegue |
| --- | --- | --- | --- | --- | --- | --- | --- |
| SYS-0001 | VENTANILLA INTEGRAL DE TRÁMITES AMBIENTALES EN LÍNEA | VITAL | N1 Sistema de información | Misional | sistema de información para la gestión y administración de los formatos únicos de trámites ambientales en línea, a través de esta plataforma los usuarios pueden realizar la solicitud de sus trámites. | Oficina de Tecnologías de la Información y la Comunicación - OTIC | On-Premises |
| SYS-0002 | Sistema de Información para la<br>Gestión de Trámites Ambientales - SILA MC | SILA MC MADS (BACKOFICE) | N1 Sistema de información | Misional | Sistema de información para la adiministración, gestión documental y gestión de trámites ambientales que permite tener trazabilidad de los documentos y expedientes relacionados de trámites y servicios ambientales que prestan las corporaciones y entidades ambientales a nivel nacional | Dirección de Bosques, Biodiversidad y Servicios Ecosistémicos | Nube Pública |
| SYS-0003 | HERRAMIENTA DE ACCION CLIMATICA | HaC | N1 Sistema de información | Misional | Sistema de información que proporciona datos con origen de las entidades oficiales, visualizados de manera dinámica, sobre el comportamiento histórico y futuro del clima cambiante; la vulnerabilidad y el riesgo climático; emisiones y absorciones de CO2 y su relación con variables socioambientales, a partir de lo cual, se construye un perfil territorial de una unidad territorial seleccionada, con el propósito de orientar la incorporación del cambio climático en las dinámicas del desarrollo y planificación del territorio. | Dirección de Cambio Climático y Gestión del Riesgo | On-Premises |
| SYS-0004 | SISTEMA DE INVENTARIO Y ADMINISTRACION FINANCIERA | SIAF | N1 Sistema de información | Apoyo | Programa que tiene el manejo de los inventarios físicos (muebles e inmuebles)del Ministerio de Ambiente y Desarrollo Sostenible, con sus entradas, salidas y alojando un resultado que va alineado con el sistema contable de la entidad. (Modulo) | Grupo De Servicios Administrativos | On-Premises |
| SYS-0005 | SISTEMA DE INFORMACIÓN PARA LA PLANEACIÓN Y GESTIÓN AMBIENTAL DE LAS CAR | CARDINAL | N1 Sistema de información | Misional | CARDINAL (anteriormente conocido como SIPGA-CAR) es el Sistema de Información para la Planificación y Gestión Ambiental de las Corporaciones Autónomas Regionales (CAR). Liderado por el Ministerio de Ambiente (Minambiente), centraliza la información física, financiera y ambiental (como cuencas, vertimientos y ecosistemas) para planificar la gestión de las CAR. | Dirección de Ordenamiento Ambiental Territorial y Coordinación SINA | Nube Pública |
| SYS-0006 | SIFAME HOMINIS (MODULO NOMINA) |  | N1 Sistema de información | Apoyo | Sistema de información que liquida la nómina, seguridad social y prestaciones económicas. (Modulo) | Grupo de Talento Humano | On-Premises |
| SYS-0007 | Sistema de Información Programa Ozono | SIPO | N1 Sistema de información | Apoyo | Este sistema se encarga de monitorear y gestionar los proyectos relacionados con la eliminación de sustancias agotadoras de la capa de ozono (SAO), en cumplimiento del Protocolo de Montreal.El SIPO forma parte de los esfuerzos del Ministerio de Ambiente y se apoya en los lineamientos del Sistema de Información Ambiental de Colombia (SIAC) para el manejo de datos ambientales y territoriales | Dirección de Asuntos Ambientales, Sectorial y Urbana | On-Premises |
| SYS-0008 | PORTAL DE INFORMACIÓN DE TRÁFICO ILEGAL DE FAUNA SILVESTRE - PIFS | PIFS | N1 Sistema de información | Misional | Sistema que permite registrar y hacer seguimiento a las especies relacionadas con el trafico ilegal, desde el acta de decomiso, traslados y disposicion final | Dirección de Bosques, Biodiversidad y Servicios Ecosistémicos | On-Premises |
| SYS-0009 | Salvoconducto Único Nacional en Línea | SUNL | N1 Sistema de información | Misional | Salvoconducto Único Nacional en Línea (SUNL): Permite la movilización de especímenes de la diversidad biológica dentro del territorio nacional, corresponde a un modulo de VITAL. | Dirección de Bosques, Biodiversidad y Servicios Ecosistémicos | Nube Pública |
| SYS-0010 | LIBRO DE OPERACIONES FORESTALES EN LINEA | LOFL | N1 Sistema de información | Misional | Libro de Operaciones Forestales en Línea (LOFL): Es el registro en línea que ampara el inventario de productos forestales en las empresas o industrias forestales en el territorio nacional, autorizado por la autoridad ambiental competente, a través de la Ventanilla Integral de Trámites Ambientales en Línea (VITAL). | Dirección de Bosques, Biodiversidad y Servicios Ecosistémicos | Nube Pública |
| SYS-0011 | Administración y Recepción de Correspondencia Ambiental | ARCA (ORFEO) | N1 Sistema de información | Apoyo | Administración y recepción de correspondencia ambiental | Grupo de Gestión Documental | On-Premises |
| SYS-0012 | Registro Único de Ecosistemas y Áreas Ambientales | REAA | N1 Sistema de información | Misional | Herramienta tecnológica para la gestión de las Autoridades Ambientales que permita el registro automatizado de ecosistemas y áreas de importancia ambiental priorizadas por cada Corporación Autónoma Regional y de Desarrollo sostenible y Autoridades Ambientales Urbanas en sus jurisdicciones, a partir de los criterios definidos por el Ministerio de Ambiente y Desarrollo Sostenible, en las que se podrán implementar Pagos por Servicios Ambientales (PSA) y otros incentivos e instrumentos orientados a la conservación.<br><br>El REAA permitira el registro, consolidación, parametrización, actualización y visualización de la oferta de información ambiental de ecosistemas y áreas ambientales del territorio nacional, priorizadas por las autoridades ambientales en sus jurisdicciones, con excepción de las áreas protegidas registradas en el Registro Único Nacional de Área Protegidas (RUNAP). | Dirección de Bosques, Biodiversidad y Servicios Ecosistémicos | Nube Pública |
| SYS-0013 | Sistema de Información para la Planeación y Gestión Ambiental de las CAR | SIPGACAR | N1 Sistema de información | Estratégica | Sistema para registrar la información de las CARs, referente al avance de ejecución de las metas físicas y financieras del Plan de Acción Institucional (PAI); Indicadores Mínimos de Gestión, ingresos, gastos, medida de efectividad a nivel de impacto ambiental y financiero. Dado el caso, que las CARs tengan esta información en sus sistemas de información propios, se debe extraer de forma automática dicha información y almacenarla en el Sistema de Información que se está diseñando | Dirección de Asuntos Ambientales, Sectorial y Urbana | Nube Pública |
| SYS-0014 | SISTEMA DE INFORMACIÓN DEL RECURSO HÍDIRICO | SIRH | N1 Sistema de información | Misional | Formularios de captura para el registro sobre los diferentes instrumentos de gestión (POMCA, PORH, PMA, etc), y para hacer seguimiento al logro de sus actividades. Incluye Visor geográfico para registrar areas donde se desarrolalron actividades. | Dirección de Gestión Integral del Recurso Hídrico | Nube Pública |
| SYS-0015 | SISTEMA DE INFORMACIÓN DE PROYECTOS CONVOCATORIAS ASIGNACIÓN AMBIENTAL SGR |  | N1 Sistema de información | Estratégica | Garantiza la operación de las convocatorias mediante la recepción y el trámite de los proyectos de la Asignación Ambiental y el 20% del mayor recaudo del Sistema General de Regalías | Oficina Asesora de Planeación | Nube Pública |
| SYS-0016 | Registro Nacional de Reducción de Emisiones - RENARE | RENARE | N1 Sistema de información | Misional | El Registro Nacional de Reducción de Emisiones de Gases de Efecto Invernadero (RENARE) fue creado por la Resolución 1447 de 2018 para gestionar iniciativas de mitigación de gases de efecto invernadero a nivel nacional. Este registro permite registrar proyectos de reducción y remoción de emisiones, como NAMAs, MDL, y Proyectos REDD+. La plataforma RENARE permite el seguimiento de los avances en el cumplimiento de las metas climáticas del país y facilita la certificación de iniciativas de mitigación.<br><br>La versión actual de la plataforma, fue desarrollada e implementada por la OTIC (Oficina de Tecnologías de la Información y las Comunicaciones) de MinAmbiente en su Fase de Factibilidad, con el apoyo de la Dirección de Cambio Climático y Gestión del Riesgo.<br>Adicionalmente, se implementaron funcionalidades para integración con Arca (Radicación) y Consulta de Iniciativas. | Dirección de Cambio Climático y Gestión del Riesgo | Nube Pública |
|  | CONSERVAR PAGA |  |  |  |  |  |  |
|  | 5. ROE Reporte Obligatorio de Emisiones |  |  |  |  |  |  |
|  | Sistema de Captura y Verificación de Negocios Verdes |  |  |  |  |  |  |

# 11. Hoja: Avance por Dependencia

Use esta hoja para gestionar el cierre de brechas dependencia por dependencia. Se calcula automáticamente desde la hoja Catálogo; no diligencie aquí.

Dependencias: Despacho del Ministro; Despacho del Viceministro de Políticas y Normalización Ambiental; Despacho del Viceministro de Ordenamiento Ambiental del Territorio; Secretaría General; Oficina Asesora de Planeación; Oficina Asesora Jurídica; Oficina de Tecnologías de la Información y la Comunicación — OTIC; Oficina de Control Interno; Oficina de Negocios Verdes y Sostenibles; Oficina de Asuntos Internacionales; Dirección de Asuntos Marinos, Costeros y Recursos Acuáticos; Dirección de Bosques, Biodiversidad y Servicios Ecosistémicos; Dirección de Cambio Climático y Gestión del Riesgo; Dirección de Gestión Integral del Recurso Hídrico; Dirección de Asuntos Ambientales, Sectorial y Urbana; Dirección de Ordenamiento Ambiental Territorial y Coordinación SINA; Subdirección Administrativa y Financiera; Subdirección de Educación y Participación; Grupo de Talento Humano; Grupo de Gestión Documental; Grupo de Contratos; Grupo de Comunicaciones; Grupo De Servicios Administrativos.

## Patrón de cálculo

| Indicador | Fórmula fila 5 |
| --- | --- |
| Soluciones registradas | =COUNTIF(Catálogo!$I$6:$I$304,$A5) |
| Activas en gestión | =COUNTIFS(Catálogo!$I$6:$I$304,$A5,Catálogo!$AF$6:$AF$304,"<>Retirado") |
| Históricas (retiradas, preservadas) | =COUNTIFS(Catálogo!$I$6:$I$304,$A5,Catálogo!$AF$6:$AF$304,"Retirado") |
| % Avance promedio P1 (activas) | =IFERROR(AVERAGEIFS(Catálogo!$CQ$6:$CQ$304,Catálogo!$I$6:$I$304,$A5,Catálogo!$AF$6:$AF$304,"<>Retirado"),"") |
| Prioridad 1 asignadas | =COUNTIFS(Catálogo!$I$6:$I$304,$A5,Catálogo!$CP$6:$CP$304,"1 - Prioritaria") |
| Sin prioridad asignada | =COUNTIFS(Catálogo!$I$6:$I$304,$A5,Catálogo!$AF$6:$AF$304,"<>Retirado",Catálogo!$CP$6:$CP$304,"") |

# 12. Observaciones estructurales derivadas del archivo

- `Catálogo` tiene 99 columnas (A:CU), mientras `Diccionario` documenta atributos adicionales hasta DA.
- `Instrucciones` aún se identifica internamente como Versión 3 y habla de 8 hojas, pero el libro contiene 10.
- `Tablero` contiene fórmulas con referencias `#REF!` para indicadores de seguridad y continuidad.
- `Alertas Caducidad` presenta referencias `#REF!`.
- `Hoja2` contiene registros de sistemas que no están cargados en la hoja principal `Catálogo`.
