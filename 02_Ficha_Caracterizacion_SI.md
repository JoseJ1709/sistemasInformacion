---
title: "F-A-GTI-01 — Ficha de Caracterización de Sistema de Información"
source_file: "Ficha_Caracterizacion_SI_Final.docx"
conversion: semantic-markdown
note: "Texto y tablas conservados; imágenes decorativas, formato visual y espacios vacíos omitidos para reducir tokens."
---

## FICHA DE CARACTERIZACIÓN

Soluciones Tecnológicas

| Entidad | Nombre oficial de la entidad |  |  |
| --- | --- | --- | --- |
| Sector | Sector al que pertenece | Código DANE | Código DANE si aplica |
| Versión ficha | Ej: 1.0 | Fecha | DD/MM/AAAA |
| Elaboró | Nombre y cargo | Aprobó | Nombre y cargo |

| 📌 Esta ficha debe diligenciarse por sistema de información. Una vez completada, sus datos se trasladan al Catálogo Consolidado de Sistemas de Información. Campos marcados con * son de obligatorio diligenciamiento. Lineamiento: MGGTI.LI.SI.02 — MinTIC 2023. |
| --- |

## 1. IDENTIFICACIÓN GENERAL DEL SISTEMA

| Campo | Contenido / Guía |
| --- | --- |
| Id solución * | Código único. Ej: SYS-001 |
| Nombre oficial de la solución (*) | Nombre completo y oficial del sistema de información |
| Sigla / Acrónimo * | Ej: SIGEP, SECOP, SIIF |
| Clase de activo | Sistema_de_información/ Aplicación/ Componente/ Integración/ Plataforma/ Servicio_tecnológico/ Solución_analítica/ Herramienta_transversal. |
| Tipo solución | Escoger el tipo de solución: Sistema de Información / Aplicativo /Sistema Transaccional / ERP CRM/ Hub de Integración / Bus de Servicios (ESB)/ API / Servicio Web / Middleware.. entre otros |
| Descripción del sistema * | Propósito general, alcance y contexto de uso. Máximo 15 líneas. |
| Funcionalidades principales | Liste las funciones clave que ofrece el sistema (mín. 3, máx. 10) |
| Categoría Institucional * | Estratégico / Misional / Apoyo / Evaluación / Otros |
| Dependencia dueña del proceso | Dependencia que realiza el proyecto |
| No. Iniciativa / proyecto origen | ID de la iniciativa aprobada que originó el sistema. 'Preexistente' si fue heredado. |

## 2. ARQUITECTURA Y DESPLIEGUE TECNOLÓGICO

| Campo | Contenido / Guía |
| --- | --- |
| Proceso (s) que soporta | Procesos del mapa de procesos institucional (P01 Gestión Integrada del Portafolio de Planes Programas y Proyectos) Nombre exacto del proceso según el mapa de procesos institucional.ⓘ Use la nomenclatura del Mapa de Procesos vigente de la entidad. |
| Módulos / Componentes | Describa cada módulo o subsistema. Ej: Módulo de Nómina, Módulo de Reportes.<br>ⓘ Si el sistema no tiene módulos definidos, indique "Sistema sin modularización". |
| Entradas (Inputs) | ¿Qué información, datos, archivos o transacciones recibe el sistema? ¿De dónde provienen? |
| Salidas (Outputs) | ¿Qué información produce? ¿Reportes, archivos, notificaciones, datos a otros sistemas? |
| Sistemas con los que se integra (internos) | Nombre de otros sistemas con los que intercambia datos. |
| Tipo de integración | Mecanismo técnico: API REST, SOAP, FTP, SFTP, DB Link, Archivo plano, Otro. Especifique por integración.<br>ⓘ Ej: Con SIIF mediante API REST (JSON). Con archivo RRHH mediante FTP batch diario. |

| Campo | Contenido | Campo | Contenido |
| --- | --- | --- | --- |
| Modelo de despliegue * | On-Premises / Nube Pública / Nube Privada / Híbrida / SaaS /PaaS / No Definido | Tipo de arquitectura | Monolítico / Microservicios / SOA / Cliente-Servidor / N-Capas |
| Sistema operativo | SO del servidor principal. Ej: Windows Server 2019, Ubuntu 22 | Lenguaje de programación | Ej: Java 17, .NET 6, PHP 8, Python 3.10 |
| Plataforma de Base de Datos Base de datos | Motor y versión. Ej: Oracle 19c, SQL Server 2019, PostgreSQL 14 | Versión actual | Versión del sistema en producción. Ej: 3.2.1 |
| ¿Interopera con entidades externas? | Sí / No | Entidades externas integradas | Nombre de entidades del Estado u otras organizaciones. |

## 3. CICLO DE VIDA Y SOPORTE

| Campo | Contenido | Campo | Contenido |
| --- | --- | --- | --- |
| Estado actual * | Activo / En Migración / En Mantenimiento / En Desarrollo / Deprecado / Retirado | Versión actual | Versión del sistema en producción. Ej: 3.2.1 |
| Fecha puesta en producción * | DD/MM/AAAA | Fecha última actualización | DD/MM/AAAA — Última versión mayor desplegada |
| Tipo de desarrollo * | Desarrollo Propio / A la Medida / COTS / Open Source / SaaS / Híbrido | Fabricante * | Empresa o equipo que construyó el sistema |
| Proveedor de soporte * | Empresa o área que brinda soporte actualmente | Vencimiento del soporte * | DD/MM/AAAA — Fecha límite del contrato o garantía de soporte |
| Licenciamiento * | Propietario-Perpetuo / Propietario-Suscripción / Open Source / Freeware |  |  |

| 📌 Si el vencimiento del soporte ya pasó o está dentro de los próximos 6 meses, notifique inmediatamente al área de contratación. Un sistema sin soporte vigente es un riesgo operacional y de seguridad. |
| --- |

| Campo | Contenido / Guía |
| --- | --- |
| Estado del ANS * | Vigente / Vencido / No Aplica / En Negociación<br>ⓘ ANS = Acuerdo de Nivel de Servicio. Lineamiento MGGTI.LI.SI.10 |
| Indicadores del ANS | Métricas pactadas: disponibilidad, tiempo de respuesta a incidentes, ventanas de mantenimiento, penalidades. |

## 4. VALOR PARA LA ENTIDAD Y GOBIERNO DE DATOS

| Campo | Contenido / Guía |
| --- | --- |
| Objetivos estratégicos que soporta | ¿A qué objetivo del Plan Estratégico Institucional o del PND contribuye este sistema? |
| Marco legal aplicable | Norma, decreto o resolución que exige o regula este sistema. Ej: Decreto 1510 de 2013 (SECOP), Ley 1712 de 2014.<br>ⓘ Si el sistema existe por mandato legal, su retiro requiere concepto jurídico. |
| Nivel de criticidad operacional * | Alta / Media / Baja (ver criterio en Guía) |
| Cantidad de usuarios activos | Número de usuarios que lo usan o usarían regularmente |
| Nivel de cobertura del proceso | Alto (>80%) / Medio (50-80%) / Bajo (<50%) / No Evaluado |

| Campo | Contenido | Campo | Contenido |
| --- | --- | --- | --- |
| Clasificación de la información * | Pública / De Uso Interno / Reservada / Clasificada (Ley 1712) | Manejo de datos personales * | Sí-Responsable / Sí-Encargado / No (Ley 1581 de 2012) |

| 📌 Si el sistema gestiona datos personales, verifique el registro en el RNBD (Registro Nacional de Bases de Datos) ante la SIC. Obligación: Ley 1581 de 2012, Decreto 1074 de 2015. |
| --- |

## 5. RESPONSABILIDAD Y GOBIERNO DEL SISTEMA

| Campo | Contenido | Campo | Contenido |
| --- | --- | --- | --- |
| Área responsable técnico * | Área de TI responsable de la operación técnica | Nombre responsable técnico * | Nombre completo y cargo del funcionario |
| Área responsable funcional * | Área de negocio dueña del sistema (líder funcional) | Nombre responsable funcional * | Nombre completo y cargo del funcionario |
| Correo responsable técnico | correo@entidad.gov.co | Correo responsable funcional | correo@entidad.gov.co |

| 📌 El Responsable Técnico responde por la operación, seguridad y mantenimiento del sistema. El Responsable Funcional responde por los requerimientos, capacitación y uso adecuado. Ambos deben estar identificados en el catálogo en todo momento. |
| --- |

## 6. CALIDAD Y ANÁLISIS ESTRATÉGICO

## ANÁLISIS DOFA DEL SISTEMA

| FORTALEZAS (interno, positivo)<br>¿Qué hace bien este sistema? ¿Qué valoran los usuarios? ¿Qué atributos técnicos destacan? | DEBILIDADES (interno, negativo)<br>¿Qué falla frecuentemente? ¿Qué quejas recurrentes tienen los usuarios? ¿Qué no puede hacer? |
| --- | --- |
| OPORTUNIDADES (externo, positivo)<br>¿Qué mejoras tecnológicas o funcionales son posibles? ¿Hay nuevas normas que favorezcan su evolución? | AMENAZAS (externo, negativo)<br>¿Hay riesgo de obsolescencia? ¿El proveedor va a retirar el soporte? ¿Cambios normativos que lo afecten? |

| Campo | Contenido / Guía |
| --- | --- |
| Incidentes reportados (últimos 12 meses) | Número de tickets, PQRS o incidentes formales |
| Riesgos tecnológicos identificados | Obsolescencia de SO, fin de soporte del proveedor, problemas de compatibilidad, deuda técnica, dependencias críticas. |
| Nivel de madurez | Grado de gestión formal del sistema |
| Evolución prevista del sistema | ¿Qué planes de modernización, integración o migración están previstos a mediano y largo plazo? |

## CLASIFICACIÓN EN EL CUADRANTE TIME *

| I — INVERTIR | T — TOLERAR | M — MIGRAR | E — ELIMINAR |
| --- | --- | --- | --- |
| Alto valor + alta eficiencia. Priorizar inversión. | Funciona. Mantener sin cambios mayores. | Bajo rendimiento técnico. Necesario pero debe migrar. | Sin valor estratégico. Planear retiro. |

| Campo | Contenido / Guía |
| --- | --- |
| Clasificación TIME del sistema * | Indique: I / T / M / E y justifique la decisión basándose en: valor al negocio, eficiencia técnica y relación costo-riesgo. |
| Tipo de intervención recomendada | ¿Qué acción concreta se propone? Ej: Migración a nube en 2025, Retiro en Q2-2024, Rediseño de módulo X, Sin cambios. |

## 7. DIMENSIÓN ECONÓMICA (TCO — Costo Total de Propiedad)

| 📌 El TCO no requiere contabilidad exacta. Es un estimado anual que permite comparar sistemas y justificar decisiones de inversión. Fuente: área financiera o contratos. |
| --- |

| Concepto de Costo | Valor Anual ($COP) | Observaciones |
| --- | --- | --- |
| Costo anual licenciamiento de software | $ | Incluir todos los módulos y componentes licenciados |
| Costo de soporte y mantenimiento anual (contrato) | $ | Valor del contrato de soporte vigente |
| Costo anual infraestructura asociada (servidores / nube) | $ | Proporcional si es infraestructura compartida |
| Mantenimiento evolutivo (desarrollos nuevos) | $ | Estimado anual de mejoras |
| Mantenimiento correctivo (corrección de errores) | $ |  |
| Capacitación y formación de usuarios | $ |  |
| TCO ANUAL TOTAL ESTIMADO | $ | Suma de todas las líneas anteriores |

## 8. ESTADO DE LA DOCUMENTACIÓN

| 📌 Lineamiento MGGTI.LI.SI.08: Todos los sistemas deben tener documentación técnica y funcional actualizada. Un sistema sin documentación genera dependencia de personas y riesgo ante rotación de personal. |
| --- |

| Documento | Estado | Ubicación / Observaciones |
| --- | --- | --- |
| Manual técnico (arquitectura, instalación, configuración) | Vigente / Desactualizado / No existe | Ruta o repositorio donde se encuentra el documento |
| Manual de usuario final | Vigente / Desactualizado / No existe | Ruta o repositorio donde se encuentra el documento |
| Manual de operación y administración | Vigente / Desactualizado / No existe | Ruta o repositorio donde se encuentra el documento |
| Documentación de requerimientos (SRS / Historias de usuario) | Vigente / Desactualizado / No existe | Ruta o repositorio donde se encuentra el documento |
| Arquitectura de solución (diagramas) | Vigente / Desactualizado / No existe | Ruta o repositorio donde se encuentra el documento |
| Plan de pruebas | Vigente / Desactualizado / No existe | Ruta o repositorio donde se encuentra el documento |
| Plan de mantenimiento | Vigente / Desactualizado / No existe | Ruta o repositorio donde se encuentra el documento |

## 9. CONTROL DE CAMBIOS DE LA FICHA

| Ver. | Fecha | Descripción del Cambio | Elaboró | Aprobó |
| --- | --- | --- | --- | --- |
| 1.0 | DD/MM/AAAA | Versión inicial de la ficha | Carlos Centeno |  |
| 1.1 | DD/MM/AAAA | Describa el cambio realizado |  |  |
| 1.2 | DD/MM/AAAA | Describa el cambio realizado |  |  |
| 2.0 | DD/MM/AAAA | Describa el cambio realizado |  |  |

## 10. FIRMAS DE APROBACIÓN

| RESPONSABLE TÉCNICO | RESPONSABLE FUNCIONAL | DIRECTOR DE TI / LÍDER DE SISTEMAS |
| --- | --- | --- |
| _________________________<br><br>Nombre y cargo<br><br>Firma y fecha | _________________________<br><br>Nombre y cargo<br><br>Firma y fecha | _________________________<br><br>Nombre y cargo<br><br>Firma y fecha |

| 📌 Una vez firmada, esta ficha constituye el documento de registro oficial del sistema ante auditorías internas o externas. Archivo en: repositorio documental de TI / carpeta del sistema. |
| --- |
