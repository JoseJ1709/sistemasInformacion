# 08_ESPECIFICACION_FINAL

## 1. Objeto de la especificación

Esta especificación consolida las decisiones conceptuales necesarias para construir materialmente:

1. el libro Excel **F-A-GTI-02 — Catálogo Institucional de Sistemas de Información**;
2. la **F-A-GTI-01 — Ficha de Caracterización**;
3. la **G-A-GTI-01 — Guía de diligenciamiento y administración**.

No deben tomarse decisiones conceptuales nuevas durante la construcción si se sigue este documento junto con `04_Taxonomia_Institucional_SI.md`, `05_Modelo_Datos_Catalogo.md`, `06_Estructura_Ficha_Final.md` y `07_Estructura_Guia_Final.md`.

## 2. Decisiones conceptuales cerradas

1. **FICHA ⊃ CATÁLOGO.**
2. El **Catálogo principal inventaría solamente Sistemas de Información**.
3. Componentes, módulos, APIs, servicios web, interfaces, integraciones, plataformas, servicios tecnológicos y SaaS **no son SI por defecto**.
4. La taxonomía **N1-N8 se sustituye** por:
   - **Clase de inventario A-F** para decidir hoja o artefacto.
   - **Tipo o patrón de SI** para clasificar únicamente los registros que sí son SI.
5. Integraciones e interfaces se normalizan en hoja aparte.
6. Componentes se normalizan en hoja aparte cuando tengan identidad técnica relevante.
7. La Guía absorbe las instrucciones; el Excel no debe llevar hoja de instrucciones independiente.

## 3. Clasificación institucional obligatoria

### 3.1 Clase de inventario A-F

- **A. Sistema de Información** → `Catálogo_SI` + `Ficha`
- **B. Componente de un SI** → `Componentes` o referencia en la Ficha
- **C. Integración / Interfaz** → `Integraciones_Interfaces`
- **D. Plataforma tecnológica** → catálogo/hoja de plataformas o soporte; no `Catálogo_SI`
- **E. Servicio de TI** → catálogo de servicios de TI; no `Catálogo_SI`
- **F. Otro activo tecnológico** → no requiere inventario independiente en este instrumento, salvo decisión posterior

### 3.2 Regla obligatoria de pertenencia al Catálogo_SI

Un activo entra al `Catálogo_SI` solo si:

1. soporta uno o más procesos o servicios institucionales;
2. gestiona información del negocio;
3. tiene responsabilidad funcional y técnica identificables;
4. tiene ciclo de vida y gobierno propios;
5. es reconocible como unidad funcional completa para la entidad.

## 4. Taxonomía funcional del SI

Todo registro en `Catálogo_SI` debe clasificarse en uno de estos tipos o patrones:

- Sistema transaccional
- ERP
- CRM
- BPM / BPMS
- CMS
- Sistema de Gestión Documental
- GIS
- Solución analítica
- Otro SI institucional

### Reglas de frontera ya resueltas

- **Dashboard**: normalmente no es SI; se documenta dentro de una solución analítica o de otro SI.
- **SaaS**: atributo de despliegue, nunca clase principal.
- **API / Servicio web / Interfaz / Integración**: nunca SI.
- **Microservicio / Módulo / Base de datos**: componente o detalle técnico, no SI por defecto.
- **Hub / ESB / iPaaS / Middleware / API Gateway**: plataforma o componente de integración, no SI de negocio.
- **ERP / CRM / BPM / CMS / SGD / GIS**: pueden ser SI cuando constituyen la unidad funcional gobernada; de lo contrario son plataforma o componente.

## 5. Estructura exacta del libro F-A-GTI-02

El libro final debe contener exactamente **7 hojas**:

1. `Catálogo_SI`
2. `Integraciones_Interfaces`
3. `Componentes`
4. `Diccionario`
5. `Listas`
6. `Tablero`
7. `Calidad`

### 5.1 Hojas que no deben construirse

- `Instrucciones`
- `Alertas Caducidad`
- `Avance por Dependencia`
- `Control de Cambios` como hoja operativa
- `Hoja2`

## 6. Estructura exacta de `Catálogo_SI`

`Catálogo_SI` debe tener exactamente **44 columnas**, en este orden:

1. ID_SI
2. Nombre_oficial
3. Sigla_Acronimo
4. Tipo_o_patron_de_SI
5. Categoria_institucional
6. Descripcion_breve
7. Procesos_institucionales_soportados
8. Dependencia_duena_del_proceso
9. Area_responsable_funcional
10. Responsable_funcional
11. Area_responsable_tecnica
12. Responsable_tecnico
13. Estado_del_SI
14. Fecha_salida_produccion
15. Version_actual
16. Modelo_de_despliegue
17. Tipo_de_desarrollo_adquisicion
18. Fabricante_o_proveedor_principal
19. Tipo_de_licenciamiento
20. Soporte_vigente_hasta
21. Estado_ANS_terceros
22. Marco_legal_mandatorio
23. Objetivos_estrategicos_que_apoya
24. Criticidad_operacional
25. Usuarios_activos
26. Cobertura_del_proceso
27. Clasificacion_de_la_informacion
28. Manejo_de_datos_personales
29. Interopera_con_entidades_externas
30. Numero_integraciones_activas
31. Numero_componentes_registrados
32. Valoracion_de_seguridad
33. Nivel_de_riesgo_residual
34. Backup_definido
35. Plan_de_continuidad
36. Estado_documentacion_minima
37. Clasificacion_TIME
38. Tipo_intervencion_recomendada
39. Prioridad_intervencion
40. TCO_anual_total_COP
41. Ratio_TCO_por_usuario_COP
42. Ultima_revision_anual
43. Proxima_revision_programada
44. Vigencia_del_registro

## 7. Reglas de construcción del libro

### 7.1 Reglas para `Integraciones_Interfaces`

- una fila por integración o interfaz relevante;
- enlace obligatorio por `ID_SI_Origen`;
- cuando el destino no sea un SI interno, identificar activo o entidad externa;
- registrar tipo de interfaz, propósito, criticidad y estado.

### 7.2 Reglas para `Componentes`

- una fila por componente que amerite seguimiento independiente;
- enlace obligatorio por `ID_SI_Padre`;
- no inventariar módulos triviales sin valor de gobierno separado;
- registrar tipo, función, estado, versión y soporte si aplica.

### 7.3 Reglas para `Calidad`

Debe administrar:

- completitud del registro;
- hallazgos;
- inconsistencias de vocabulario;
- trazabilidad de migración;
- fechas de detección y cierre.

### 7.4 Reglas para `Tablero`

Debe incluir mínimo:

- total de SI vigentes/históricos;
- distribución por tipo y categoría;
- TIME del portafolio;
- soporte vencido o próximo a vencer;
- TCO total y promedio;
- SI con seguridad desactualizada;
- SI con documentación crítica;
- próximas revisiones programadas.

## 8. Estructura obligatoria de la Ficha F-A-GTI-01

La Ficha final debe tener **12 secciones temáticas más un encabezado documental**:

0. Encabezado y control documental
1. Identificación general del SI
2. Gobierno y responsables
3. Arquitectura funcional y de información
4. Componentes internos del SI
5. Integraciones e interfaces
6. Arquitectura tecnológica y despliegue
7. Ciclo de vida, soporte y operación
8. Seguridad, privacidad y continuidad
9. Calidad, valor y análisis estratégico
10. Dimensión económica y mantenimiento
11. Estado de documentación y evidencias
12. Validación, firmas y control de cambios

> Nota de construcción: el encabezado es previo a las secciones temáticas y no altera la regla de 12 secciones sustantivas.

### 8.1 Regla de contenido

La Ficha debe incluir:

- todos los campos del catálogo del SI correspondiente;
- detalle ampliado de arquitectura, componentes, integraciones, seguridad, TIME y TCO;
- referencias a documentos existentes.

La Ficha no debe duplicar innecesariamente manuales, diagramas o contratos completos: debe **referenciarlos**.

## 9. Estructura obligatoria de la Guía G-A-GTI-01

La Guía final debe tener **12 secciones**:

1. Propósito, alcance y definiciones de uso
2. Base normativa y diferenciación de fuentes
3. Taxonomía institucional y frontera del inventario
4. Árbol de decisión de clasificación
5. Modelo del libro Excel
6. Diligenciamiento de `Catálogo_SI`
7. Diligenciamiento de `Integraciones_Interfaces` y `Componentes`
8. Diligenciamiento de la Ficha
9. Vocabularios controlados y validaciones
10. Ciclo de actualización y eventos disparadores
11. Control de calidad y gobierno del dato
12. Ejemplos mínimos de clasificación y diligenciamiento

## 10. Diferenciación obligatoria de fuentes

Durante la construcción del material final debe preservarse esta distinción:

| Categoría | Qué puede afirmarse |
| --- | --- |
| Obligación MinTIC / Gobierno Digital | Solo lo expresamente soportado por MGGTI, MAE/MRAE, MSPI, Decreto 767 y demás norma oficial citada. |
| Recomendación MinTIC | Lo sugerido por guías o marcos oficiales sin carácter de obligación taxativa de campo. |
| Decisión institucional propuesta | Definiciones de frontera, diseño del libro, campos exactos y reglas de clasificación cerradas en este proyecto. |
| Buena práctica | Complementos técnicos usados cuando MinTIC no define el concepto con suficiente detalle. Incluye el uso de TIME como marco complementario, no como obligación MinTIC. |

## 11. Contradicciones resueltas frente al estado actual

1. El actual inventario mezcla SI con componentes, integraciones, plataformas y servicios; el nuevo modelo los separa.
2. La taxonomía N1-N8 deja de gobernar el catálogo principal.
3. La documentación detallada deja de vivir en múltiples columnas del catálogo y pasa a la Ficha.
4. Las integraciones dejan de almacenarse en texto agregado y pasan a hoja normalizada.
5. Los datos de avance y completitud dejan de contaminar la vista principal y pasan a `Calidad`.
6. Las alertas dejan de requerir hojas ad hoc y pasan a `Tablero` + `Calidad`.

## 12. Criterio de listo para construcción

El diseño queda **listo para construcción** cuando el agente implementador:

1. cree el libro de 7 hojas exactamente como aquí se define;
2. construya `Catálogo_SI` con las 44 columnas en el orden fijado;
3. use la clase de inventario A-F para enrutar cada activo a la hoja o catálogo correcto;
4. construya la Ficha con la estructura definida en `06_Estructura_Ficha_Final.md`;
5. construya la Guía con la estructura definida en `07_Estructura_Guia_Final.md`;
6. mantenga explícita la diferencia entre obligación MinTIC y decisión institucional.

## 13. Fuentes base para construcción

Usar, como mínimo, las fuentes listadas en `04_Taxonomia_Institucional_SI.md`, en especial:

- MGGTI / MGGTI.G.SI
- MAE / MRAE / Resolución 1978 de 2023
- Decreto 767 de 2022
- NIST SP 800-145
- ISO/IEC 2382
- W3C Web Services Architecture
- OASIS SOA Reference Architecture
- ISO 19101 / Esri para GIS
