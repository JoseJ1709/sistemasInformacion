# 07_Estructura_Guia_Final

## 1. Propósito de la Guía final

La **G-A-GTI-01** debe explicar cómo clasificar, registrar, actualizar y controlar la calidad de la información del catálogo y de la ficha, sin convertirse en tratado teórico.

## 2. Alcance de la Guía

La guía debe cubrir únicamente:

1. marco normativo y jerarquía de fuentes;
2. taxonomía institucional y árbol de decisión;
3. reglas de inclusión/exclusión del inventario;
4. diligenciamiento del `Catálogo_SI`;
5. diligenciamiento de `Integraciones_Interfaces` y `Componentes`;
6. diligenciamiento de la Ficha;
7. vocabularios controlados;
8. actualización, revisión, calidad y gobierno.

## 3. Estructura final propuesta de la Guía

### Sección 1 — Propósito, alcance y definiciones de uso

**Debe contener:**

- objetivo de la guía;
- a quién aplica;
- relación entre Catálogo, Ficha y Guía;
- principio `FICHA ⊃ CATÁLOGO`.

### Sección 2 — Base normativa y diferenciación de fuentes

**Debe contener una tabla explícita con cuatro categorías:**

- obligación MinTIC / Gobierno Digital;
- recomendación MinTIC;
- decisión institucional propuesta;
- buena práctica técnica.

**Debe citar al menos:**

- Decreto 767 de 2022 para las definiciones normativas de Sistema de Información, Servicio Tecnológico y Plataforma;
- Resolución 1978 de 2023;
- MGGTI.G.SI como referencia oficial del dominio de gestión de sistemas de información, aclarando cuando la numeración fina de sublineamientos requiera validación directa;
- MAE.G.ASI y MAE.GE.ASI.01 como referencias del dominio ASI, aclarando que no debe asumirse una serie separada `MAE.LI.ASI.01-.03` sin verificación documental directa;
- fuentes complementarias usadas para API, SaaS, microservicio, ESB, GIS y base de datos.

### Sección 3 — Taxonomía institucional y frontera del inventario

**Debe incluir:**

- la decisión de sustituir N1-N8;
- la clase de inventario A-F;
- el tipo o patrón de SI;
- glosario resumido de conceptos;
- reglas de frontera para ERP, CRM, BPM, CMS, SGD, GIS, dashboard, API, microservicio, SaaS y base de datos.

### Sección 4 — Árbol de decisión “¿Este activo entra al Catálogo Institucional de SI?”

**Debe incluir:**

- el árbol cerrado de la Fase 1;
- ejemplos de clasificación correcta;
- errores frecuentes de clasificación.

### Sección 5 — Modelo del libro Excel

**Debe explicar:**

- las 7 hojas del libro;
- la función concreta de cada una;
- qué hojas desaparecen respecto del estado actual;
- por qué integraciones y componentes se normalizan.

### Sección 6 — Instrucciones de diligenciamiento de `Catálogo_SI`

**Debe contener una tabla campo a campo** con, como mínimo:

- nombre del campo;
- qué significa;
- cómo diligenciarlo;
- responsable primario;
- error frecuente;
- si es obligatorio o recomendado.

**Debe cubrir exactamente los 44 campos del modelo final.**

### Sección 7 — Instrucciones para `Integraciones_Interfaces` y `Componentes`

**Debe explicar:**

- cuándo crear un registro en cada hoja;
- cuándo basta con dejar el dato solo en la Ficha;
- cómo manejar cardinalidad uno-a-muchos;
- cómo enlazar por ID con `Catálogo_SI`.

### Sección 8 — Instrucciones de diligenciamiento de la Ficha

**Debe organizarse por las 12 secciones definidas en `06_Estructura_Ficha_Final.md` y explicar:**

- objetivo de cada sección;
- datos mínimos;
- fuentes típicas del dato;
- responsables;
- anexos o evidencias de referencia.

### Sección 9 — Vocabularios controlados y reglas de validación

**Debe incluir:**

- listas controladas del catálogo;
- reglas de formato (IDs, fechas, moneda, listas múltiples);
- validaciones condicionales;
- reglas para “No aplica”, “Desconocido” y vacíos permitidos.

### Sección 10 — Ciclo de actualización y eventos disparadores

**Debe explicar:**

- alta inicial del SI;
- actualización al pasar a producción;
- revisión anual obligatoria;
- actualización por incidentes, vencimientos, cambio normativo, cambio de responsable o retiro.

### Sección 11 — Control de calidad y gobierno del dato

**Debe contener controles mínimos para:**

- completitud;
- consistencia entre Catálogo, Ficha, Integraciones y Componentes;
- validación de vocabulario;
- vigencia de soporte, seguridad y continuidad;
- coherencia del modelo institucional de priorización, TIME complementario y TCO;
- preservación del histórico.

### Sección 12 — Ejemplos mínimos de clasificación y diligenciamiento

**Debe traer solo ejemplos cortos y funcionales**, no casos extensos:

- un SI transaccional;
- una integración API;
- un componente microservicio;
- una plataforma iPaaS;
- una solución analítica / dashboard dependiente.

## 4. Reglas editoriales de la Guía

1. No repetir definiciones largas que ya están en la taxonomía; resumir y referenciar.
2. No volver a explicar teoría general de AE o Gobierno Digital salvo lo necesario para diligenciar bien.
3. No crear tablas duplicadas entre Guía y Diccionario sin función distinta.
4. Usar ejemplos del Ministerio solo cuando aclaren la frontera del inventario.
5. Diferenciar visualmente obligación, recomendación y decisión institucional.

## 5. Resultado de la Fase 3 para la Guía

La Guía final queda definida como un documento operativo de **12 secciones**, centrado en clasificar bien, diligenciar bien y mantener la calidad del instrumento.
