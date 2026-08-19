---
title: "Handoff optimizado — Catálogo Institucional de Sistemas de Información"
purpose: "Contexto mínimo para continuar el proyecto en Claude Fable 5 sin releer toda la conversación."
version: "1.0"
date: "2026-08-19"
---

# MODO DE USO

Este archivo es el contexto rector. Léelo completo al iniciar una sesión.

No leas automáticamente los tres documentos fuente completos. Primero identifica la evidencia necesaria para la tarea actual y consulta únicamente el archivo y las secciones pertinentes.

Cuando una decisión esté marcada como **DECISIÓN CERRADA**, no la reabras salvo nueva evidencia oficial de MinTIC, una contradicción objetiva en los archivos o instrucción expresa del usuario.

No generes artefactos nuevos por defecto. Primero determina si el resultado pertenece a uno de los tres instrumentos existentes.

# FÓRMULA DE CONTEXTO

`CONTEXTO = NÚCLEO + ESTADO + FUENTES_NECESARIAS + DELTA`

- `NÚCLEO`: objetivo, principios, decisiones cerradas y reglas de este archivo.
- `ESTADO`: pregunta exacta del turno.
- `FUENTES_NECESARIAS`: solo las secciones relevantes del Catálogo, Ficha o Guía.
- `DELTA`: cambios y decisiones nuevas desde la última iteración.

Evita:

`CONTEXTO = conversación_completa + 3_documentos_completos + análisis_previos + nueva_tarea`

# PATRÓN DE PROMPT

## OBJETIVO
Una sola decisión o producto verificable.

## DECISIONES CERRADAS
Lo que no debe volver a discutirse.

## LEER
Archivos/secciones estrictamente necesarias.

## VERIFICAR
Fuentes oficiales externas necesarias.

## PRODUCIR
Resultado exacto.

## NO HACER
Trabajo fuera de alcance.

## CRITERIO DE CIERRE
Condición objetiva de terminación.

# PRINCIPIO DE TOKEN-BUDGET

Prioriza contexto rector pequeño y estable, recuperación selectiva de fuentes, resultados incrementales y generación de archivos solo después de congelar la estructura.

El repositorio es la memoria; el modelo debe recuperar solo lo necesario.

# PROYECTO

Ministerio de Ambiente y Desarrollo Sostenible de Colombia — OTIC.

Objetivo: revisar, depurar y dejar listos los instrumentos institucionales para caracterización y gestión de Sistemas de Información, alineados con MinTIC, evitando sobre-documentación y complejidad innecesaria.

Fuentes:

1. `01_Catalogo_SI_F-A-GTI-02_V4.md`
2. `02_Ficha_Caracterizacion_SI.md`
3. `03_Guia_Diligenciamiento_SI_V8.md`

# ARQUITECTURA DOCUMENTAL

## F-A-GTI-02 — Catálogo Institucional
Vista consolidada del portafolio de Sistemas de Información. Debe permitir identificar, comparar, gobernar, priorizar, alertar y decidir. No debe almacenar todo el detalle técnico.

## F-A-GTI-01 — Ficha de Caracterización
**DECISIÓN CERRADA:** la Ficha debe ser más completa que la fila correspondiente del Catálogo.

`FICHA ⊃ CATÁLOGO`

La Ficha contiene la caracterización profunda por Sistema de Información. El Catálogo conserva el subconjunto necesario para gestión consolidada y puede incluir campos calculados.

## G-A-GTI-01 — Guía
Debe explicar el modelo de información adoptado, la taxonomía, las reglas de clasificación, los campos del Catálogo y los campos adicionales de la Ficha. Se ajustará después de congelar taxonomía y modelo de datos.

# PROBLEMA CENTRAL

La taxonomía actual mezcla niveles distintos: Sistema de información, Aplicación, Componente, Integración, Plataforma, Servicio tecnológico, Solución analítica y Herramienta transversal; además mezcla conceptos como sistema transaccional, ERP, CRM, CMS, API, servicio web, microservicio, hub, ESB, middleware y SaaS.

Esto debe resolverse antes de cerrar el modelo de datos.

# HIPÓTESIS DE DISEÑO A VALIDAR

La hoja principal del Catálogo debería registrar principalmente **Sistemas de Información** como objetos gobernados de primer nivel.

Objetos técnicos relacionados deberían modelarse como entidades vinculadas:

- Sistema de Información → Catálogo principal + Ficha.
- Sistema transaccional / ERP / CRM / BPM / CMS → tipos o patrones de SI cuando cumplan la definición institucional.
- Módulo → componente interno de un SI.
- Microservicio → componente de software.
- API / REST / SOAP → interfaz/contrato de integración.
- Integración → relación entre origen y destino.
- Hub / ESB / iPaaS → plataforma/capacidad de integración.
- SaaS → modelo de prestación/despliegue, no clase equivalente a SI.
- Dashboard / BI → evaluar si es artefacto analítico o solución con gobierno propio.
- Servicios TI corporativos → evaluar en Catálogo de Servicios de TI separado.

Esta hipótesis NO está cerrada.

# PRÓXIMA DECISIÓN

Construir una **Taxonomía Institucional v1** para: Sistema de Información; sistema transaccional; aplicación; módulo; componente de software; microservicio; API; servicio web; integración; interfaz; hub de integración; ESB; middleware; plataforma; ERP; CRM; BPM; CMS; solución analítica; dashboard; servicio de TI; SaaS.

Para cada término producir:

1. término;
2. definición MinTIC cuando exista;
3. definición de estándar/autor reconocido cuando haga falta;
4. definición institucional propuesta;
5. criterios de inclusión/exclusión;
6. relación con otros objetos;
7. ejemplo;
8. lugar de registro;
9. regla para casos frontera.

# REGLA DE PERTENENCIA PRELIMINAR

> Un elemento se registra como Sistema de Información cuando constituye una unidad funcional identificable que soporta uno o más procesos o servicios institucionales, gestiona información del negocio y posee responsabilidad funcional, ciclo de vida y gobierno propios. Los módulos, componentes, interfaces y plataformas que habilitan su funcionamiento no adquieren automáticamente la condición de Sistema de Información.

# CICLO 1 — ESTADO

No modificar todavía los instrumentos.

Hallazgos:

- `Catálogo`: 99 columnas A:CU.
- `Diccionario`: documenta atributos hasta DA y no coincide plenamente con la hoja real.
- `Instrucciones`: contiene información residual de versión anterior y declara 8 hojas aunque existen 10.
- `Tablero`: referencias rotas en seguridad.
- `Alertas Caducidad`: referencias `#REF!`.
- La hoja principal `Catálogo` no tiene registros visibles debajo de encabezados; `Hoja2` sí contiene registros.
- Guía V8 y Ficha no son completamente consistentes respecto de seguridad/continuidad.
- El Excel mezcla catálogo, ficha técnica, integraciones, DevOps, documentación, mantenimiento, análisis estratégico y control de diligenciamiento.

# PRINCIPIOS DE DISEÑO

1. Mínimo suficiente, no mínimo absoluto.
2. Conservar un campo si permite identificar, gobernar, comparar, priorizar, alertar o decidir.
3. No añadir campos solo por buena práctica.
4. Distinguir obligación MinTIC, recomendación MinTIC, decisión institucional, buena práctica y dato calculado.
5. No forzar información no aplicable.
6. No crear catálogos paralelos sin necesidad.
7. Normalizar relaciones repetibles, especialmente integraciones y componentes.
8. Ficha = registro profundo; Catálogo = vista consolidada.
9. Congelar taxonomía y modelo de datos antes de ajustar archivos.
10. Máximo tres ciclos: diagnóstico, consolidación y QA.

# CLASIFICACIÓN DE CAMPOS

Cada campo existente se clasifica como:

- MANTENER
- MODIFICAR
- CALCULAR
- MOVER A FICHA
- MOVER A OTRO ARTEFACTO/HOJA
- ELIMINAR

Para cada decisión registrar finalidad, fuente, obligatoriedad/recomendación, uso, responsable y justificación.

# REGLA DE INVESTIGACIÓN

Para MinTIC: usar fuentes oficiales vigentes, citar documento y URL exactos y no atribuir a MinTIC fórmulas o umbrales internos.

Para taxonomía: preferir estándar o fuente primaria cuando MinTIC no defina suficientemente el concepto.

# REGLA DE STOP

Detener investigación cuando la evidencia ya permite tomar y justificar la decisión y nuevas fuentes solo repiten lo establecido.

# PRIMERA TAREA PARA FABLE 5

Continúa el Ciclo 1. No modifiques archivos.

Construye la **Taxonomía Institucional v1** comenzando por distinguir:

1. Sistema de Información
2. Aplicación
3. Sistema transaccional
4. Plataforma
5. Componente de software
6. Microservicio
7. Integración
8. API
9. Servicio web
10. Hub / ESB / iPaaS
11. Servicio de TI
12. SaaS

Usa fuentes oficiales de MinTIC y, cuando MinTIC no defina suficientemente un concepto, estándares o autores primarios.

Al final propón un árbol de decisión para decidir si un objeto:
A) entra al Catálogo principal de SI;
B) se registra como componente;
C) se registra como integración/interfaz;
D) se registra en catálogo de servicios/plataformas;
E) no requiere inventario independiente.

No diseñes todavía el Excel final.
