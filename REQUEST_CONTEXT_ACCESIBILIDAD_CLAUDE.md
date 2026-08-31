# REQUEST + CONTEXTO MAESTRO — ACCESIBILIDAD DIGITAL MINAMBIENTE

**Estado:** Baseline de trabajo para transferencia a otra IA  
**Fecha de corte:** 31/08/2026  
**Entidad:** Ministerio de Ambiente y Desarrollo Sostenible — MinAmbiente  
**Ámbito:** Accesibilidad web y de contenidos digitales asociados al portal institucional  
**Modelo destino:** Claude Fable 5  
**Propósito del archivo:** transferir el contexto acumulado, las decisiones ya tomadas, las fuentes, las restricciones, los pendientes y el método de trabajo para que otra IA pueda continuar el proyecto sin reiniciarlo, mezclarlo con otros proyectos ni reabrir decisiones cerradas sin evidencia nueva.

---

## 0. PROMPT MAESTRO MEJORADO

Actúa como un equipo senior interdisciplinario especializado en accesibilidad digital del sector público colombiano, WCAG, Gobierno Digital, arquitectura y operación web, seguridad digital, gestión documental, servicio a la ciudadanía, lenguaje claro, gobierno institucional y diseño de instrumentos del Sistema Integrado de Gestión.

Tu objetivo es continuar y cerrar de forma técnicamente rigurosa el proyecto de **accesibilidad digital de MinAmbiente**, utilizando como baseline toda la información, documentos, decisiones y restricciones consignadas en este archivo y en las fuentes adjuntas.

No empieces de cero. No generes un manual genérico de accesibilidad. No conviertas cada requisito normativo en un documento independiente. No mezcles este trabajo con el proyecto del **Catálogo Institucional de Sistemas de Información**, su arquitectura documental, sus matrices, su REQUEST/OUTLINE ni sus decisiones.

Trabaja con estas reglas obligatorias:

1. **Primero evidencia, después conclusión.** Toda afirmación normativa, funcional o institucional debe poder rastrearse a una fuente identificada. Si una fuente no soporta una afirmación, indícalo.
2. **Diferencia cuatro tipos de conclusión:** `VERIFICADA`, `DERIVADA`, `PROPUESTA` y `PENDIENTE DE DECISIÓN`. No presentes una responsabilidad propuesta como una función jurídica ya asignada.
3. **Jerarquiza las fuentes.** Una norma vigente prevalece sobre una guía; un instrumento institucional vigente prevalece sobre un borrador; la versión más reciente de un borrador sustituye a la anterior solo en las materias que expresamente haya cambiado.
4. **No confundas accesibilidad con gobierno general del portal.** El Modelo de Gobierno del Portal V0.3 separó ambos asuntos. Usa ese documento para conocer fronteras de responsabilidad, pero desarrolla accesibilidad en instrumentos especializados.
5. **Línea jurídica mínima:** la Resolución MinTIC 1519 de 2020 y su Anexo 1 exigen WCAG 2.1 nivel AA. WCAG 2.2 puede usarse como extensión institucional o mejora, pero no debe sustituir silenciosamente la base jurídica 2.1 AA.
6. **Conformidad sin promedios.** Un promedio, puntaje o porcentaje puede servir para priorización o gestión, pero no sustituye la verificación de todos los criterios A y AA aplicables al alcance declarado. Un estado `Parcial` se considera no conforme para efectos de declaración de cumplimiento.
7. **Accesibilidad desde el origen y no regresión.** Todo contenido, documento, plantilla, componente, formulario o cambio nuevo debe incorporar controles antes de publicarse o pasar a producción. Una liberación no debe reintroducir barreras ya corregidas.
8. **Separación de responsabilidades.** Distingue propiedad sustantiva del contenido, gestión editorial, requerimientos de ciudadanía/transparencia, propiedad funcional del trámite o servicio, custodia técnica, ejecución técnica y aseguramiento independiente.
9. **Reutilizar antes que crear.** Antes de proponer un nuevo manual, guía, procedimiento, formato o matriz, demuestra qué brecha concreta no cubren los instrumentos vigentes.
10. **Documentación proporcional.** El objetivo es una arquitectura mínima, mantenible y auditable; no una colección de documentos para administrar otros documentos.
11. **Las herramientas automáticas son apoyo.** La evaluación debe combinar revisión manual, teclado, foco, zoom/reflujo, tecnología de asistencia, formularios, contraste, documentos y multimedia, además de escaneos automáticos.
12. **No usar “certificación” sin competencia formal.** Preferir `evaluación de accesibilidad`, `informe de conformidad` y `declaración de accesibilidad`, según corresponda.
13. **Los terceros no eliminan la responsabilidad institucional.** Cuando exista contenido o componente de terceros, registra nivel de control, obligación contractual, alternativa accesible, riesgo, responsable y fecha de revisión.
14. **Lenguaje claro y trazabilidad.** Redacta en español profesional, preciso y comprensible; cita fuente, sección y página cuando sea posible; distingue hechos, análisis y propuestas.
15. **No inventes tecnologías actuales.** No asumas CMS, versión de PHP, base de datos, hosting, herramientas o arquitectura si no aparecen verificadas en una fuente vigente.
16. **No reabras decisiones cerradas por preferencia estilística.** Solo cuestiona una decisión si encuentras nueva evidencia normativa, institucional o técnica que la contradiga o haga inviable.

### Resultado esperado de tu trabajo

Debes producir, en este orden:

1. una revisión de baseline y conflictos de fuentes;
2. una arquitectura documental mínima para accesibilidad;
3. una matriz breve de decisiones `VERIFICADA / DERIVADA / PROPUESTA / PENDIENTE`;
4. un OUTLINE del instrumento o instrumentos que realmente deban formalizarse;
5. una propuesta de ajuste del formato F-A-SCD-26 y del método de evaluación;
6. una ruta de implementación y cierre con responsables, evidencia y criterios de aceptación;
7. únicamente después de validar lo anterior, los borradores institucionales definitivos.

Si detectas una omisión que pueda producir reproceso, contradicción normativa o sobredocumentación, debes señalarla **antes** de incorporarla al diseño final.

---

## 1. SOLICITUD ORIGINAL Y OBJETIVO DEL PROYECTO

El proyecto busca establecer un esquema institucional sostenible para que el portal web y los contenidos digitales de MinAmbiente cumplan las obligaciones de accesibilidad aplicables, y para que el cumplimiento pueda mantenerse, verificarse y demostrarse mediante responsabilidades claras, pruebas reproducibles y evidencia trazable.

El objetivo no es producir una “certificación” documental ni declarar cumplimiento por la sola existencia de listas de chequeo. La documentación debe habilitar el control; la conformidad solo se alcanza cuando los requisitos aplicables han sido implementados y verificados sobre el alcance definido.

El proyecto debe resolver, como mínimo:

- qué estándar mínimo se exige y cómo se mide;
- qué alcance institucional se evalúa;
- quién define requisitos, quién implementa, quién verifica, quién aprueba y quién conserva evidencia;
- cómo se gestionan barreras de contenido frente a barreras de diseño/código;
- cómo se incorporan requisitos de accesibilidad en publicaciones y cambios nuevos;
- cómo se remedia el contenido heredado;
- qué instrumentos institucionales son realmente necesarios;
- cómo se evita duplicar el Manual de Publicación, el Manual de Comunicaciones, los procedimientos técnicos o los instrumentos del SIG;
- cómo se prepara y mantiene una declaración de accesibilidad sustentada en evidencia.

---

## 2. FRONTERA DEL PROYECTO — NO MEZCLAR CON EL CATÁLOGO DE SISTEMAS

Este proyecto es **Accesibilidad**.

Existe otro proyecto independiente para el **Catálogo Institucional de Sistemas de Información y Soluciones Tecnológicas**. Sus matrices, modelos de datos, arquitectura documental, Ficha de Caracterización, REQUEST, OUTLINE, decisiones M/R/C/F y expediente técnico no forman parte de este trabajo.

Solo puede citarse un instrumento del dominio de sistemas cuando tenga una relación directa y demostrable con el portal o con una actividad técnica de accesibilidad. No importar al proyecto de accesibilidad la arquitectura documental del Catálogo ni utilizarla como plantilla conceptual automática.

La regla de separación es estricta:

> Accesibilidad web y contenidos digitales = este proyecto.  
> Catálogo institucional de sistemas = proyecto distinto.

---

## 3. ESTADO ACTUAL Y EVOLUCIÓN DE LOS BORRADORES

### 3.1 Borrador V0.1 — 30/07/2026

La primera versión consolidó un modelo federado de gobierno y accesibilidad del portal, incorporó el diagnóstico de accesibilidad, revisión del Manual de Publicación M-E-GET-02 V3, una matriz RACI y una ruta de cumplimiento.

Aportes que siguen siendo útiles para accesibilidad:

- accesibilidad desde el origen;
- conformidad sin promedios;
- separación de responsabilidad editorial, funcional y técnica;
- línea base verificable;
- priorización de remediación;
- pruebas manuales y automáticas;
- evidencia antes/después;
- declaración solo después de verificación completa del alcance.

### 3.2 Borrador V0.2 — 04/08/2026

La V0.2 amplió roles, responsabilidades críticas, rutas de cumplimiento, criterios de cierre y arquitectura documental. Fue la versión más desarrollada en materia de accesibilidad.

Decisiones relevantes de esta versión:

- el Grupo de Comunicaciones lideraba la orientación editorial general;
- UCGA se proponía como líder de requisitos funcionales de accesibilidad, lenguaje claro, transparencia y experiencia ciudadana;
- OTIC ejercía custodia técnica, cambios, pruebas y gestión técnica de proveedores;
- cada dependencia respondía por la exactitud, vigencia, legalidad y oportunidad de la información que genera;
- cada dueño funcional de trámite, formulario o servicio debía aceptar funcionalmente su comportamiento;
- `Parcial` se trataba como no conforme para declarar;
- la línea jurídica mínima se mantenía en WCAG 2.1 A/AA;
- WCAG 2.2 se conservaba como extensión o mejora institucional;
- se evitaba usar “certificación” salvo competencia formal.

La V0.2 propuso inicialmente una arquitectura documental integrada. Esa propuesta **no debe adoptarse automáticamente**, porque la versión V0.3 cambió la frontera entre gobierno general del portal y accesibilidad.

### 3.3 Borrador V0.3 — 12/08/2026

La V0.3 reorganizó el trabajo alrededor del **gobierno general del portal** y estableció expresamente que la accesibilidad web no sería el componente central de ese modelo, sino que sus obligaciones debían mantenerse en instrumentos específicos de cumplimiento y calidad digital.

Por tanto, para este proyecto:

- la V0.3 **prevalece** sobre la V0.2 en decisiones de gobierno general del portal que hayan sido modificadas;
- la V0.2 sigue siendo una fuente de diseño para la ruta y controles específicos de accesibilidad;
- no debe volver a incrustarse todo el estándar de accesibilidad dentro del Modelo de Gobierno del Portal;
- el Modelo de Gobierno debe referenciar los instrumentos especializados de accesibilidad, no duplicarlos.

La V0.3 también refinó la clasificación de responsabilidades:

- `función existente y verificada`;
- `responsabilidad derivada`;
- `responsabilidad propuesta`;
- `requiere formalización`;
- `requiere decisión institucional`.

Esta clasificación debe preservarse.

---

## 4. DECISIONES DE PARTIDA YA CERRADAS

Salvo evidencia nueva que las contradiga, las siguientes decisiones se consideran baseline:

### 4.1 Estándar legal mínimo

La Resolución MinTIC 1519 de 2020, artículo 3 y Anexo 1, establece como mínimo WCAG 2.1 nivel AA para los sujetos obligados y aplica a procesos de actualización, estructuración, reestructuración, diseño y rediseño de portales, sedes electrónicas y contenidos.

**Regla:** el modelo de evaluación institucional debe distinguir:

- criterios WCAG 2.1 A/AA = base obligatoria para la declaración institucional;
- criterios WCAG 2.2 adicionales = mejora institucional, extensión o control complementario, sin confundirlos con la base legal mínima.

### 4.2 Conformidad criterio a criterio

La conformidad no se decide por promedio. Para el alcance declarado deben cumplirse todos los criterios A y AA aplicables sobre páginas completas y procesos completos.

Los puntajes pueden mantenerse para priorización gerencial, pero deben estar separados del resultado de conformidad.

### 4.3 Tratamiento de “Parcial”

`Parcial` puede existir como estado interno de avance, pero para declarar cumplimiento se computa como **no conforme** hasta que el criterio aplicable esté completamente satisfecho.

### 4.4 Accesibilidad desde el origen

Todo contenido y cambio nuevo debe cumplir los controles aplicables antes de publicarse o liberarse. El proyecto no puede limitarse a auditorías periódicas posteriores.

### 4.5 No regresión

Toda liberación o modificación relevante debe demostrar que no reintroduce barreras previamente corregidas, especialmente en plantillas y componentes reutilizables.

### 4.6 Evidencia reproducible

Un hallazgo válido debe incluir, como mínimo:

- criterio WCAG asociado;
- URL o activo afectado;
- página, componente, documento o proceso;
- fecha;
- entorno;
- navegador/dispositivo cuando aplique;
- zoom o configuración relevante;
- tecnología de asistencia o herramienta utilizada;
- pasos de reproducción;
- resultado esperado y observado;
- evidencia;
- tipo de barrera;
- severidad/prioridad;
- responsable;
- fecha objetivo;
- criterio de aceptación;
- estado de cierre.

### 4.7 Clasificación de hallazgos

Separar al menos:

- contenido/editorial;
- diseño/UX;
- código/componente;
- documento digital;
- multimedia;
- formulario/trámite;
- infraestructura/configuración técnica cuando corresponda;
- tercero o componente externo.

Esta separación debe permitir asignar correctamente la corrección.

### 4.8 Herramientas automáticas

Los escaneos automáticos apoyan la detección, pero no sustituyen la verificación manual ni las pruebas con teclado y tecnologías de asistencia.

### 4.9 Terminología institucional

Usar preferentemente:

- evaluación de accesibilidad;
- informe de conformidad;
- declaración de accesibilidad;
- hallazgo/barrera;
- remediación;
- evidencia de verificación.

Evitar `certificación de accesibilidad` salvo que exista una competencia formal y un mecanismo jurídico/técnico que permita usar ese término.

### 4.10 Terceros

Para componentes, contenidos, plataformas o servicios de terceros deben registrarse:

- nivel de control institucional;
- obligación contractual o mecanismo de exigibilidad;
- criterio incumplido;
- alternativa accesible temporal, cuando sea viable;
- riesgo residual;
- responsable de seguimiento;
- fecha de revisión/remediación.

### 4.11 No sobredocumentar

No crear once manuales o formatos independientes. Toda nueva pieza debe justificar su función única y su relación con instrumentos ya existentes.

---

## 5. INTERFACES DE GOBIERNO QUE DEBEN RESPETARSE

La accesibilidad es transversal y no convierte a una sola dependencia en propietaria de todo el portal.

### 5.1 Grupo de Comunicaciones — GCOM

Baseline de gobierno general del portal:

- liderazgo editorial general;
- coherencia del canal;
- estructura/taxonomía y backlog funcional general del CMS, **si se formaliza** la recomendación de V0.3;
- revisión editorial en su ámbito;
- administración funcional/editorial de secciones generales según acto o instrumento que se adopte.

Límite: no responde por la sustancia de información ajena ni administra infraestructura, código o servidores.

### 5.2 UCGA

Funciones de referencia:

- transparencia y acceso a información pública;
- relación con ciudadanía;
- orientación y seguimiento en su ámbito;
- apoyo a publicación/actualización de información bajo sus competencias.

La V0.2 proponía a UCGA como líder funcional de accesibilidad. Dado que V0.3 separó accesibilidad del modelo general, esta asignación debe tratarse ahora como **PROPUESTA A REVALIDAR**, no como función jurídica cerrada, salvo que una fuente institucional vigente la asigne expresamente.

### 5.3 OTIC

Baseline técnico:

- arquitectura;
- infraestructura;
- CMS como plataforma técnica;
- seguridad técnica;
- ambientes;
- monitoreo;
- respaldo y continuidad;
- cambios y despliegues;
- integraciones;
- mantenimiento tecnológico;
- gestión técnica de proveedores;
- pruebas técnicas y evidencias asociadas.

Límite: OTIC no define la veracidad del contenido ni las reglas de negocio del trámite.

### 5.4 Dependencia propietaria del contenido, trámite o servicio — DPC

Responsabilidades de origen:

- exactitud y vigencia de su información;
- reserva y tratamiento sustantivo correspondiente;
- propiedad intelectual/derechos de uso cuando aplique;
- reglas funcionales del trámite o servicio;
- producción/corrección de contenido bajo su competencia;
- aceptación funcional del resultado.

La dependencia propietaria no debe transferir su responsabilidad sustantiva al editor, a UCGA, a GCOM o a OTIC por el solo hecho de que estos intervengan en la publicación.

### 5.5 Secretaría General / alta dirección / instancia competente

Debe intervenir en:

- adopción formal cuando corresponda;
- resolución de conflictos de competencia;
- priorización de recursos y escalamiento institucional;
- aprobación de excepciones críticas, cuando el modelo adoptado así lo determine.

No debe convertirse en aprobador de cada publicación o cambio ordinario.

### 5.6 SIG, Jurídica, Seguridad Digital, Protección de Datos, Gestión Documental y OCI

Su intervención debe activarse por competencia y riesgo, no como revisión indiscriminada de toda publicación.

- SIG: control documental, versiones, adopción/anulación y coherencia con procesos.
- Jurídica/datos/seguridad/gestión documental: controles especializados cuando aplique.
- OCI: aseguramiento independiente; no debe asumir gestión ni aprobar el trabajo que posteriormente audita.

---

## 6. JERARQUÍA Y USO DE LAS FUENTES

Aplicar la siguiente jerarquía práctica.

### Nivel 1 — Norma obligatoria

Usar como base jurídica principal:

1. `resolucion_mintic_1519_2020.pdf`.
2. Anexo 1 de la Resolución 1519 — `Directrices de accesibilidad web`.

Otras normas citadas en los documentos deben verificarse en su texto vigente antes de usarlas como fundamento decisorio: Ley 1712 de 2014, Decreto 1081 de 2015, Decreto 1078 de 2015, Decreto 767 de 2022, Ley 1618 de 2013, Ley 1680 de 2013 y demás que correspondan.

### Nivel 2 — Guías técnicas oficiales

- `Guía para la implementación de accesibilidad web — WCAG 2.1 Nivel AA, Versión 2, octubre 2022`.
- `Condiciones mínimas técnicas y de seguridad digital — Anexo 3 de la Resolución 1519 de 2020`.
- `Lineamientos para estandarizar ventanillas únicas, portales de programas transversales y sedes electrónicas`.
- `Guía de Lenguaje Claro para Servidores Públicos de Colombia`.

Estas fuentes apoyan implementación, criterios de aceptación, diseño de controles y lenguaje. No reemplazan la jerarquía normativa.

### Nivel 3 — Instrumentos institucionales vigentes de MinAmbiente

Cuando estén disponibles, revisar antes de modificar o crear instrumentos paralelos:

- `M-E-GET-02 V3 — Manual de Publicación de Contenidos en el Portal Web Institucional` — vigencia 13/10/2022.
- `M-E-GCE-01 V4 — Manual de Comunicaciones Estratégicas` — vigencia 11/06/2026.
- `P-E-GCE-02 V7 — Gestión de la comunicación pública interna y externa` — vigencia 30/04/2026.
- Manual de Identidad Visual Ambiente 2024.
- Resolución MinAmbiente 1019 de 2023 — funciones UCGA.
- Decreto 3570 de 2011 — estructura y funciones del Ministerio.
- Resolución MinAmbiente 0401 de 2026 — estructura/planta, cuando aplique.
- Instrumentos vigentes de seguridad digital, gestión documental, contratación/supervisión y SIG que afecten la solución.

### Nivel 4 — Diagnóstico institucional

- `F-A-SCD-26_V3 (Eval, Página Web MIN Ambiente) 30-jun-2026).pdf`.

Este archivo es una línea base de diagnóstico, no una norma. Usa WCAG 2.2 y puntajes. Debe ser normalizado para separar:

- cumplimiento jurídico WCAG 2.1 A/AA;
- extensión WCAG 2.2;
- estado de gestión;
- prioridad;
- evidencia reproducible.

No interpretar su promedio como declaración de conformidad.

### Nivel 5 — Borradores de trabajo

- `Borrador_Modelo_Gobierno_Portal_Web_Accesibilidad_MinAmbiente_V0.1.docx`.
- `Borrador_Modelo_Gobierno_Portal_Web_Accesibilidad_MinAmbiente_V0.2_Reunion.docx`.
- `Borrador_Modelo_Gobierno_Portal_Web_MinAmbiente_V0.3_Reunion.docx`.

Los borradores son evidencia de análisis y decisiones de trabajo. No son normas ni instrumentos adoptados.

---

## 7. HECHOS Y REQUISITOS EXTRAÍDOS DE LAS FUENTES PRINCIPALES

### 7.1 Resolución 1519 de 2020

Aspectos que el trabajo debe respetar:

- el objeto incluye publicación/divulgación, accesibilidad web, seguridad digital y datos abiertos;
- el artículo 3 exige estándares AA de WCAG 2.1 conforme al Anexo 1;
- el requisito aplica a actualizaciones, estructuraciones, reestructuraciones, diseño y rediseño, así como a contenidos existentes;
- la resolución incluye además obligaciones sobre información digital archivada y seguridad digital que pueden afectar el ciclo de vida del portal y sus contenidos.

### 7.2 Directrices de Accesibilidad Web — Anexo 1

Principios y reglas relevantes:

- Perceptible, Operable, Comprensible y Robusto;
- permanencia de la accesibilidad;
- integralidad de la implementación: no basta con una página de inicio accesible si los contenidos internos no lo son;
- estudiar criterios antes de implementar;
- todo lo nuevo debe nacer accesible;
- debe existir un plan para incorporar accesibilidad en información ya publicada;
- la accesibilidad debe mantenerse en el tiempo;
- incluye criterios para páginas y para documentos digitales publicados en web.

### 7.3 Guía para la implementación de accesibilidad web — 2022

Debe usarse como fuente de criterios de aceptación y ejemplos de implementación. Entre otros, aborda:

- alternativas textuales;
- multimedia;
- estructura semántica;
- encabezados;
- orden de lectura;
- orientación y responsive;
- propósito de campos;
- uso del color;
- control de audio;
- contraste mínimo;
- zoom y reflujo;
- teclado;
- navegación;
- errores de formularios;
- compatibilidad con tecnologías de asistencia.

### 7.4 Seguridad digital — Anexo 3

La accesibilidad no puede diseñarse aislada de seguridad. El Anexo 3 exige, entre otros:

- controles de seguridad durante el ciclo de vida;
- autenticación, roles, privilegios y separación de funciones;
- hardening;
- actualización de software, frameworks y plugins;
- monitoreo de seguridad;
- respaldos;
- logs;
- conexiones seguras;
- controles de formularios;
- continuidad;
- buenas prácticas de desarrollo seguro.

Los controles de accesibilidad que alteren formularios, autenticación, mensajes, componentes o infraestructura deben coordinarse con estas exigencias.

### 7.5 Lenguaje claro

La Guía de Lenguaje Claro orienta a:

- pensar en la audiencia;
- organizar, escribir, revisar y validar;
- usar estructura clara;
- oraciones más simples;
- voz activa;
- palabras comprensibles;
- información relevante y suficiente.

La accesibilidad cognitiva y la comprensibilidad de los contenidos deben incorporar este enfoque sin convertir la guía en un duplicado del Manual de Comunicaciones.

### 7.6 Procedimiento P-E-GCE-02 V7

El flujo de comunicación institucional ya contempla:

- recepción de solicitudes de divulgación;
- Consejo de Redacción;
- producción de productos;
- revisión por articuladores;
- revisión/aprobación final del Grupo de Comunicaciones;
- monitoreo e informe de gestión;
- acciones de mejora.

El control de accesibilidad para contenidos web debe integrarse mediante puntos de control y responsabilidades claras, evitando crear un circuito editorial paralelo contradictorio.

---

## 8. DIAGNÓSTICO F-A-SCD-26 — TRATAMIENTO REQUERIDO

El diagnóstico aplicado al portal en junio de 2026 es una fuente relevante para identificar barreras, pero debe revisarse metodológicamente antes de usarlo para declaraciones institucionales.

Problemas ya identificados:

1. usa WCAG 2.2 mientras la obligación jurídica mínima referenciada por la Resolución 1519 sigue siendo WCAG 2.1 AA;
2. incluye niveles A, AA y AAA en un esquema que puede mezclar lo obligatorio con lo adicional;
3. utiliza puntajes/promedios que pueden inducir a concluir cumplimiento global;
4. conserva `Parcial` como categoría de avance, que no equivale a conformidad;
5. debe fortalecer la trazabilidad de cada hallazgo a URL, prueba, evidencia y responsable;
6. debe permitir separar barreras de contenido, diseño y código;
7. debe soportar la remediación y la prueba de cierre, no solo el diagnóstico inicial.

### Ajuste esperado del formato

El nuevo diseño debe permitir, como mínimo, estas dimensiones:

| Dimensión | Contenido esperado |
|---|---|
| Identificación | URL/activo, sección, propietario, tipo de contenido/proceso |
| Norma | criterio WCAG, nivel, versión base 2.1, equivalencia 2.2 cuando aplique |
| Aplicabilidad | aplica / no aplica + justificación |
| Resultado | conforme / no conforme / parcial interno / no evaluado |
| Prueba | método, herramienta, dispositivo, navegador, tecnología de asistencia |
| Evidencia | captura, log, archivo, descripción reproducible |
| Hallazgo | descripción precisa y tipo de barrera |
| Riesgo/prioridad | P0-P3 u otra escala institucional definida |
| Tratamiento | corrección, alternativa, responsable, fecha objetivo |
| Aceptación | criterio de cierre y evidencia posterior |
| Estado | abierto / en tratamiento / listo para verificar / cerrado |
| Trazabilidad | fecha, evaluador, versión, revalidación |

No agregar campos sin demostrar que sirven para decidir, corregir, verificar o auditar.

---

## 9. CONJUNTO MÍNIMO DE PRUEBAS

El método institucional debe contemplar, al menos:

1. escaneo automático como apoyo;
2. navegación completa por teclado;
3. orden de foco y foco visible;
4. ausencia de trampas de teclado;
5. zoom al 200 % y reflujo sin pérdida de contenido/funcionalidad;
6. lector de pantalla en navegación, formularios y mensajes de estado;
7. contraste de texto y componentes aplicables;
8. uso no exclusivo del color;
9. textos alternativos y equivalentes;
10. áreas accionables y controles interactivos;
11. contenido que aparece al foco o puntero;
12. encabezados y estructura semántica;
13. formularios: etiquetas, instrucciones, errores, sugerencias, confirmación y prevención de errores;
14. documentos Office y PDF publicados;
15. audio, video, subtítulos, transcripciones y demás alternativas aplicables;
16. pruebas de regresión de plantillas y componentes reutilizables;
17. validación especializada o con usuarios para servicios críticos cuando sea viable y aporte evidencia real.

El método debe registrar exactamente qué pruebas se ejecutaron, no limitarse a marcar una casilla general de “cumple”.

---

## 10. PRIORIZACIÓN DE REMEDIACIÓN

Conservar una priorización simple orientada a riesgo e impacto.

### P0 — Bloqueante

Barreras que impiden completar una tarea esencial, operar por teclado, acceder a información crítica, recibir mensajes indispensables o que puedan generar un riesgo significativo para la persona usuaria.

Tratamiento: corrección inmediata o alternativa accesible documentada mientras se corrige.

### P1 — Alta

Incumplimientos A/AA frecuentes, presentes en plantillas/componentes reutilizados o con alto impacto ciudadano.

Tratamiento: corregir con prioridad alta y prueba de regresión.

### P2 — Media

Barreras localizadas con impacto moderado o cuya corrección depende de una intervención programada.

### P3 — Mejora

Aspectos adicionales, criterios superiores o mejoras que no sustituyen los requisitos A/AA aplicables.

Claude debe validar si esta taxonomía requiere ajuste al sistema de riesgos o priorización institucional existente antes de formalizarla.

---

## 11. ARQUITECTURA DOCUMENTAL OBJETIVO — HIPÓTESIS A VALIDAR

La arquitectura debe ser **más simple que la propuesta inicial de V0.2** y coherente con la separación realizada en V0.3.

La hipótesis preferida es la siguiente:

```text
                 MARCO GENERAL DEL PORTAL
       Modelo de Gobierno + M-E-GET-02 actualizado
                     (referencia y roles)
                              │
                              ▼
          ESTÁNDAR INSTITUCIONAL DE ACCESIBILIDAD
       requisitos + criterios + contenido + documentos
                              │
                              ▼
       PROCEDIMIENTO DE EVALUACIÓN Y REMEDIACIÓN
   alcance → prueba → hallazgo → corrección → aceptación
                              │
               ┌──────────────┼──────────────┐
               ▼              ▼              ▼
        F-A-SCD-26        Backlog/evidencia  Declaración
         ajustado            vivo             vigente
```

### 11.1 Instrumento A — Estándar/Guía Institucional de Accesibilidad Digital

Función propuesta:

- establecer qué debe cumplirse;
- adoptar WCAG 2.1 A/AA como baseline legal;
- mapear WCAG 2.2 como extensión institucional cuando se decida;
- fijar reglas de accesibilidad para contenido, documentos, multimedia, formularios, componentes y terceros;
- incorporar accesibilidad desde el origen y no regresión;
- referenciar, no copiar íntegramente, los estándares oficiales.

Debe ser estable y relativamente breve. Los ejemplos operativos pueden ir en anexos o material de apoyo.

### 11.2 Instrumento B — Procedimiento de Evaluación, Remediación, Aceptación y Declaración

Función propuesta:

- definir el ciclo operativo de cumplimiento;
- determinar alcance e inventario;
- ejecutar evaluación;
- registrar hallazgos;
- priorizar y asignar tratamiento;
- implementar correcciones;
- verificar cierre;
- gestionar excepciones/terceros;
- preparar declaración;
- programar reevaluación y control de regresión.

Antes de crear este procedimiento como documento nuevo, verificar si puede integrarse razonablemente en un procedimiento institucional vigente sin perder claridad ni trazabilidad.

### 11.3 Instrumento C — F-A-SCD-26 ajustado

Función:

- registro estructurado de evaluación y seguimiento;
- no convertirse en manual;
- separar conformidad de prioridad/puntaje;
- conservar evidencia y trazabilidad.

### 11.4 Registros vivos

Evitar convertir información dinámica en capítulos rígidos de un manual. Mantener como registros, cuando aplique:

- inventario del alcance evaluado;
- mapa de propietarios;
- backlog de hallazgos;
- repositorio de evidencias;
- excepciones/terceros;
- historial de reevaluaciones;
- declaración de accesibilidad vigente y versiones anteriores conforme a gestión documental.

### 11.5 Relación con M-E-GET-02 y Modelo de Gobierno del Portal

El Manual de Publicación o su versión actualizada debe:

- referenciar el estándar y el procedimiento de accesibilidad;
- incorporar puntos de control antes de publicar;
- señalar responsabilidades y escalamiento;
- no reproducir toda WCAG ni duplicar el método de evaluación.

El Modelo de Gobierno del Portal debe mantener únicamente las interfaces de responsabilidad necesarias.

---

## 12. RUTA DE CUMPLIMIENTO A CONSERVAR Y DEPURAR

Usar como baseline la ruta desarrollada en V0.2, ajustándola a la nueva arquitectura documental.

### Fase 0 — Mandato y decisión

Definir:

- autoridad de adopción;
- alcance preliminar;
- actores;
- responsable funcional de accesibilidad o mecanismo de coordinación;
- custodio técnico;
- mecanismo de escalamiento.

**Cierre:** decisión formal suficiente para iniciar el trabajo.

### Fase 1 — Gobierno y adopción

- validar instrumentos existentes;
- aprobar la arquitectura mínima;
- formalizar roles y enlaces;
- definir repositorio de evidencia;
- definir recursos, cronograma y tratamiento de terceros.

**Cierre:** instrumentos y responsabilidades formalizados conforme al SIG.

### Fase 2 — Alcance e inventario

Inventariar, según corresponda:

- dominios/subdominios;
- micrositios;
- plantillas;
- páginas/procesos;
- formularios;
- documentos;
- multimedia;
- componentes/terceros;
- propietarios;
- criticidad;
- fecha de revisión.

**Cierre:** alcance identificado y con propietario.

### Fase 3 — Línea base verificable

- normalizar F-A-SCD-26;
- evaluar WCAG 2.1 A/AA;
- mapear 2.2 sin mezclar resultados;
- registrar evidencia reproducible;
- crear backlog inicial.

**Cierre:** ningún hallazgo genérico sin activo, prueba y responsable.

### Fase 4 — Controles preventivos

- checklist de publicación;
- plantillas accesibles;
- reglas para PDF/Office;
- alternativas textuales;
- lenguaje claro;
- requisitos de formularios;
- criterios contractuales;
- control de cambios nuevos.

**Cierre:** lo nuevo no ingresa sin el control aplicable.

### Fase 5 — Planificación de remediación

- priorizar;
- estimar esfuerzo;
- identificar dependencias;
- asignar responsable y fecha;
- definir criterio de aceptación.

**Cierre:** todos los hallazgos tienen tratamiento definido.

### Fase 6 — Remediación

- corregir contenido;
- corregir plantillas/componentes/código;
- ajustar documentos y multimedia;
- corregir formularios;
- gestionar terceros;
- ejecutar pruebas en ambiente adecuado.

**Cierre:** evidencia antes/después y resultado listo para verificación.

### Fase 7 — Verificación y aceptación

- repetir pruebas aplicables;
- validar páginas/procesos completos;
- ejecutar regresión;
- cerrar solo con evidencia.

**Cierre:** todos los criterios A/AA aplicables del alcance objetivo están conformes o existe un tratamiento formal que impide declarar ese alcance como conforme.

### Fase 8 — Declaración y operación continua

- preparar declaración sustentada;
- publicar por el canal autorizado;
- mantener canal de reporte de barreras;
- revisar ante cambios significativos y con periodicidad definida;
- conservar historial y evidencia.

**Cierre:** pasa a operación continua, no a “proyecto terminado”.

---

## 13. DECISIONES QUE CLAUDE DEBE TRATAR COMO ABIERTAS

Estas materias no deben cerrarse por inferencia si no aparece evidencia institucional suficiente:

1. **Responsable funcional institucional de accesibilidad.** La V0.2 proponía UCGA; debe verificarse contra funciones vigentes y contra la separación de V0.3.
2. **Instancia que adopta el estándar/procedimiento.** Determinar según naturaleza documental, SIG y competencias.
3. **Alcance exacto de la declaración.** Portal principal, micrositios, trámites, formularios, documentos y/o terceros deben quedar explícitamente definidos.
4. **Tipo documental SIG de cada instrumento.** Estándar, guía, procedimiento, instructivo, formato o anexo debe decidirse según el sistema documental institucional, no por preferencia del redactor.
5. **Periodicidad de reevaluación.** Debe ser proporcional a cambios, criticidad y obligaciones vigentes.
6. **Gobierno del F-A-SCD-26.** Definir quién lo aplica, quién revisa, quién aprueba el cierre y quién conserva evidencia.
7. **Extensión WCAG 2.2.** Decidir si se adopta formalmente como estándar institucional adicional o solo como referencia de mejora.
8. **Tratamiento de terceros.** Verificar cláusulas contractuales y capacidad real de remediación.
9. **Integración con M-E-GET-02.** Decidir el mínimo ajuste requerido para referenciar accesibilidad sin volver a mezclar todo el gobierno general con el estándar especializado.
10. **Canal de reporte ciudadano de barreras.** Identificar el canal institucional vigente y su mecanismo de escalamiento.

Si una de estas decisiones bloquea un documento definitivo, Claude debe dejarla marcada como `PENDIENTE DE DECISIÓN` y proponer exactamente qué evidencia o qué actor debe resolverla.

---

## 14. PRODUCTOS ESPERADOS DE CLAUDE

### 14.1 `REVIEW.md`

Debe contener:

- inventario de fuentes revisadas;
- vigencia/autoridad relativa de cada fuente;
- conflictos o inconsistencias;
- decisiones que se mantienen;
- decisiones que deben descartarse o revalidarse;
- brechas reales;
- riesgos de sobredocumentación;
- lista de preguntas estrictamente bloqueantes.

### 14.2 `OUTLINE.md`

Debe definir, antes de redactar documentos finales:

- arquitectura documental mínima;
- propósito de cada instrumento;
- relación con M-E-GET-02, M-E-GCE-01 y P-E-GCE-02;
- roles y fronteras;
- estructura del estándar;
- estructura del procedimiento;
- estructura del formato F-A-SCD-26;
- registros vivos y evidencias;
- ruta de adopción.

### 14.3 Matriz de trazabilidad normativa y documental

Debe ser breve y funcional. Columnas recomendadas:

| Requisito | Fuente | Evidencia institucional actual | Brecha | Instrumento destino | Responsable propuesto | Estado |
|---|---|---|---|---|---|---|

No crear una matriz gigantesca de múltiples capas si no agrega control real.

### 14.4 Propuesta de F-A-SCD-26

Debe mostrar:

- campos;
- reglas de diligenciamiento;
- estados;
- criterios de cierre;
- tratamiento 2.1/2.2;
- ejemplo mínimo diligenciado.

### 14.5 Borradores institucionales

Solo después de aprobar REVIEW + OUTLINE:

- Estándar/Guía Institucional de Accesibilidad Digital;
- Procedimiento operativo, si la brecha demuestra que debe existir como documento independiente;
- F-A-SCD-26 ajustado;
- anexos/checklists estrictamente necesarios.

---

## 15. REGLAS DE REDACCIÓN Y DISEÑO DE LOS PRODUCTOS

1. Redacción institucional en español, clara y precisa.
2. Evitar párrafos inflados, retórica genérica o introducciones extensas.
3. Definir cada término solo una vez y reutilizarlo de forma consistente.
4. No copiar extensamente WCAG: citar y operacionalizar.
5. Separar obligación, recomendación y buena práctica.
6. Identificar siempre si una asignación es verificada, derivada o propuesta.
7. No afirmar que un documento está “vigente” o “adoptado” si es un borrador.
8. No incluir nombres de tecnologías concretas salvo evidencia actual o decisión de arquitectura vigente.
9. Evitar diagramas decorativos; cada diagrama debe explicar un flujo, una decisión o una dependencia.
10. Las tablas deben usarse cuando faciliten comparación, RACI, trazabilidad o criterios de aceptación; no para convertir toda la narrativa en cuadrículas.
11. Mantener compatibilidad con identidad institucional, pero nunca sacrificar contraste, reflujo, legibilidad o uso no exclusivo del color.
12. Los documentos finales deben ser ellos mismos accesibles: estilos de encabezado, orden de lectura, textos alternativos, tablas simples, enlaces descriptivos, idioma, contraste y metadatos.

---

## 16. CRITERIOS DE CALIDAD / DEFINITION OF DONE

La propuesta se considera lista para validación institucional cuando cumpla simultáneamente:

- [ ] La base normativa de WCAG 2.1 AA está claramente separada de extensiones WCAG 2.2.
- [ ] No se usa un promedio como criterio de conformidad.
- [ ] `Parcial` no se interpreta como conforme.
- [ ] El alcance de evaluación/declaración puede identificarse sin ambigüedad.
- [ ] Cada hallazgo es reproducible y tiene evidencia.
- [ ] Cada hallazgo tiene propietario y criterio de aceptación.
- [ ] Se distingue contenido, diseño, código, documento, multimedia, formulario y tercero.
- [ ] Existe control preventivo para contenido/cambios nuevos.
- [ ] Existe prueba de no regresión.
- [ ] Se definen pruebas manuales y tecnológicas suficientes.
- [ ] Las funciones institucionales se distinguen de las propuestas.
- [ ] No se asigna toda la accesibilidad a una sola dependencia sin fundamento.
- [ ] La arquitectura documental es mínima y no duplica instrumentos existentes.
- [ ] M-E-GET-02 y P-E-GCE-02 se integran por referencia/puntos de control, no mediante circuitos paralelos.
- [ ] Los terceros tienen tratamiento explícito.
- [ ] La declaración de accesibilidad se sustenta en evidencia y alcance.
- [ ] La operación continua tiene responsable, periodicidad y repositorio de evidencia.
- [ ] Los documentos producidos cumplen criterios básicos de accesibilidad documental.
- [ ] No se mezcló contenido del proyecto Catálogo de Sistemas de Información.

---

## 17. REGLAS DE CONTROL DE CAMBIOS PARA ESTA TRANSFERENCIA

Claude debe mantener un registro simple de decisiones con este formato:

| ID | Decisión | Estado | Fuente/fundamento | Cambio frente al baseline | Impacto |
|---|---|---|---|---|---|

Estados permitidos:

- `MANTENER`;
- `AJUSTAR`;
- `DESCARTAR`;
- `NUEVA DECISIÓN`;
- `PENDIENTE`.

Cualquier cambio sobre una decisión cerrada debe explicar:

1. qué fuente nueva lo motiva;
2. qué contradicción o riesgo resuelve;
3. qué documentos se ven afectados;
4. cómo evita reproceso o duplicación.

---

## 18. ORDEN DE TRABAJO RECOMENDADO

No producir todos los documentos de una vez. Seguir este orden:

1. revisar fuentes y construir `REVIEW.md`;
2. reconciliar V0.2 vs V0.3;
3. cerrar frontera de accesibilidad frente a gobierno del portal;
4. confirmar arquitectura documental mínima;
5. cerrar roles pendientes y estados de responsabilidad;
6. diseñar OUTLINE;
7. normalizar F-A-SCD-26;
8. definir método de evaluación/remediación;
9. diseñar estándar/guía;
10. integrar puntos de control con M-E-GET-02 y P-E-GCE-02;
11. validar paquete completo contra criterios de calidad;
12. redactar versiones institucionales para reunión/adopción.

---

## 19. FUENTES QUE DEBEN ACOMPAÑAR ESTE ARCHIVO

### Fuentes ya disponibles en el paquete actual

1. `resolucion_mintic_1519_2020.pdf`
2. `ac4bb25d-d367-46c3-9040-549647303608-Directrices de accesibilidad web.pdf`
3. `ce171797-ab3c-4309-9e15-301ddbd87c66-Guía para la implementación de accesibilidad web.pdf`
4. `3a72055f-0da0-4cd2-85f2-2d77e59237ab-Condiciones mínimas técnicas y de seguridad digital.pdf`
5. `46f182cb-7181-42f8-ba4d-67e5707c5f97-Anexo 1 - Lineamientos generales.pdf`
6. `GUIA DEL LENGUAJE CLARO.pdf`
7. `P-E-GCE-02_V7_copia_controlada.pdf`
8. `f9c9e9b5-7b75-40cd-86e4-2b5d0008b30d-Requisitos mínimos de datos abiertos.pdf` — referencia secundaria; no convertir datos abiertos en objeto central del proyecto.

### Fuentes de proyecto que deben añadirse a Claude cuando estén disponibles

9. `F-A-SCD-26_V3 (Eval, Página Web MIN Ambiente) 30-jun-2026).pdf`
10. `Borrador_Modelo_Gobierno_Portal_Web_Accesibilidad_MinAmbiente_V0.2_Reunion.docx`
11. `Borrador_Modelo_Gobierno_Portal_Web_MinAmbiente_V0.3_Reunion.docx`
12. `M-E-GET-02 V3 — Manual de Publicación de Contenidos en el Portal Web Institucional`
13. `M-E-GCE-01 V4 — Manual de Comunicaciones Estratégicas`
14. Manual de Identidad Visual Ambiente 2024.
15. Resolución MinAmbiente 1019 de 2023.
16. Decreto 3570 de 2011 y demás actos internos vigentes necesarios para validar funciones.
17. Instrumentos vigentes de seguridad digital, gestión documental, contratación/supervisión y SIG que resulten aplicables.

Si una fuente de los numerales 9–17 no está disponible, no inventar su contenido. Marcar la validación como pendiente y trabajar únicamente con lo que pueda probarse.

---

## 20. SALIDA ESPERADA DE LA PRIMERA EJECUCIÓN EN CLAUDE

La primera respuesta de Claude no debe ser un documento institucional terminado. Debe entregar:

1. **Resumen de comprensión del problema** en máximo una página.
2. **Tabla de fuentes y precedencia**.
3. **Conflictos detectados**, en especial V0.2 vs V0.3 y WCAG 2.1 vs uso interno de WCAG 2.2.
4. **Decisiones que considera cerradas**.
5. **Decisiones que siguen abiertas** y por qué.
6. **Arquitectura documental mínima propuesta**, con justificación de cada pieza.
7. **Lista de documentos que NO recomienda crear**, para controlar sobredocumentación.
8. **OUTLINE preliminar**.
9. **Preguntas bloqueantes**, solo si una respuesta es indispensable para continuar sin inventar.
10. **Siguiente acción concreta**.

No redactar versiones finales antes de que el usuario valide esta primera salida.

---

## 21. CRITERIO DE CIERRE DE ESTA FASE

La fase de transferencia se considera completa cuando Claude pueda continuar el proyecto sin depender de conversaciones anteriores para comprender:

- el objetivo;
- la frontera del proyecto;
- la jerarquía de fuentes;
- las decisiones ya cerradas;
- los conflictos que debe reconciliar;
- los roles y sus estados de validación;
- la metodología de conformidad;
- el paquete documental mínimo esperado;
- la ruta de implementación;
- los criterios de aceptación.

El siguiente hito debe ser la aprobación del `REVIEW.md` y del `OUTLINE.md`. Solo después debe iniciarse la redacción de instrumentos institucionales definitivos.
