# 06_Estructura_Ficha_Final

## 1. Propósito de la Ficha final

La **Ficha F-A-GTI-01** es el expediente técnico-funcional completo de cada **Sistema de Información**. Debe contener:

- todos los datos del registro correspondiente del `Catálogo_SI`;
- el detalle ampliado que no conviene mantener como columnas del catálogo;
- referencias a artefactos especializados existentes, sin duplicar innecesariamente documentos completos.

## 2. Principios de diseño de la Ficha

1. **Una ficha por SI**, no por componente ni por integración.
2. **La Ficha incorpora el subconjunto del catálogo** para evitar doble captura inconsistente.
3. **Los componentes e integraciones repetibles se listan en tablas**, no como párrafos abiertos.
4. **La Ficha referencia** manuales, diagramas, repositorios, contratos y estudios existentes, en lugar de copiarlos.
5. **La Ficha sirve para auditoría, gobierno y mantenimiento**, no para almacenar detalles efímeros de operación diaria.

## 3. Estructura final propuesta

### 3.1 Encabezado y control documental

| Elemento | Contenido requerido | Tipo |
| --- | --- | --- |
| Código del instrumento | F-A-GTI-01 | Fijo |
| Versión de la ficha | Número de versión de la ficha | Obligatorio |
| Fecha de elaboración / actualización | Fecha de emisión vigente | Obligatorio |
| ID del SI | Igual a `ID_SI` del catálogo | Obligatorio |
| Nombre oficial del SI | Igual al catálogo | Obligatorio |
| Estado de la ficha | Borrador / Vigente / En actualización / Cerrada | Obligatorio |
| Responsable de elaboración | Nombre y cargo | Obligatorio |
| Responsable de aprobación | Nombre y cargo | Obligatorio |

### 3.2 Sección 1 — Identificación general del SI

**Objetivo:** capturar identidad, propósito, clasificación y contexto institucional.

**Campos mínimos:**

- ID_SI
- Nombre_oficial
- Sigla_Acronimo
- Tipo_o_patron_de_SI
- Categoria_institucional
- Descripcion_breve
- Objetivo funcional del SI
- Alcance funcional
- Dependencia_dueña_del_proceso
- Procesos_institucionales_soportados
- Marco_legal_mandatorio
- Objetivos_estrategicos_que_apoya
- Fecha_salida_produccion
- Estado_del_SI
- Vigencia_del_registro

**Información narrativa obligatoria:**

- propósito del SI en lenguaje de negocio;
- problema institucional que resuelve;
- alcance funcional actual y límites explícitos.

**Responsables:** funcional + técnico.

### 3.3 Sección 2 — Gobierno y responsables

**Objetivo:** dejar explícitos los dueños funcionales y técnicos del SI.

**Campos mínimos:**

- Area_responsable_funcional
- Responsable_funcional
- Correo_responsable_funcional
- Area_responsable_tecnica
- Responsable_tecnico
- Correo_responsable_tecnico
- Instancia de gobierno o comité asociado (si existe)
- Dependencia o área de soporte contractual

**Evidencias / referencias:** acto, memorando, designación o práctica vigente que respalde la responsabilidad.

### 3.4 Sección 3 — Arquitectura funcional y de información

**Objetivo:** describir cómo opera el SI sin convertir la Ficha en manual de ingeniería exhaustivo.

**Campos / tablas:**

- Procesos_institucionales_soportados
- Funcionalidades_principales
- Entradas_principales
- Salidas_principales
- Actores internos / externos
- Clasificacion_de_la_informacion
- Manejo_de_datos_personales
- Diccionario resumido de entidades de información críticas (tabla corta)
- Zona(s) de arquitectura MAE/MRAE relacionadas

**Tabla sugerida: datos clave**

| Dato / entidad | Descripción | Fuente / origen | Sensibilidad | Observaciones |
| --- | --- | --- | --- | --- |

**Narrativa requerida:**

- contexto del flujo de información;
- dependencias funcionales relevantes;
- límites del SI respecto de otros sistemas.

### 3.5 Sección 4 — Componentes internos del SI

**Objetivo:** registrar la descomposición técnica o funcional relevante del SI.

**Tabla obligatoria:**

| ID_Componente | Nombre | Tipo | Función | Compartido con otros SI | Estado | Versión | Observaciones |
| --- | --- | --- | --- | --- | --- | --- | --- |

**Regla:**

- si un componente también está en la hoja `Componentes`, la Ficha solo lo referencia por ID y resumen;
- si el componente no amerita inventario independiente, basta la tabla interna de la Ficha.

### 3.6 Sección 5 — Integraciones e interfaces

**Objetivo:** describir de forma normalizada las relaciones del SI con otros activos.

**Tabla obligatoria:**

| ID_Integracion | Origen / destino | Tipo de interfaz | Propósito | Dirección | Entidad externa asociada | Criticidad | Estado |
| --- | --- | --- | --- | --- | --- | --- | --- |

**Campos narrativos mínimos:**

- resumen de interoperabilidad externa;
- dependencias críticas con terceros;
- observaciones sobre intercambio de datos sensibles.

### 3.7 Sección 6 — Arquitectura tecnológica y despliegue

**Objetivo:** capturar el detalle técnico mínimo suficiente para soporte y evolución.

**Campos mínimos:**

- Modelo_de_despliegue
- Tipo_de_arquitectura
- Tipo_de_desarrollo_adquisicion
- Version_actual
- Fabricante_o_proveedor_principal
- Tipo_de_licenciamiento
- Sistemas_operativos_principales
- Lenguajes_principales
- Motores_de_base_de_datos
- Contenerización (sí/no; tecnología)
- CI/CD (sí/no; herramienta)
- Repositorios técnicos / URLs / ubicaciones

**Regla:** rutas de Dockerfile, pipelines u otros artefactos muy volátiles se referencian por enlace, no como campos estructurados obligatorios del catálogo.

### 3.8 Sección 7 — Ciclo de vida, soporte y operación

**Objetivo:** consolidar estado operativo, soporte, contratos y mantenibilidad.

**Campos mínimos:**

- Estado_del_SI
- Fecha_ultima_actualizacion_relevante
- Soporte_vigente_hasta
- Proveedor_de_soporte_actual
- Estado_ANS_terceros
- Indicadores del ANS (si aplica)
- Ventanas de mantenimiento
- Incidentes reportados últimos 12 meses
- Riesgos tecnológicos identificados
- Obsolescencias conocidas
- Evolución prevista

### 3.9 Sección 8 — Seguridad, privacidad y continuidad

**Objetivo:** documentar el cumplimiento mínimo de seguridad y continuidad necesario para gobernanza.

**Campos mínimos:**

- Valoracion_de_seguridad
- Nivel_de_riesgo_residual
- Clasificacion_de_la_informacion
- Manejo_de_datos_personales
- RNBD u otra referencia de cumplimiento cuando aplique
- Backup_definido
- Frecuencia de backup
- RTO y RPO cuando existan
- Plan_de_continuidad
- Controles de acceso relevantes
- Accesibilidad web (si aplica por canal ciudadano)
- Hallazgos o brechas críticas

**Evidencias / referencias:**

- documento de análisis de riesgos;
- plan de continuidad o contingencia;
- referencia a controles MSPI / SGSI / seguridad institucional.

### 3.10 Sección 9 — Calidad, valor y análisis estratégico

**Objetivo:** soportar decisiones de portafolio sin recargar el catálogo principal.

**Subsecciones:**

1. **Valor y cobertura**
   - Usuarios_activos
   - Cobertura_del_proceso
   - Beneficios esperados / observados
2. **Análisis DOFA**
   - fortalezas, debilidades, oportunidades, amenazas
3. **Madurez y satisfacción**
   - nivel de madurez
   - satisfacción de usuarios
4. **TIME detallado**
   - eje valor al negocio
   - eje eficiencia técnica
   - eje costos y riesgos
   - clasificación final
   - justificación
   - tipo de intervención recomendada
   - prioridad_intervencion

### 3.11 Sección 10 — Dimensión económica y mantenimiento

**Objetivo:** dejar trazable la estructura del TCO y los insumos del plan de mantenimiento.

**Tabla obligatoria TCO:**

| Concepto | Valor anual COP | Fuente | Confirmado / estimado | Observaciones |
| --- | --- | --- | --- | --- |
| Licenciamiento |  |  |  |  |
| Soporte y mantenimiento |  |  |  |  |
| Infraestructura |  |  |  |  |
| Evolutivo |  |  |  |  |
| Correctivo |  |  |  |  |
| Otros aprobados por OTIC |  |  |  |  |
| **TCO total** |  |  |  |  |

**Campos adicionales:**

- Tipo_mantenimiento_recomendado
- Periodicidad_mantenimiento_sugerida
- Proxima_revision_programada
- Observaciones para el plan anual de mantenimiento

### 3.12 Sección 11 — Estado de documentación y evidencias

**Objetivo:** verificar disponibilidad de la documentación mínima exigible.

**Tabla obligatoria:**

| Documento / evidencia | Estado | Ubicación o enlace | Responsable de actualizar | Observaciones |
| --- | --- | --- | --- | --- |
| Manual técnico |  |  |  |  |
| Manual de usuario |  |  |  |  |
| Manual de operación |  |  |  |  |
| Requerimientos / historias |  |  |  |  |
| Arquitectura de solución |  |  |  |  |
| Plan de pruebas |  |  |  |  |
| Plan de mantenimiento |  |  |  |  |
| Contrato o acto principal (si aplica) |  |  |  |  |

### 3.13 Sección 12 — Validación, firmas y control de cambios

**Elementos obligatorios:**

- tabla de control de cambios de la ficha;
- validación del responsable técnico;
- validación del responsable funcional;
- validación OTIC / líder designado;
- fecha de aprobación.

## 4. Relación explícita Catálogo ↔ Ficha

### 4.1 Campos del Catálogo que deben replicarse en la Ficha

Todos los 44 campos de `Catálogo_SI` deben existir en la Ficha, ya sea como:

- campo visible en secciones 1–10; o
- dato calculado o resumido incorporado en la portada / secciones de síntesis.

### 4.2 Información que debe vivir en la Ficha y no en el Catálogo

1. funcionalidades detalladas;
2. entradas y salidas;
3. componentes y módulos detallados;
4. integraciones detalladas;
5. stack técnico completo;
6. contactos de correo;
7. DOFA completo;
8. ejes detallados de TIME;
9. desagregación de TCO;
10. ubicaciones detalladas de documentación;
11. evidencias, anexos y referencias.

## 5. Resultado de la Fase 3 para la Ficha

La Ficha final queda estructurada como expediente de **12 secciones** y se confirma que es el artefacto profundo del SI, mientras el catálogo conserva solo la vista consolidada.
