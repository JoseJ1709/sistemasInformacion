# G-A-GTI-01 — Guía de Diligenciamiento y Administración del Catálogo Institucional de Sistemas de Información

> **Instrumentos que gobierna esta guía:**
> - **F-A-GTI-02** — Catálogo Institucional de Sistemas de Información (libro Excel de 7 hojas).
> - **F-A-GTI-01** — Ficha de Caracterización de Sistema de Información.
>
> **Entidad:** Ministerio de Ambiente y Desarrollo Sostenible — OTIC.

---

## Sección 1 — Propósito, alcance y definiciones de uso

**Objetivo de la guía.** Explicar cómo clasificar, registrar, actualizar y controlar la calidad de la información del Catálogo (F-A-GTI-02) y de la Ficha (F-A-GTI-01), sin convertirse en tratado teórico.

**A quién aplica.** A la OTIC, a los responsables funcionales y técnicos de cada Sistema de Información (SI), y a las áreas que aportan datos contractuales, de seguridad o financieros.

**Relación entre los tres instrumentos:**

| Instrumento | Función |
| --- | --- |
| F-A-GTI-02 Catálogo | Vista consolidada del portafolio: identificar, comparar, gobernar, priorizar, alertar y decidir. Un registro por SI. |
| F-A-GTI-01 Ficha | Expediente técnico-funcional completo de cada SI. Una ficha por SI. |
| G-A-GTI-01 Guía | Reglas de clasificación, diligenciamiento, vocabularios, actualización y calidad. |

**Principio rector — `FICHA ⊃ CATÁLOGO`:** la Ficha contiene todos los campos del registro del Catálogo más el detalle ampliado. El Catálogo nunca contiene información que no esté también reflejada o sintetizada en la Ficha del SI.

---

## Sección 2 — Base normativa y diferenciación de fuentes

Todo dato o regla del instrumento pertenece a una de estas cuatro categorías, que deben mantenerse diferenciadas:

| Categoría | Qué puede afirmarse | Ejemplos en este instrumento |
| --- | --- | --- |
| **Obligación MinTIC / Gobierno Digital** | Solo lo expresamente soportado por norma o marco oficial citado. | Definiciones normativas de Sistema de Información, Servicio Tecnológico y Plataforma (Decreto 767 de 2022); adopción del MRAE v3 (Resolución 1978 de 2023). |
| **Recomendación MinTIC** | Lo sugerido por guías o marcos oficiales sin carácter de obligación taxativa de campo. | Lineamientos del dominio de SI del MGGTI.G.SI sobre documentación, soporte y ciclo de vida. |
| **Decisión institucional propuesta** | Definiciones de frontera, diseño del libro, campos exactos y reglas de clasificación cerradas en este proyecto. | Clase de inventario A-F, las 44 columnas de `Catálogo_SI`, patrón de IDs, vocabularios controlados. |
| **Buena práctica técnica** | Complementos usados cuando MinTIC no define el concepto con suficiente detalle. | TIME como marco complementario de portafolio (no es obligación MinTIC); definiciones de SaaS (NIST), API (ISO/IEC 2382), servicio web (W3C). |

**Fuentes mínimas citadas:**

- **Decreto 767 de 2022** — definiciones normativas de Sistema de Información, Servicio Tecnológico y Plataforma. <https://gobiernodigital.mintic.gov.co/692/w3-article-272977.html>
- **Resolución 1978 de 2023** — adopta la versión 3 del MRAE. <https://normograma.mintic.gov.co/mintic/compilacion/docs/resolucion_mintic_1978_2023.htm>
- **MGGTI.G.SI** — referencia oficial del dominio de gestión de sistemas de información; la numeración fina de sublineamientos requiere validación directa en red institucional. <https://mintic.gov.co/arquitecturaempresarial/630/articles-237662_recurso_1.pdf>
- **MAE.G.ASI y MAE.GE.ASI.01** — referencias del dominio ASI; no debe asumirse una serie separada `MAE.LI.ASI.01-.03` sin verificación documental directa. <https://mintic.gov.co/arquitecturaempresarial/>
- **Fuentes complementarias:** NIST SP 800-145 (SaaS), ISO/IEC 2382 (API, base de datos), W3C Web Services Architecture (servicio web), OASIS SOA RA (ESB/mediación), ISO 19101 / Esri (GIS).

---

## Sección 3 — Taxonomía institucional y frontera del inventario

**Decisión cerrada:** la clasificación "Naturaleza N1-N8" del instrumento anterior **se sustituye** por dos mecanismos:

1. **Clase de inventario A-F** — decide en qué hoja o artefacto se registra cada activo.
2. **Tipo o patrón de SI** — clasifica únicamente los registros que sí son SI.

### 3.1 Clase de inventario A-F

| Clase | Objeto | Dónde se registra |
| --- | --- | --- |
| **A** | Sistema de Información | `Catálogo_SI` + Ficha F-A-GTI-01 |
| **B** | Componente de un SI | Hoja `Componentes` o referencia en la Ficha |
| **C** | Integración / Interfaz | Hoja `Integraciones_Interfaces` |
| **D** | Plataforma tecnológica | Catálogo/hoja de plataformas o soporte; **no** `Catálogo_SI` |
| **E** | Servicio de TI | Catálogo de servicios de TI; **no** `Catálogo_SI` |
| **F** | Otro activo tecnológico | No requiere inventario independiente en este instrumento, salvo decisión posterior de OTIC |

### 3.2 Regla obligatoria de pertenencia al `Catálogo_SI`

Un activo entra al `Catálogo_SI` **solo si cumple las cinco condiciones**:

1. soporta uno o más procesos o servicios institucionales;
2. gestiona información del negocio;
3. tiene responsabilidad funcional y técnica identificables;
4. tiene ciclo de vida y gobierno propios;
5. es reconocible como unidad funcional completa para la entidad.

### 3.3 Glosario resumido

(Definiciones completas y fuentes: `04_Taxonomia_Institucional_SI.md`.)

- **Sistema de Información (SI):** unidad funcional completa que soporta procesos institucionales, gestiona información del negocio y tiene gobierno propio.
- **Aplicación / sistema transaccional:** forma o patrón de SI; no una clase de inventario distinta.
- **Módulo / microservicio / base de datos:** componentes internos (clase B).
- **API / servicio web / interfaz:** contrato o mecanismo de interoperabilidad (clase C); nunca SI.
- **Integración:** relación origen→destino entre activos (clase C).
- **Hub / ESB / iPaaS / middleware / API Gateway:** plataforma o capacidad de integración (clase D); no SI de negocio.
- **Servicio de TI:** capacidad consumida como servicio para operación o soporte (clase E).
- **SaaS:** modalidad de despliegue/prestación; **atributo**, nunca clase principal.

### 3.4 Reglas de frontera (decisiones cerradas)

- **ERP / CRM / BPM / CMS / SGD / GIS:** pueden ser SI cuando constituyen la unidad funcional gobernada; de lo contrario son plataforma o componente.
- **Dashboard:** normalmente no es SI; se documenta dentro de una solución analítica o de otro SI.
- **SaaS:** se registra en `Modelo_de_despliegue`, no como tipo de SI.
- **API / servicio web / interfaz / integración:** nunca SI; van a `Integraciones_Interfaces`.
- **Microservicio / módulo / base de datos:** componente o detalle técnico, no SI por defecto.
- **Hub / ESB / iPaaS / middleware:** plataforma o componente de integración, no SI de negocio.

---

## Sección 4 — Árbol de decisión: ¿Este activo entra al Catálogo Institucional de SI?

1. **¿El activo soporta directamente uno o más procesos o servicios institucionales y gestiona información del negocio?**
   - No → vaya a 6. · Sí → vaya a 2.
2. **¿Tiene responsabilidad funcional identificable, responsable técnico, ciclo de vida y gobierno propios?**
   - No → **B. Componente** o **F. Otro activo**, según corresponda. · Sí → vaya a 3.
3. **¿La unidad funcional es completa para el usuario institucional, aunque internamente use varios módulos, APIs o componentes?**
   - Sí → **A. Sistema de Información**. · No → vaya a 4.
4. **¿Es un contrato, endpoint, interfaz, flujo de datos o mecanismo de interoperabilidad entre soluciones?**
   - Sí → **C. Integración / Interfaz**. · No → vaya a 5.
5. **¿Habilita varias soluciones como capacidad base (motor, bus, gateway, iPaaS, IAM, DB compartida, plataforma BPM)?**
   - Sí → **D. Plataforma tecnológica**. · No → **B. Componente de un SI**.
6. **¿Es una capacidad consumida como servicio para operación o soporte (correo, hosting, monitoreo, VPN, respaldo, repositorio, servicio cloud)?**
   - Sí → **E. Servicio de TI**. · No → vaya a 7.
7. **¿Es solo un atributo o modalidad de prestación (SaaS, on-premises, nube pública)?**
   - Sí → **F. Atributo**, no inventario independiente. · No → vaya a 8.
8. **¿Es únicamente un elemento interno sin gobierno separado (módulo, microservicio, base de datos, dashboard dependiente)?**
   - Sí → **B. Componente** o simple referencia en Ficha. · No → **F. Otro activo tecnológico** hasta que OTIC defina un inventario especializado.

**Ejemplos de clasificación correcta:**

| Activo observado | Clase | Registro |
| --- | --- | --- |
| Sistema de gestión documental institucional con dueño funcional y soporte propio | A | `Catálogo_SI` + Ficha |
| Microservicio de autenticación usado por un SI | B | `Componentes` |
| API REST que expone información a otra entidad | C | `Integraciones_Interfaces` |
| Bus de integración / iPaaS institucional | D | Catálogo de plataformas |
| Servicio de correo electrónico corporativo | E | Catálogo de servicios de TI |
| Modalidad SaaS de un SI contratado | F (atributo) | Campo `Modelo_de_despliegue` del SI |

**Errores frecuentes que deben evitarse:**

- registrar cada módulo o microservicio como un SI independiente;
- registrar una API o un servicio web como SI;
- registrar "SaaS" como tipo de sistema en lugar de modalidad de despliegue;
- crear un registro de SI para un dashboard que depende de otra solución;
- dejar integraciones descritas como texto libre dentro del registro del SI en lugar de la hoja normalizada.

---

## Sección 5 — Modelo del libro Excel F-A-GTI-02

El libro contiene **exactamente 7 hojas**:

| Hoja | Función |
| --- | --- |
| `Catálogo_SI` | Inventario consolidado: un registro por SI, 44 columnas. |
| `Integraciones_Interfaces` | Relación normalizada de integraciones, APIs, servicios web e interfaces relevantes (una fila por relación). |
| `Componentes` | Componentes internos o compartidos de los SI cuando ameriten inventario independiente. |
| `Diccionario` | Definición, fuente, obligatoriedad, responsable, tipo, vocabulario y reglas de cada campo de las hojas operativas. |
| `Listas` | Vocabularios controlados que alimentan las validaciones de datos. |
| `Tablero` | Indicadores agregados, alertas y semáforos gerenciales (fórmulas automáticas). |
| `Calidad` | Completitud calculada por SI, hallazgos, inconsistencias y trazabilidad de migración. |

**Hojas que desaparecen respecto del estado anterior y por qué:**

| Hoja anterior | Destino |
| --- | --- |
| `Instrucciones` | Absorbida por esta Guía; el Excel no lleva hoja de instrucciones. |
| `Alertas Caducidad` | Absorbida por `Tablero` (fórmulas) y `Calidad`. |
| `Log de Calidad` | Sustituida por `Calidad`. |
| `Avance por Dependencia` | Vista calculada en `Tablero` / `Calidad`. |
| `Control de Cambios` | Pasa a gestión documental del instrumento, no hoja operativa. |
| `Hoja2` | Insumo transitorio de migración; se elimina tras migrar. |

**Por qué se normalizan integraciones y componentes:** son relaciones uno-a-muchos. Mantenerlas como texto agregado en columnas del catálogo impide contarlas, alertar sobre ellas y auditarlas. En hoja propia, cada relación se enlaza por `ID_SI_Origen` / `ID_SI_Padre` y el catálogo recibe automáticamente los conteos (`Numero_integraciones_activas`, `Numero_componentes_registrados`).

---

## Sección 6 — Instrucciones de diligenciamiento de `Catálogo_SI` (44 campos)

Convenciones: **O** = Obligatorio, **R** = Recomendado, **C** = Condicional, **A** = Automático (no diligenciar manualmente).

| # | Campo | Qué significa | Cómo diligenciarlo | Responsable primario | Error frecuente | Obl. |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | ID_SI | Código único del SI. | Patrón `SI-####` asignado por OTIC al crear el registro. No reutilizar IDs de SI retirados. | OTIC | Reutilizar un ID o cambiarlo después de creado. | O |
| 2 | Nombre_oficial | Nombre institucional vigente. | Nombre completo oficial, sin siglas ni versiones. | Resp. funcional | Registrar el nombre comercial del proveedor. | O |
| 3 | Sigla_Acronimo | Sigla usada oficialmente. | Solo si existe uso institucional real. | Resp. funcional | Inventar siglas. | R |
| 4 | Tipo_o_patron_de_SI | Patrón funcional del SI. | Elegir de la lista (transaccional, ERP, CRM, BPM/BPMS, CMS, SGD, GIS, solución analítica, otro). | OTIC + responsables | Usar clases que no son SI (API, plataforma, SaaS). | O |
| 5 | Categoria_institucional | Misional / Estratégica / Apoyo / Evaluación y control / Otro. | Según el proceso institucional soportado. | Resp. funcional | Clasificar por la dependencia y no por el proceso. | O |
| 6 | Descripcion_breve | Resumen ejecutivo de propósito y alcance. | Máximo un párrafo, lenguaje de negocio. | Resp. funcional | Copiar descripciones técnicas extensas (eso va en la Ficha). | O |
| 7 | Procesos_institucionales_soportados | Procesos del mapa institucional. | Nombres oficiales de procesos vigentes; separar con «;». | Resp. funcional | Escribir actividades en vez de procesos del mapa. | O |
| 8 | Dependencia_duena_del_proceso | Dependencia dueña del proceso. | Elegir del listado oficial de dependencias (hoja `Listas`). | Resp. funcional | Registrar a la OTIC como dueña de procesos misionales. | O |
| 9 | Area_responsable_funcional | Área con liderazgo funcional. | Del listado de dependencias. | Resp. funcional | Confundir con el área técnica. | O |
| 10 | Responsable_funcional | Persona designada. | Nombre completo del titular vigente. | Resp. funcional | Dejar nombres de exfuncionarios. | O |
| 11 | Area_responsable_tecnica | Área TI responsable de operación. | Del listado de dependencias / áreas TI. | Resp. técnico | Dejarlo vacío en SaaS (siempre hay responsable interno). | O |
| 12 | Responsable_tecnico | Persona designada. | Nombre completo del titular vigente. | Resp. técnico | Registrar al proveedor externo como responsable. | O |
| 13 | Estado_del_SI | Estado del ciclo de vida. | Lista: Activo, En desarrollo, En mantenimiento, En migración, Deprecado, Retirado. | Resp. técnico | No actualizarlo al retirar el SI. | O |
| 14 | Fecha_salida_produccion | Primera puesta en producción. | DD/MM/AAAA. Si es histórica y exacta desconocida, usar la mejor evidencia y anotarlo en `Calidad`. | Resp. técnico | Registrar la fecha de la última versión. | O |
| 15 | Version_actual | Versión operativa. | Según esquema del producto. | Resp. técnico | No actualizar tras liberaciones mayores. | R |
| 16 | Modelo_de_despliegue | Modalidad principal de operación. | Lista: On-premises, nube pública, nube privada, híbrida, SaaS, PaaS. | Resp. técnico | Usar SaaS como tipo de SI (campo 4). | O |
| 17 | Tipo_de_desarrollo_adquisicion | Forma de obtención. | Lista: Propio, a la medida, COTS, open source, SaaS, híbrido, legado. | Resp. técnico | Confundir COTS con desarrollo a la medida. | O |
| 18 | Fabricante_o_proveedor_principal | Proveedor principal. | Nombre del fabricante o contratista vigente. | Técnico / contratación | Registrar al integrador en lugar del fabricante. | R |
| 19 | Tipo_de_licenciamiento | Modalidad de licenciamiento. | Lista controlada. | Técnico / contratación | Marcar «Sin licenciamiento» en productos comerciales. | R |
| 20 | Soporte_vigente_hasta | Vencimiento de soporte principal. | DD/MM/AAAA de la cobertura contractual o del fabricante. | Técnico / contratación | No actualizar al renovar el contrato. | O |
| 21 | Estado_ANS_terceros | Estado del ANS con terceros. | Lista: Vigente, Vencido, En negociación, No aplica. «No aplica» solo si no hay terceros. | Técnico / contratación | Dejar vacío en lugar de «No aplica». | C |
| 22 | Marco_legal_mandatorio | Norma principal que obliga el SI. | Referencia corta (norma, artículo). | Resp. funcional | Listar todas las normas relacionadas (eso va en la Ficha). | R |
| 23 | Objetivos_estrategicos_que_apoya | Objetivos PEI/sectoriales. | Referencias del plan vigente; separar con «;». | Resp. funcional | Copiar objetivos genéricos sin trazabilidad al PEI. | R |
| 24 | Criticidad_operacional | Impacto por indisponibilidad. | Lista: Alta, Media, Baja, valorada con el responsable técnico. | Funcional + técnico | Calificar todo como «Alta» sin criterio. | O |
| 25 | Usuarios_activos | Usuarios activos o recurrentes. | Número entero ≥ 0 con la mejor evidencia disponible. | Resp. funcional | Registrar usuarios creados en vez de activos. | R |
| 26 | Cobertura_del_proceso | Grado de cobertura del proceso. | Lista: Alto, Medio, Bajo, No evaluado. | Resp. funcional | Dejar «No evaluado» indefinidamente. | R |
| 27 | Clasificacion_de_la_informacion | Nivel de clasificación (Ley 1712). | Lista: Pública, Uso interno, Reservada, Clasificada. Usar el nivel más alto tratado. | Resp. funcional | Clasificar por el promedio y no por el dato más sensible. | O |
| 28 | Manejo_de_datos_personales | Tratamiento de datos personales y rol. | Lista: Sí-responsable, Sí-encargado, No (Ley 1581 / Decreto 1074). | Resp. funcional | Marcar «No» cuando hay datos de funcionarios. | O |
| 29 | Interopera_con_entidades_externas | Interoperabilidad con terceros externos. | Sí / No. El detalle va en `Integraciones_Interfaces`. | Resp. técnico | Inconsistencia con la hoja de integraciones. | O |
| 30 | Numero_integraciones_activas | Conteo de integraciones activas. | **Automático** (fórmula sobre `Integraciones_Interfaces`). No editar. | Calculado | Sobrescribir la fórmula manualmente. | A |
| 31 | Numero_componentes_registrados | Conteo de componentes del SI. | **Automático** (fórmula sobre `Componentes`). No editar. | Calculado | Sobrescribir la fórmula manualmente. | A |
| 32 | Valoracion_de_seguridad | Vigencia de la valoración MSPI/seguridad. | Lista: Vigente, Desactualizada, No realizada. | Técnico / seguridad | Marcar «Vigente» con valoraciones de más de un año. | O |
| 33 | Nivel_de_riesgo_residual | Riesgo residual más reciente. | Lista: Alto, Medio, Bajo, No evaluado, tomado del análisis de riesgos. | Seguridad / técnico | Registrar riesgo inherente en vez de residual. | R |
| 34 | Backup_definido | Existencia de respaldo definido. | Lista: Sí, No, Desconocido. | Resp. técnico | Marcar «Sí» sin evidencia de restauración probada. | O |
| 35 | Plan_de_continuidad | Estado del plan de continuidad. | Lista: Vigente, Desactualizado, No existe. | Resp. técnico | Confundir backup con plan de continuidad. | R |
| 36 | Estado_documentacion_minima | Estado agregado de la documentación mínima. | Lista: Completa, Parcial, Crítica, No evaluada, derivado de la Sección 11 de la Ficha. | Calculado desde Ficha/Calidad | Calificar sin revisar la tabla de documentación de la Ficha. | O |
| 37 | Clasificacion_TIME | Clasificación estratégica (marco complementario; no obligación MinTIC). | Lista: T, I, M, E, con justificación en la Ficha (Sección 9.4). | OTIC / comité | Asignar TIME sin diligenciar los ejes en la Ficha. | O |
| 38 | Tipo_intervencion_recomendada | Acción principal sugerida. | Lista: Modernizar, migrar, retirar, sostener, optimizar. Debe ser coherente con TIME. | OTIC | Recomendar «sostener» a un SI clasificado E. | O |
| 39 | Prioridad_intervencion | Prioridad resultante. | Lista: Alta, Media, Baja. | OTIC | Todas las intervenciones en «Alta». | O |
| 40 | TCO_anual_total_COP | TCO anual consolidado. | Valor en COP ≥ 0, igual al total de la tabla TCO de la Ficha (Sección 10). | Financiero / técnico | Registrar solo licenciamiento como TCO total. | R |
| 41 | Ratio_TCO_por_usuario_COP | TCO / usuarios activos. | **Automático** (fórmula). No editar. | Calculado | Editar la celda manualmente. | A |
| 42 | Ultima_revision_anual | Última revisión integral. | DD/MM/AAAA de la revisión anual efectiva. | OTIC | Registrar actualizaciones parciales como revisión integral. | O |
| 43 | Proxima_revision_programada | Próxima revisión programada. | DD/MM/AAAA; normalmente última revisión + 12 meses. | OTIC | No reprogramar tras cada revisión. | R |
| 44 | Vigencia_del_registro | Registro vigente o histórico. | Lista: Vigente, Histórico. Los SI retirados pasan a «Histórico»; **nunca se eliminan filas**. | OTIC | Borrar filas de SI retirados. | O |

---

## Sección 7 — Instrucciones para `Integraciones_Interfaces` y `Componentes`

### 7.1 Cuándo crear un registro

| Situación | Acción |
| --- | --- |
| Integración o interfaz operativa relevante entre el SI y otro activo o entidad | Crear fila en `Integraciones_Interfaces`. |
| Componente con identidad técnica relevante (versión, soporte o criticidad propios, o compartido entre SI) | Crear fila en `Componentes`. |
| Componente trivial sin valor de gobierno separado (módulo menor, librería) | Solo tabla interna de la Ficha (Sección 4); no crear fila. |
| Detalle puramente descriptivo de un flujo interno | Solo narrativa en la Ficha (Secciones 3 y 5). |

### 7.2 Cardinalidad y enlace por ID

- La relación es **uno-a-muchos**: un SI puede tener N integraciones y N componentes; cada fila pertenece a un solo SI.
- En `Integraciones_Interfaces` es obligatorio `ID_SI_Origen`; debe existir en `Catálogo_SI`. `Nombre_SI_Origen` se deriva automáticamente por búsqueda.
- Cuando el destino es un SI interno, usar su `ID_SI` en `ID_SI_Destino_o_Activo_Destino`; cuando es externo, identificar el activo o la entidad externa y diligenciar `Entidad_externa_relacionada`.
- En `Componentes` es obligatorio `ID_SI_Padre`; debe existir en `Catálogo_SI`. Un componente compartido se registra una vez, con `Compartido_con_otro_SI = Sí`, asociado al SI que ejerce su gobierno principal, y se referencia desde las fichas de los demás SI.
- IDs: `INT-####` para integraciones, `CMP-####` para componentes; los asigna OTIC y no se reutilizan.
- Los conteos del catálogo (campos 30 y 31) se calculan desde estas hojas: si el conteo no cuadra, el error está en las hojas normalizadas, no en el catálogo.

### 7.3 Datos mínimos por fila

- **Integración:** tipo de registro, tipo de interfaz o mecanismo, propósito, dirección del flujo, criticidad y estado.
- **Componente:** tipo, función, estado, versión y soporte cuando aplique.

---

## Sección 8 — Instrucciones de diligenciamiento de la Ficha F-A-GTI-01

La Ficha se organiza en un encabezado documental y 12 secciones (`06_Estructura_Ficha_Final.md`).

| Sección | Objetivo | Datos mínimos | Fuentes típicas | Responsable | Evidencias / anexos de referencia |
| --- | --- | --- | --- | --- | --- |
| 0. Encabezado | Control documental de la ficha. | Código, versión, fechas, ID_SI, estado, elaborador, aprobador. | Gestión documental. | OTIC | Historial de versiones. |
| 1. Identificación general | Identidad, propósito y contexto. | Campos de identificación del catálogo + objetivo, alcance y narrativa de negocio. | Catálogo, mapa de procesos, PEI. | Funcional + técnico | Actos de creación, normas. |
| 2. Gobierno y responsables | Dueños funcionales y técnicos explícitos. | Áreas, nombres y correos de responsables; comité si existe. | Designaciones, actos internos. | Funcional + técnico | Memorando o acto de designación. |
| 3. Arquitectura funcional y de información | Cómo opera el SI. | Funcionalidades, entradas/salidas, actores, entidades de información críticas, zonas MAE/MRAE. | Documentación funcional, arquitectura. | Funcional + técnico | Diagramas y catálogos de datos (referenciados). |
| 4. Componentes internos | Descomposición técnica relevante. | Tabla de componentes; referencia por ID a la hoja `Componentes` cuando exista. | Arquitectura de solución, repositorios. | Técnico | Documento de arquitectura. |
| 5. Integraciones e interfaces | Relaciones con otros activos. | Tabla de integraciones + narrativa de interoperabilidad y terceros críticos. | Hoja `Integraciones_Interfaces`, contratos de intercambio. | Técnico | Acuerdos de intercambio, especificaciones de API. |
| 6. Arquitectura tecnológica y despliegue | Detalle técnico mínimo suficiente. | Despliegue, stack, contenerización, CI/CD, repositorios (por enlace). | Documentación técnica, DevOps. | Técnico | Enlaces a repositorios y pipelines. |
| 7. Ciclo de vida, soporte y operación | Estado operativo y soporte. | Estado, soporte, ANS, incidentes 12M, riesgos, obsolescencias, evolución prevista. | Contratos, mesa de servicio. | Técnico + contratación | Contratos, informes de ANS. |
| 8. Seguridad, privacidad y continuidad | Cumplimiento mínimo de seguridad. | Valoración, riesgo residual, clasificación, datos personales, backup, RTO/RPO, continuidad, accesibilidad si aplica. | Análisis de riesgos MSPI, planes de continuidad. | Técnico + seguridad | Análisis de riesgos, plan de continuidad. |
| 9. Calidad, valor y análisis estratégico | Soporte de decisiones de portafolio. | Valor y cobertura, DOFA, madurez, ejes TIME + clasificación y justificación. | Encuestas, comité de portafolio. | OTIC + funcional | Actas de comité. |
| 10. Dimensión económica y mantenimiento | Trazabilidad del TCO. | Tabla TCO desagregada, mantenimiento recomendado y observaciones para el plan anual. | Presupuesto, contratos. | Financiero + técnico | Certificados y contratos. |
| 11. Documentación y evidencias | Verificación de documentación mínima. | Tabla de documentos con estado, ubicación y responsable. | Repositorios documentales. | Técnico | Enlaces a repositorio documental. |
| 12. Validación y control de cambios | Aprobación formal. | Control de cambios, validaciones técnica, funcional y OTIC, fecha de aprobación. | Gestión documental. | OTIC | Registro de aprobación. |

**Reglas transversales de la Ficha:**

- Todos los 44 campos del catálogo deben verse o resumirse en la Ficha (trazabilidad en el anexo de `F-A-GTI-01_Ficha_Caracterizacion.md`).
- La Ficha **referencia** manuales, diagramas y contratos; no los transcribe.
- Los valores compartidos con el catálogo deben coincidir exactamente; toda discrepancia se registra como hallazgo en `Calidad`.

---

## Sección 9 — Vocabularios controlados y reglas de validación

### 9.1 Listas controladas

Los vocabularios viven en la hoja `Listas` del libro y alimentan las validaciones de datos de `Catálogo_SI`, `Integraciones_Interfaces`, `Componentes` y `Calidad`. Solo OTIC modifica la hoja `Listas`; cualquier cambio de vocabulario se registra como versión del instrumento.

### 9.2 Reglas de formato

| Elemento | Regla |
| --- | --- |
| IDs | `SI-####`, `INT-####`, `CMP-####`; consecutivos, asignados por OTIC, nunca reutilizados. |
| Fechas | DD/MM/AAAA (formato de fecha real de Excel, no texto). |
| Moneda | COP, números enteros sin puntos ni símbolos escritos a mano; usar formato de celda. |
| Listas múltiples (procesos, objetivos) | Valores separados por «;» dentro de la celda. |
| Campos calculados | Celdas sombreadas azul; nunca se digitan manualmente. |

### 9.3 Validaciones condicionales

- `Estado_ANS_terceros` distinto de «No aplica» exige `Fabricante_o_proveedor_principal` diligenciado.
- `Interopera_con_entidades_externas = Sí` exige al menos una fila en `Integraciones_Interfaces` con `Entidad_externa_relacionada` diligenciada.
- `Manejo_de_datos_personales` distinto de «No» exige revisar la Sección 8 de la Ficha (RNBD cuando aplique).
- `Estado_del_SI = Retirado` exige `Vigencia_del_registro = Histórico`.
- `Clasificacion_TIME` diligenciada exige ejes TIME y justificación en la Ficha (Sección 9.4).

### 9.4 «No aplica», «Desconocido» y vacíos

- **«No aplica»** solo en campos condicionales (por ejemplo `Estado_ANS_terceros` sin terceros).
- **«Desconocido»** solo donde el vocabulario lo prevé (por ejemplo `Backup_definido`); genera hallazgo en `Calidad` con fecha límite de resolución.
- **Vacío** solo se permite en campos Recomendados u Opcionales; un campo Obligatorio vacío es un hallazgo de completitud.

---

## Sección 10 — Ciclo de actualización y eventos disparadores

| Evento | Acción sobre los instrumentos |
| --- | --- |
| **Alta inicial del SI** | OTIC asigna `ID_SI`, se diligencian los campos obligatorios del catálogo y se abre la Ficha en estado Borrador. |
| **Paso a producción** | Se actualizan `Estado_del_SI`, `Fecha_salida_produccion`, `Version_actual`; la Ficha pasa a Vigente. |
| **Revisión anual obligatoria** | Revisión integral de los 44 campos y de la Ficha; se actualizan `Ultima_revision_anual` y `Proxima_revision_programada`. |
| **Incidente relevante** | Revisar `Criticidad_operacional`, `Valoracion_de_seguridad`, `Nivel_de_riesgo_residual` y Sección 7 de la Ficha. |
| **Vencimiento de soporte o ANS** | Actualizar `Soporte_vigente_hasta` y `Estado_ANS_terceros`; el `Tablero` alerta 90 días antes. |
| **Cambio normativo** | Revisar `Marco_legal_mandatorio` y clasificación de la información. |
| **Cambio de responsable** | Actualizar campos 9-12 del catálogo y Sección 2 de la Ficha, con evidencia de designación. |
| **Retiro del SI** | `Estado_del_SI = Retirado`, `Vigencia_del_registro = Histórico`; la fila **no se elimina**; la Ficha se cierra. |

---

## Sección 11 — Control de calidad y gobierno del dato

Controles mínimos, administrados en la hoja `Calidad`:

1. **Completitud:** porcentaje calculado por SI (bloque A de `Calidad`); los campos obligatorios vacíos se registran como hallazgos (bloque B).
2. **Consistencia entre hojas:** conteos del catálogo vs. filas de `Integraciones_Interfaces` y `Componentes`; coincidencia de valores compartidos entre Catálogo y Ficha; IDs referenciados que existan en `Catálogo_SI`.
3. **Validación de vocabulario:** solo valores de la hoja `Listas`; las validaciones de datos del libro bloquean valores fuera de vocabulario.
4. **Vigencia:** soporte, valoración de seguridad, plan de continuidad y revisiones se monitorean en `Tablero`; los vencidos generan hallazgo.
5. **Coherencia del modelo de priorización:** `Clasificacion_TIME`, `Tipo_intervencion_recomendada` y `Prioridad_intervencion` deben ser coherentes entre sí y con los ejes de la Ficha; el TCO del catálogo debe igualar el total de la tabla TCO de la Ficha.
6. **Preservación del histórico:** nunca se eliminan filas; los retiros pasan a `Vigencia_del_registro = Histórico` y las reclasificaciones y la migración desde el inventario anterior se trazan en `Calidad`.

**Roles:** OTIC administra el libro, las listas y los IDs; los responsables funcionales y técnicos aportan y validan los datos de sus SI; los hallazgos tienen responsable de corrección, fecha de detección y fecha de cierre.

---

## Sección 12 — Ejemplos mínimos de clasificación y diligenciamiento

1. **SI transaccional.** Un sistema institucional de trámites con dueño funcional, responsable técnico y soporte propio → Clase **A**; fila en `Catálogo_SI` con `Tipo_o_patron_de_SI = Sistema transaccional` + Ficha completa.
2. **Integración API.** El mismo sistema consume un servicio REST de otra entidad para validar identidad → Clase **C**; fila en `Integraciones_Interfaces` (`Tipo_de_registro = Interfaz consumida`, `Tipo_de_interfaz_o_mecanismo = API REST`, `Entidad_externa_relacionada` diligenciada). En el catálogo solo cambia `Interopera_con_entidades_externas = Sí` y el conteo automático.
3. **Componente microservicio.** El sistema tiene un microservicio de notificaciones con versión y despliegue propios → Clase **B**; fila en `Componentes` (`Tipo_de_Componente = Microservicio`, `ID_SI_Padre` del sistema) y referencia por ID en la Sección 4 de la Ficha.
4. **Plataforma iPaaS.** El bus de integración institucional que conecta varios SI → Clase **D**; **no** entra a `Catálogo_SI`; se registra en el catálogo de plataformas y cada flujo que lo atraviesa se documenta como integración de su SI origen.
5. **Solución analítica con dashboard dependiente.** Una bodega de datos con gobierno propio que publica tableros → la solución analítica es Clase **A** (`Tipo_o_patron_de_SI = Solución analítica`); cada dashboard es contenido de esa solución y se documenta en su Ficha, **sin** registro propio en el catálogo.

---

## Reglas editoriales de esta guía

1. No repite definiciones largas que ya están en `04_Taxonomia_Institucional_SI.md`; resume y referencia.
2. No vuelve a explicar teoría general de AE o Gobierno Digital salvo lo necesario para diligenciar bien.
3. No duplica el `Diccionario` del libro: el Diccionario define campos; esta guía explica cómo diligenciarlos.
4. Usa ejemplos del Ministerio solo cuando aclaran la frontera del inventario.
5. Diferencia explícitamente obligación MinTIC, recomendación MinTIC, decisión institucional y buena práctica (Sección 2).
