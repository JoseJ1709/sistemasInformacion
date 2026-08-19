# 04_Taxonomia_Institucional_SI

## 1. Propósito y criterio de uso

Este documento cierra la frontera conceptual del inventario institucional y define qué entra al **Catálogo Institucional de Sistemas de Información** y qué debe registrarse en artefactos vinculados.

### 1.1 Regla rectora cerrada

- **Decisión institucional propuesta:** el **Catálogo principal** registra únicamente **Sistemas de Información (SI)** como objetos gobernados de primer nivel.
- **Decisión institucional propuesta:** componentes, módulos, APIs, servicios web, interfaces, integraciones, plataformas, servicios tecnológicos y modelos de prestación como SaaS **no se registran como SI por defecto**.
- **Decisión cerrada del proyecto, consolidada también en `08_ESPECIFICACION_FINAL.md`:** `FICHA ⊃ CATÁLOGO`.

### 1.2 Jerarquía de fuentes usada

1. **Obligación MinTIC / Gobierno Digital**: caracterizar y gestionar los sistemas de información, mantener arquitectura y documentación, y usar insumos para mantenimiento y gobierno.
2. **Complemento técnico reconocido**: cuando MinTIC no define con suficiente detalle términos como API, microservicio, SaaS o ESB, se usan estándares o fuentes primarias reconocidas.
3. **Decisión institucional propuesta**: reglas de frontera, lugar de registro y criterio operativo para el Ministerio.

### 1.3 Decisión sobre la taxonomía N1-N8 existente

**Decisión:** la taxonomía **N1-N8 debe sustituirse**, no mantenerse ni reformularse como eje principal del nuevo catálogo.

**Justificación:**

1. **Mezcla niveles distintos**: en una misma columna conviven clases de inventario (SI, componente, integración, plataforma, servicio) y patrones funcionales (ERP, CRM, dashboard, SaaS).
2. **Contradice el principio de frontera**: el catálogo principal debe consolidar SI, no mezclar en una sola tabla objetos heterogéneos.
3. **Dificulta gobernanza y calidad**: forzar DOFA, TIME, TCO y responsables equivalentes para APIs, microservicios y dashboards produce datos artificiales.
4. **No es una obligación MinTIC**: MinTIC exige caracterización y gestión de SI, pero no impone la taxonomía N1-N8 observada en los archivos actuales.

### 1.4 Taxonomía sustitutiva propuesta

La clasificación institucional se separa en dos planos:

1. **Clase de inventario (decide la hoja / artefacto):**
   - A. Sistema de Información
   - B. Componente de un SI
   - C. Integración / Interfaz
   - D. Plataforma tecnológica
   - E. Servicio de TI
   - F. Otro activo tecnológico

2. **Tipo o patrón del SI** (solo para registros que sí son SI):
   - Sistema transaccional
   - ERP
   - CRM
   - BPM / BPMS
   - CMS
   - Sistema de Gestión Documental
   - GIS
   - Solución analítica
   - Otro SI institucional

3. **Atributos complementarios, no taxonomías de primer nivel:**
   - Modelo de prestación: SaaS / PaaS / IaaS / On-premises / híbrido
   - Estilo técnico: monolítico / microservicios / SOA / etc.
   - Mecanismo de integración: API REST / SOAP / archivo / evento / ETL / etc.

## 2. Definiciones institucionales y frontera del inventario

> **Regla institucional de pertenencia:** un activo se registra como **Sistema de Información** cuando constituye una unidad funcional identificable, soporta uno o más procesos o servicios institucionales, gestiona información del negocio y tiene responsabilidad funcional, ciclo de vida y gobierno propios.

| Concepto | Fuente autorizada | Definición institucional propuesta | Nivel arquitectónico | ¿Puede ser SI? | Criterio de distinción y lugar de registro | Ejemplo institucional / típico |
| --- | --- | --- | --- | --- | --- | --- |
| **Sistema de Información** | **MinTIC / Gobierno Digital**: Decreto 767 de 2022 define SI; MGGTI.G.SI y MAE.G.ASI exigen su caracterización y gestión, aunque no fijan una taxonomía de frontera tan detallada como la requerida aquí. | Unidad funcional gobernada que soporta procesos o servicios institucionales, gestiona información del negocio, tiene usuarios y responsables propios, y puede estar compuesta por aplicaciones, componentes, datos e integraciones. | Negocio + aplicaciones | **Sí; es el objeto principal.** | Si tiene propósito misional o de apoyo claramente delimitado, datos de negocio, responsables funcional y técnico, ciclo de vida y gobierno propios, entra en **Catálogo_SI** y tiene **Ficha**. | REAA, ARCA/ORFEO, VITAL, RENARE. |
| **Sistema transaccional** | Uso técnico extendido; MinTIC no da definición operativa específica. | Tipo de SI orientado a capturar, validar, registrar y consultar transacciones del negocio con reglas, trazabilidad y persistencia. | Aplicación / negocio | **Sí, como tipo de SI.** | Si ejecuta el proceso y registra transacciones de negocio, se registra como **SI**. Si solo expone una pantalla o módulo de captura de otro SI, es componente o aplicación subordinada. | Sistema de PQRSD, nómina, trámites, inventarios. |
| **Aplicación** | Fuente técnica general; MinTIC la usa de forma amplia pero no la separa de SI en los lineamientos citados. | Pieza de software con funcionalidad acotada, usualmente enfocada en una tarea, canal o capacidad específica. | Aplicación | **Solo a veces.** | Si la aplicación por sí sola cumple la regla de SI, entra al catálogo como SI; si solo implementa una función puntual de otro SI, va a **Componentes** o se referencia en la Ficha. | Portal de autoservicio, app móvil de consulta, front web de un SI mayor. |
| **Plataforma** | MinTIC MAE/MRAE reconoce dominios y capacidades de arquitectura; no define una taxonomía operativa única para “plataforma”. | Capacidad tecnológica base que habilita múltiples aplicaciones, integraciones o servicios. | Tecnología / plataforma | **No por defecto.** | Si su función principal es habilitar otras soluciones, va a **catálogo de plataformas** o a la hoja de soporte correspondiente, no a Catálogo_SI. Solo entra como SI si además constituye una solución funcional institucional gobernada como tal. | Plataforma BPM compartida, IAM, iPaaS corporativo. |
| **ERP** | Categoría reconocida de suite empresarial; MinTIC no define detalle taxonómico. | Suite integrada para procesos corporativos administrativos o de gestión interna. | Negocio + aplicaciones | **Sí, si es la unidad funcional gobernada.** | Si el Ministerio lo usa como solución funcional de procesos corporativos con gobierno propio, es **tipo de SI**. Si solo es la base sobre la cual corren módulos sin gestión funcional unificada en esta entidad, trátese como plataforma y registre los SI funcionales por separado. | ERP financiero o administrativo institucional. |
| **CRM** | Categoría reconocida de suite empresarial; sin definición MinTIC específica. | Solución para gestionar relaciones, interacciones, trazabilidad y servicios hacia usuarios, ciudadanos, clientes o grupos de interés. | Negocio + aplicaciones | **Sí, si gobierna el proceso.** | Entra a **Catálogo_SI** cuando es la solución funcional de atención/relación y no solo un módulo accesorio de otro sistema. | CRM de atención al ciudadano o relacionamiento. |
| **BPM / BPMS** | Patrón y categoría tecnológica ampliamente reconocidos; MinTIC no define frontera operativa aquí. | Suite o solución para modelar, automatizar, ejecutar y monitorear procesos. | Aplicación / plataforma | **A veces.** | Si el BPMS es solamente la **plataforma** sobre la que se construyen varios SI, va a **plataformas**. Si la solución desplegada con ese motor es el sistema funcional institucional, el **SI** es la solución de negocio, no el motor BPM en abstracto. | Plataforma Bizagi compartida vs. sistema de trámite específico montado sobre ella. |
| **CMS** | Categoría técnica reconocida. | Sistema para crear, administrar y publicar contenidos digitales. | Aplicación / plataforma | **A veces.** | Si administra un proceso institucional de contenido con gobierno, usuarios y datos propios, puede registrarse como SI. Si solo habilita sitios o micrositios, va como plataforma o componente. | Gestor de contenidos del portal institucional. |
| **Sistema de Gestión Documental** | La gestión documental tiene respaldo normativo archivístico; la herramienta tecnológica puede ser un SI. | SI especializado para radicación, trámite, archivo, expediente y trazabilidad documental. | Negocio + aplicaciones | **Sí.** | Si soporta el proceso formal de gestión documental, se registra como **SI**. Si solo es repositorio técnico de documentos de otra solución, es plataforma o componente. | ARCA / ORFEO. |
| **GIS** | Fuente reconocida: ISO 19101 / Esri para geoinformación. | Solución para capturar, almacenar, analizar, administrar y visualizar información geográfica. | Datos + aplicación | **A veces.** | Si el GIS soporta procesos misionales, administra datos geográficos y tiene gobierno propio, es **SI** o tipo de SI analítico/misional. Si es solo visor embebido, capa cartográfica o componente de mapas, va a **Componentes**. | Visor geográfico institucional con operación propia vs. mapa incrustado en otro SI. |
| **Solución analítica** | MinTIC exige gestión y arquitectura de SI, pero no define taxonomía precisa para BI/dashboard. | Solución orientada a consolidar, transformar, analizar y explotar datos para seguimiento, decisión o inteligencia institucional. | Datos + aplicación | **A veces.** | Si tiene gobierno propio, fuentes definidas, usuarios, reglas y ciclo de vida institucional, puede registrarse como SI. Si solo es un reporte o tablero dependiente de otro activo, no. | Data warehouse con operación institucional, suite BI de seguimiento sectorial. |
| **Dashboard** | Fuente reconocida de analítica; MinTIC no lo define de forma específica. | Visualización o tablero que presenta indicadores y análisis, normalmente dependiente de un SI o solución analítica mayor. | Presentación / analítica | **No por defecto.** | Un dashboard aislado normalmente **no es SI**. Solo subiría a Catálogo_SI si además captura, procesa y gobierna información y decisiones como solución completa. En la mayoría de casos se documenta en **Ficha** o como parte de una **solución analítica**. | Tablero Power BI dependiente de un data mart. |
| **Componente de software** | Fuente técnica general; alineado con la arquitectura de solución descrita en MAE.G.ASI y MAE.GE.ASI.01. | Elemento de software desplegable o gestionable que cumple una responsabilidad técnica o funcional dentro de una solución mayor. | Aplicación / tecnología | **No por defecto.** | Se registra en **Componentes** cuando tiene identidad técnica propia, criticidad, reutilización o despliegue independiente; si no, basta con mencionarlo en la Ficha. | Motor de reportes, servicio de autenticación, módulo de pagos. |
| **Módulo** | Uso arquitectónico general. | Subconjunto funcional interno de un SI, normalmente no reutilizable por fuera de él. | Aplicación | **No.** | Si no tiene despliegue y gobierno propios, no merece inventario independiente: se registra dentro de la **Ficha** del SI. Si se despliega y gobierna de forma separada, tratarlo como componente. | Módulo de nómina, módulo de radicación. |
| **Microservicio** | Fuente complementaria: CNCF / microservices.io. | Componente pequeño, de responsabilidad acotada, desplegable de forma independiente y expuesto mediante interfaces bien definidas. | Aplicación / integración | **No por defecto.** | Se registra en **Componentes** cuando sea operativamente relevante; no se registra como SI salvo caso excepcional en que en la práctica sea la solución funcional completa con gobierno propio, lo cual no debería ser la norma institucional. | Microservicio de autenticación, de notificaciones o de consulta. |
| **API** | **ISO/IEC 2382** define API como conjunto de funciones y procedimientos para acceder a capacidades o datos de otro servicio. | Contrato de interfaz que expone datos o capacidades de un sistema o componente a otros consumidores. | Integración / interfaz | **No.** | Se registra en **Integraciones_Interfaces**. La API no equivale al SI que la expone ni al que la consume. | API REST de consulta de expedientes. |
| **Servicio web** | **W3C Web Services Architecture** lo define como sistema de software para interacción máquina a máquina sobre red. | Implementación de interfaz de integración expuesta mediante estándares web (SOAP, WSDL o equivalentes). | Integración / interfaz | **No.** | Se registra en **Integraciones_Interfaces** como tipo de interfaz o mecanismo técnico. | Servicio web SOAP con otra entidad. |
| **Integración** | MinTIC MAE reconoce interoperabilidad y arquitecturas de SI; complemento técnico institucional. | Relación implementada entre dos o más sistemas, componentes o entidades para intercambiar datos, eventos o capacidades. | Integración | **No.** | La integración se registra en **Integraciones_Interfaces**. El SI fuente y el SI destino siguen siendo los objetos gobernados principales. | Integración RENARE ↔ ARCA. |
| **Interfaz** | Uso técnico general; consistente con W3C/ISO en separación contrato-implementación. | Punto o contrato de interacción entre soluciones, usuarios o componentes. | Presentación / integración | **No.** | Si es interfaz de usuario, se describe en la Ficha; si es interfaz de integración, se registra en **Integraciones_Interfaces**. | Endpoint REST, WSDL, layout de archivo. |
| **Hub de integración** | Categoría técnica reconocida. | Plataforma centralizadora de conexiones, transformación o enrutamiento entre múltiples sistemas. | Plataforma de integración | **No por defecto.** | Va a **plataformas tecnológicas**. Sus flujos concretos van a **Integraciones_Interfaces**. | Hub institucional de intercambio de datos. |
| **ESB** | Fuente complementaria: OASIS SOA RA. | Patrón o plataforma de integración basada en bus para enrutar, mediar y transformar mensajes entre servicios. | Plataforma de integración | **No por defecto.** | Registrar como **plataforma tecnológica**; no como SI. Las integraciones implementadas sobre él se registran aparte. | Bus corporativo de servicios. |
| **iPaaS** | Categoría reconocida en integración cloud. | Plataforma de integración como servicio para orquestar conexiones entre aplicaciones, datos y procesos. | Plataforma de integración / servicio cloud | **No por defecto.** | Si el Ministerio consume o administra una iPaaS, se registra en **plataformas** o **servicios de TI** según el modelo de operación; sus flujos van a **Integraciones_Interfaces**. | Azure Integration Services, MuleSoft, Boomi. |
| **Middleware** | Fuente técnica general. | Capa de software intermedia que habilita comunicación, seguridad, mensajería o transacciones entre aplicaciones y componentes. | Tecnología / integración | **No.** | Se registra como **plataforma** o **componente técnico**, según su alcance. | Broker de mensajería, servidor de aplicaciones compartido. |
| **API Gateway** | Fuente técnica reconocida: Microsoft Learn / patrones de microservicios. | Componente o plataforma frontal que centraliza exposición, seguridad, limitación, trazabilidad y enrutamiento de APIs. | Integración / plataforma | **No.** | Si es corporativo y compartido, va a **plataformas**; si es específico de una solución, puede ir a **Componentes**. Nunca es el SI de negocio por sí mismo. | Gateway institucional para APIs públicas. |
| **Servicio tecnológico** | En la práctica de gobierno TI, es una capacidad consumida como servicio; MinTIC distingue dominios de gestión TI, no una taxonomía única de esta frontera. | Capacidad tecnológica consumible que habilita operación, soporte, despliegue, colaboración, monitoreo, seguridad o disponibilidad. | Servicio TI / tecnología | **No por defecto.** | Se registra en **catálogo de servicios de TI** o en la hoja correspondiente del libro, no en Catálogo_SI. | Correo, VPN, hosting, monitoreo, repositorio Git. |
| **SaaS** | **NIST SP 800-145** define SaaS como capacidad de usar aplicaciones del proveedor sobre infraestructura cloud que el consumidor no administra. | **Modelo de prestación/despliegue**, no clase de activo. | Atributo transversal | **No; por sí mismo nunca.** | No se inventaría como “tipo de solución” principal. Se usa como valor de **modelo de despliegue / servicio** del SI, plataforma o servicio de TI correspondiente. | Microsoft 365 como servicio; un SI misional consumido como SaaS. |
| **Base de datos** | **ISO/IEC 2382** define base de datos como colección organizada de datos. | Repositorio estructurado de datos administrado por un motor de base de datos. | Datos / tecnología | **No por defecto.** | Si es la base de datos interna de un SI, se documenta en la Ficha o en **Componentes**. Si es un servicio compartido administrado centralmente, va a **plataformas** o **servicios de TI**. | PostgreSQL de un SI; servicio corporativo SQL administrado. |

## 3. Reglas de frontera para casos difíciles

### 3.1 Reglas que se cierran en esta fase

1. **SaaS no es clase de inventario.** Es un atributo de despliegue o servicio.
2. **API, servicio web, interfaz e integración no son SI.** Son contratos, mecanismos o relaciones.
3. **Microservicio, módulo y base de datos no son SI por defecto.** Son partes del SI o de la plataforma.
4. **ERP, CRM, BPM, CMS, SGD, GIS y solución analítica pueden ser SI** solamente cuando cumplen la regla institucional de pertenencia.
5. **Dashboard no se registra como SI salvo excepción justificada** de solución analítica completa con gobierno propio.
6. **Hub, ESB, iPaaS, middleware y API Gateway son plataformas o componentes de integración**, no SI de negocio.

### 3.2 Regla especial para “aplicaciones”

“Aplicación” es un término demasiado amplio para gobernar el portafolio principal. Por tanto:

- si la aplicación cumple la definición institucional de SI, entra a **Catálogo_SI**;
- si no la cumple, se registra como **Componente** o se referencia solo en la **Ficha**.

### 3.3 Regla especial para soluciones analíticas

Una solución analítica **sí puede** ser SI cuando:

- tiene objetivo institucional definido;
- consolida y gobierna datos de negocio o de misión;
- tiene usuarios, responsables y ciclo de vida propios;
- no es solo una visualización dependiente de otra solución.

## 4. Árbol de decisión — ¿Este activo debe ingresar al Catálogo Institucional de SI?

1. **¿El activo soporta directamente uno o más procesos o servicios institucionales y gestiona información del negocio?**
   - **No** → vaya a 6.
   - **Sí** → vaya a 2.
2. **¿Tiene responsabilidad funcional identificable, responsable técnico, ciclo de vida y gobierno propios?**
   - **No** → **B. Componente de un SI** o **F. Otro activo tecnológico**, según corresponda.
   - **Sí** → vaya a 3.
3. **¿La unidad funcional es completa para el usuario institucional, aunque internamente use varios módulos, APIs o componentes?**
   - **Sí** → **A. Sistema de Información**.
   - **No** → vaya a 4.
4. **¿Lo que se está observando es un contrato, endpoint, interfaz, flujo de datos o mecanismo de interoperabilidad entre soluciones?**
   - **Sí** → **C. Integración / Interfaz**.
   - **No** → vaya a 5.
5. **¿Lo que se está observando habilita varias soluciones como capacidad base (motor, bus, gateway, iPaaS, IAM, DB compartida, plataforma BPM)?**
   - **Sí** → **D. Plataforma tecnológica**.
   - **No** → **B. Componente de un SI**.
6. **¿Es una capacidad consumida como servicio para operación o soporte (correo, hosting, monitoreo, VPN, respaldo, repositorio, servicio cloud)?**
   - **Sí** → **E. Servicio de TI**.
   - **No** → vaya a 7.
7. **¿Es solo un atributo o modalidad de prestación (por ejemplo SaaS, on-premises, nube pública)?**
   - **Sí** → **F. Otro activo tecnológico / atributo**, no inventario principal independiente.
   - **No** → vaya a 8.
8. **¿Es únicamente un elemento interno sin gobierno separado (módulo, microservicio, base de datos, dashboard dependiente)?**
   - **Sí** → **B. Componente de un SI** o simple referencia en Ficha si no amerita hoja propia.
   - **No** → **F. Otro activo tecnológico** hasta que OTIC defina un inventario especializado.

## 5. Salida operativa de la Fase 1

### 5.1 Clasificación inequívoca final

- **A. Sistema de Información** → registro en `Catálogo_SI` + `Ficha`.
- **B. Componente de un SI** → registro en `Componentes` cuando tenga identidad técnica relevante; en otro caso, solo en la Ficha del SI.
- **C. Integración / Interfaz** → registro en `Integraciones_Interfaces`.
- **D. Plataforma tecnológica** → registro en hoja o catálogo de plataformas/servicios de soporte; no en `Catálogo_SI`.
- **E. Servicio de TI** → registro en catálogo de servicios de TI; no en `Catálogo_SI`.
- **F. Otro activo tecnológico** → no requiere inventario independiente en este instrumento, salvo decisión posterior de OTIC.

### 5.2 Decisiones críticas que habilitan la siguiente fase

1. El catálogo principal se rediseña para **SI solamente**.
2. El concepto “Naturaleza N1-N8” sale del modelo principal y se reemplaza por una **clasificación previa de hoja** + un **tipo de SI**.
3. Integraciones y componentes se normalizan en hojas separadas.
4. SaaS se trata como atributo, no como solución de primer nivel.

## 6. Fuentes citadas

### 6.1 Fuentes oficiales MinTIC / Gobierno Digital

1. **Resolución 1978 de 2023** — adopta la versión 3 del Marco de Referencia de Arquitectura Empresarial del Estado colombiano. URL: <https://normograma.mintic.gov.co/mintic/compilacion/docs/resolucion_mintic_1978_2023.htm>
2. **Modelo de Gestión y Gobierno de TI (MGGTI)** — portal oficial de documentación. URL: <https://mintic.gov.co/arquitecturaempresarial/>
3. **MGGTI.G.SI — Guía de Dominio de Gestión de Sistemas de Información** — documento oficial usado como referencia general del dominio SI; la verificación directa de la numeración fina de sublineamientos debe hacerse en red institucional. URL: <https://mintic.gov.co/arquitecturaempresarial/630/articles-237662_recurso_1.pdf>
4. **Modelo de Arquitectura Empresarial (MAE/MRAE)** — portal oficial. URL: <https://mintic.gov.co/arquitecturaempresarial/630/w3-propertyvalue-385293.html?__noredirect=1>
5. **Dominio de Arquitectura de Sistemas de Información del MAE** — referencia a las guías `MAE.G.ASI` y `MAE.GE.ASI.01`; no se asume aquí la existencia de una serie separada `MAE.LI.ASI.01-.03`. URL de referencia del dominio: <https://mintic.gov.co/arquitecturaempresarial/>
6. **Decreto 767 de 2022** — actualización de la Política de Gobierno Digital. URL: <https://gobiernodigital.mintic.gov.co/692/w3-article-272977.html>

### 6.2 Fuentes técnicas complementarias reconocidas

1. **NIST SP 800-145** — definición de SaaS. URL: <https://doi.org/10.6028/NIST.SP.800-145>
2. **ISO/IEC 2382** — definiciones de API y base de datos. URLs: <https://www.iso.org/obp/ui#iso:std:iso-iec:2382:ed-1:v1:en> y <https://www.iso.org/obp/ui#iso:std:iso-iec:2382:ed-1:v1:en:term:2121318>
3. **W3C Web Services Architecture** — definición de servicio web. URL: <https://www.w3.org/TR/ws-arch/#webservice>
4. **OASIS SOA Reference Architecture** — referencia para ESB / integración orientada a servicios. URL: <https://docs.oasis-open.org/soa-rm/soa-ra/v1.0/soa-ra.html>
5. **CNCF / microservices.io** — referencias de microservicios como servicios modulares con interfaz definida. URLs: <https://github.com/cncf/toc/blob/main/DEFINITION.md> y <https://microservices.io/>
6. **Microsoft Learn** — patrón de API Gateway en arquitectura de microservicios. URL: <https://learn.microsoft.com/en-us/azure/architecture/microservices/design/gateway>
7. **ISO 19101-1 / Esri** — referencia para GIS. URLs: <https://www.iso.org/standard/59164.html> y <https://www.esri.com/en-us/what-is-gis/overview>
