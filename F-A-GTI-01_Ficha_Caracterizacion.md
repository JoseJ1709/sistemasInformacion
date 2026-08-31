# F-A-GTI-01 — Ficha de Caracterización de Sistema de Información

> **Instrumento:** F-A-GTI-01 · Ministerio de Ambiente y Desarrollo Sostenible — OTIC
> **Regla estructural:** `FICHA ⊃ CATÁLOGO`. Esta ficha es el expediente técnico-funcional completo de **un** Sistema de Información. Incluye todos los campos del registro correspondiente de `Catálogo_SI` más el detalle ampliado, y **referencia** (no copia) manuales, diagramas, contratos y estudios existentes.
> **Una ficha por SI.** No se elaboran fichas por componente ni por integración.

---

## 0. Encabezado y control documental

| Elemento | Valor |
| --- | --- |
| Código del instrumento | F-A-GTI-01 |
| Versión de la ficha | |
| Fecha de elaboración / actualización | |
| ID del SI (`ID_SI`, igual al catálogo) | |
| Nombre oficial del SI (igual al catálogo) | |
| Estado de la ficha (Borrador / Vigente / En actualización / Cerrada) | |
| Responsable de elaboración (nombre y cargo) | |
| Responsable de aprobación (nombre y cargo) | |

---

## 1. Identificación general del SI

**Objetivo:** capturar identidad, propósito, clasificación y contexto institucional.

| Campo | Valor |
| --- | --- |
| ID_SI | |
| Nombre_oficial | |
| Sigla_Acronimo | |
| Tipo_o_patron_de_SI | |
| Categoria_institucional | |
| Descripcion_breve | |
| Objetivo funcional del SI | |
| Alcance funcional | |
| Dependencia_duena_del_proceso | |
| Procesos_institucionales_soportados | |
| Marco_legal_mandatorio | |
| Objetivos_estrategicos_que_apoya | |
| Fecha_salida_produccion | |
| Estado_del_SI | |
| Vigencia_del_registro | |

**Narrativa obligatoria:**

- **Propósito del SI en lenguaje de negocio:**
- **Problema institucional que resuelve:**
- **Alcance funcional actual y límites explícitos:**

**Responsables de esta sección:** responsable funcional + responsable técnico.

---

## 2. Gobierno y responsables

**Objetivo:** dejar explícitos los dueños funcionales y técnicos del SI.

| Campo | Valor |
| --- | --- |
| Area_responsable_funcional | |
| Responsable_funcional | |
| Correo_responsable_funcional | |
| Area_responsable_tecnica | |
| Responsable_tecnico | |
| Correo_responsable_tecnico | |
| Instancia de gobierno o comité asociado (si existe) | |
| Dependencia o área de soporte contractual | |

**Evidencias / referencias:** acto, memorando, designación o práctica vigente que respalde la responsabilidad:

---

## 3. Arquitectura funcional y de información

**Objetivo:** describir cómo opera el SI sin convertir la ficha en manual de ingeniería exhaustivo.

| Campo | Valor |
| --- | --- |
| Procesos_institucionales_soportados | |
| Funcionalidades_principales | |
| Entradas_principales | |
| Salidas_principales | |
| Actores internos / externos | |
| Clasificacion_de_la_informacion | |
| Manejo_de_datos_personales | |
| Zona(s) de arquitectura MAE/MRAE relacionadas | |

**Diccionario resumido de entidades de información críticas:**

| Dato / entidad | Descripción | Fuente / origen | Sensibilidad | Observaciones |
| --- | --- | --- | --- | --- |
| | | | | |

**Narrativa requerida:**

- **Contexto del flujo de información:**
- **Dependencias funcionales relevantes:**
- **Límites del SI respecto de otros sistemas:**

---

## 4. Componentes internos del SI

**Objetivo:** registrar la descomposición técnica o funcional relevante del SI.

| ID_Componente | Nombre | Tipo | Función | Compartido con otros SI | Estado | Versión | Observaciones |
| --- | --- | --- | --- | --- | --- | --- | --- |
| | | | | | | | |

**Reglas:**

- Si un componente también está en la hoja `Componentes` del libro F-A-GTI-02, la ficha solo lo **referencia por ID y resumen**.
- Si el componente no amerita inventario independiente, basta esta tabla interna de la ficha.

---

## 5. Integraciones e interfaces

**Objetivo:** describir de forma normalizada las relaciones del SI con otros activos.

| Campo de síntesis (catálogo) | Valor |
| --- | --- |
| Interopera_con_entidades_externas | |
| Numero_integraciones_activas | |

| ID_Integracion | Origen / destino | Tipo de interfaz | Propósito | Dirección | Entidad externa asociada | Criticidad | Estado |
| --- | --- | --- | --- | --- | --- | --- | --- |
| | | | | | | | |

**Campos narrativos mínimos:**

- **Resumen de interoperabilidad externa:**
- **Dependencias críticas con terceros:**
- **Observaciones sobre intercambio de datos sensibles:**

---

## 6. Arquitectura tecnológica y despliegue

**Objetivo:** capturar el detalle técnico mínimo suficiente para soporte y evolución.

| Campo | Valor |
| --- | --- |
| Modelo_de_despliegue | |
| Tipo_de_arquitectura | |
| Tipo_de_desarrollo_adquisicion | |
| Version_actual | |
| Fabricante_o_proveedor_principal | |
| Tipo_de_licenciamiento | |
| Numero_componentes_registrados | |
| Sistemas_operativos_principales | |
| Lenguajes_principales | |
| Motores_de_base_de_datos | |
| Contenerización (sí/no; tecnología) | |
| CI/CD (sí/no; herramienta) | |
| Repositorios técnicos / URLs / ubicaciones | |

> **Regla:** rutas de Dockerfile, pipelines u otros artefactos muy volátiles se **referencian por enlace**; no son campos estructurados obligatorios.

---

## 7. Ciclo de vida, soporte y operación

**Objetivo:** consolidar estado operativo, soporte, contratos y mantenibilidad.

| Campo | Valor |
| --- | --- |
| Estado_del_SI | |
| Fecha_salida_produccion | |
| Fecha_ultima_actualizacion_relevante | |
| Soporte_vigente_hasta | |
| Proveedor_de_soporte_actual | |
| Estado_ANS_terceros | |
| Indicadores del ANS (si aplica) | |
| Ventanas de mantenimiento | |
| Incidentes reportados últimos 12 meses | |
| Riesgos tecnológicos identificados | |
| Obsolescencias conocidas | |
| Evolución prevista | |
| Ultima_revision_anual | |
| Proxima_revision_programada | |

---

## 8. Seguridad, privacidad y continuidad

**Objetivo:** documentar el cumplimiento mínimo de seguridad y continuidad necesario para gobernanza.

| Campo | Valor |
| --- | --- |
| Valoracion_de_seguridad | |
| Nivel_de_riesgo_residual | |
| Clasificacion_de_la_informacion | |
| Manejo_de_datos_personales | |
| RNBD u otra referencia de cumplimiento (cuando aplique) | |
| Backup_definido | |
| Frecuencia de backup | |
| RTO / RPO (cuando existan) | |
| Plan_de_continuidad | |
| Controles de acceso relevantes | |
| Accesibilidad web (si aplica por canal ciudadano) | |
| Hallazgos o brechas críticas | |

**Evidencias / referencias:**

- Documento de análisis de riesgos:
- Plan de continuidad o contingencia:
- Referencia a controles MSPI / SGSI / seguridad institucional:

---

## 9. Calidad, valor y análisis estratégico

**Objetivo:** soportar decisiones de portafolio sin recargar el catálogo principal.

### 9.1 Valor y cobertura

| Campo | Valor |
| --- | --- |
| Criticidad_operacional | |
| Usuarios_activos | |
| Cobertura_del_proceso | |
| Beneficios esperados / observados | |

### 9.2 Análisis DOFA

| Fortalezas | Debilidades |
| --- | --- |
| | |

| Oportunidades | Amenazas |
| --- | --- |
| | |

### 9.3 Madurez y satisfacción

| Campo | Valor |
| --- | --- |
| Nivel de madurez | |
| Satisfacción de usuarios | |

### 9.4 TIME detallado (marco complementario institucional; no obligación MinTIC)

| Campo | Valor |
| --- | --- |
| Eje valor al negocio (0-3) | |
| Eje eficiencia técnica (0-3) | |
| Eje costos y riesgos (0-3) | |
| Clasificacion_TIME (T / I / M / E) | |
| Justificación | |
| Tipo_intervencion_recomendada | |
| Prioridad_intervencion | |

---

## 10. Dimensión económica y mantenimiento

**Objetivo:** dejar trazable la estructura del TCO y los insumos del plan de mantenimiento.

**Tabla obligatoria TCO:**

| Concepto | Valor anual COP | Fuente | Confirmado / estimado | Observaciones |
| --- | --- | --- | --- | --- |
| Licenciamiento | | | | |
| Soporte y mantenimiento | | | | |
| Infraestructura | | | | |
| Evolutivo | | | | |
| Correctivo | | | | |
| Otros aprobados por OTIC | | | | |
| **TCO total** (= `TCO_anual_total_COP` del catálogo) | | | | |

| Campo | Valor |
| --- | --- |
| Ratio_TCO_por_usuario_COP (calculado) | |
| Tipo_mantenimiento_recomendado | |
| Periodicidad_mantenimiento_sugerida | |
| Proxima_revision_programada | |
| Observaciones para el plan anual de mantenimiento | |

---

## 11. Estado de documentación y evidencias

**Objetivo:** verificar disponibilidad de la documentación mínima exigible.

| Campo de síntesis (catálogo) | Valor |
| --- | --- |
| Estado_documentacion_minima | |

**Tabla obligatoria:**

| Documento / evidencia | Estado | Ubicación o enlace | Responsable de actualizar | Observaciones |
| --- | --- | --- | --- | --- |
| Manual técnico | | | | |
| Manual de usuario | | | | |
| Manual de operación | | | | |
| Requerimientos / historias | | | | |
| Arquitectura de solución | | | | |
| Plan de pruebas | | | | |
| Plan de mantenimiento | | | | |
| Contrato o acto principal (si aplica) | | | | |

---

## 12. Validación, firmas y control de cambios

**Control de cambios de la ficha:**

| Versión | Fecha | Descripción del cambio | Elaboró | Aprobó |
| --- | --- | --- | --- | --- |
| | | | | |

**Validaciones:**

| Rol | Nombre | Cargo | Firma / aprobación | Fecha |
| --- | --- | --- | --- | --- |
| Responsable técnico | | | | |
| Responsable funcional | | | | |
| OTIC / líder designado | | | | |

**Fecha de aprobación de la ficha:**

---

## Anexo — Trazabilidad de los 44 campos del catálogo en esta ficha

| Sección de la ficha | Campos del catálogo que deben verse o resumirse allí |
| --- | --- |
| 1 — Identificación general | ID_SI, Nombre_oficial, Sigla_Acronimo, Tipo_o_patron_de_SI, Categoria_institucional, Descripcion_breve, Procesos_institucionales_soportados, Dependencia_duena_del_proceso, Marco_legal_mandatorio, Objetivos_estrategicos_que_apoya, Estado_del_SI, Vigencia_del_registro |
| 2 — Gobierno y responsables | Area_responsable_funcional, Responsable_funcional, Area_responsable_tecnica, Responsable_tecnico |
| 3 — Arquitectura funcional | Clasificacion_de_la_informacion, Manejo_de_datos_personales |
| 5 — Integraciones e interfaces | Interopera_con_entidades_externas, Numero_integraciones_activas |
| 6 — Arquitectura tecnológica | Version_actual, Modelo_de_despliegue, Tipo_de_desarrollo_adquisicion, Fabricante_o_proveedor_principal, Tipo_de_licenciamiento, Numero_componentes_registrados |
| 7 — Ciclo de vida y soporte | Fecha_salida_produccion, Soporte_vigente_hasta, Estado_ANS_terceros, Ultima_revision_anual, Proxima_revision_programada |
| 8 — Seguridad y continuidad | Clasificacion_de_la_informacion, Manejo_de_datos_personales, Valoracion_de_seguridad, Nivel_de_riesgo_residual, Backup_definido, Plan_de_continuidad |
| 9 — Calidad y análisis estratégico | Criticidad_operacional, Usuarios_activos, Cobertura_del_proceso, Clasificacion_TIME, Tipo_intervencion_recomendada, Prioridad_intervencion |
| 10 — Dimensión económica | TCO_anual_total_COP, Ratio_TCO_por_usuario_COP |
| 11 — Documentación y evidencias | Estado_documentacion_minima |
