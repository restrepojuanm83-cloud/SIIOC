# Product Blueprint

**Nombre del proyecto:** INDUSTRIA OS - SIIOC

**Repositorio (enlace obligatorio):** SIIOC (https://github.com/restrepojuanm83-cloud/SIIOC)

> Los campos marcados como *enlace obligatorio* deben ir como enlace en Markdown, con este formato: `[texto del enlace](https://...)`. Reemplacen el texto y la dirección de ejemplo.

---

## Contenido

1. Priorización de historias
2. Propuesta de valor
3. Flujo de usuario
4. Alcance del MVP
5. Lean Canvas
6. Backlog priorizado (Kanban)
7. Arquitectura inicial
8. Uso de Stellar y justificación

---

## 1. Priorización de historias

> Historias elegidas entre las que propuso el equipo y criterio con que se priorizaron. Son las que pasan al backlog. Extensión: breve.

**Criterio de priorización:** Escriban aquí el criterio (por ejemplo, imprescindible / debería / podría / queda fuera).

| Prioridad | Historia | Propuesta por | Por qué entra al backlog |
| :---: | --- | :---: | --- |
| 1 | Como ingeniero de formulación y R&D, quiero registrar y evaluar la factibilidad técnica/regulatoria de un nuevo proyecto cosmético; para evitar falsas aprobaciones cuando existan variables de suministro, normativas o de propiedad intelectual aún no determinadas. | Juan Manuel Restrepo | Escriban aquí su respuesta. |
| 2 | Como director de operaciones industriales, quiero identificar qué datos específicos faltantes tienen mayor capacidad de reducir la incertidumbre al menor costo, para no malgastar recursos industriales persiguiendo métricas irrelevantes. | Juan Manuel Restrepo | Imprescindible. |
| 3 | Como director de investigación y desarrollo, quiero comercializar los proyectos y las fórmulas que nunca se lanzaron al mercado o que nunca pudieron presentarse a los clientes y que actualmente se encuentran en nuestros repositorios internos, para incrementar las ventas por R+D y así poder recuperar de forma parcial o total la inversión realizada en estos proyectos. | Juan Manuel Restrepo | Imprescindible. |
| 4 | Como gestor de calidad de planta, quiero registrar toda la evidencia de cambios y eventos en el repositorio con su respectiva marca temporal y origen, para construir una trazabilidad histórica exacta de cómo el proyecto llegó a su estado actual. | Juan Manuel Restrepo | Imprescindible. |
| 5 | Como auditor de cumplimiento y certificación, quiero que el sistema impida emitir una certificación formal si existen resultados de verificación pendientes o inconclusos, para garantizar que solo lotes 100% verificados reciban luz verde. | Juan Manuel Restrepo | Debería. |
| 6 | Como responsable de tecnología y cumplimiento normativo, quiero generar un hash criptográfico del certificado y anclarlo automáticamente en un contrato inteligente, para disponer de una prueba externa inalterable e independiente de nuestra base de datos interna. | Juan Manuel Restrepo | Podria. |
| 7 | Como cliente B2B o consumidor final, quiero escanear un código QR físico en el empaque del producto o lote, para comprobar instantáneamente en una página web pública la validez del certificado, el hash y su atestación sin requerir acceso al sistema interno. | Juan Manuel Restrepo | Queda fuera. |

*(Agreguen o borren filas según las historias que pasen al backlog.)*

---

## 2. Propuesta de valor

> Qué resultado obtiene el usuario y por qué elegiría esta solución. En qué se diferencia de cómo resuelve hoy. Conecta con el usuario del Problem Brief. Extensión: 150–300 palabras en total.

**Usuario (del Problem Brief):** Directores de Operaciones, Jefes de Calidad, Gerentes de I+D e ingenieros.

**Resultado que obtiene:** Reducir riesgos en el desarrollo de producto. Desbloquear y monetizar comercialmente el portafolio inactivo de fórmulas y proyectos de R+D que nunca llegaron al mercado, transformando activos científicos estáticos en un flujo rentable de ingresos para recuperar la inversión inicial.

**Por qué elegiría esta solución:** INDUSTRIA OS es mas barato, requiere menos personal, hace un analisis completo de la empresa y las variables en menos tiempo y no deja informacion fragmentada entre departamenteos. Permite empaquetar, evaluar mediante el motor de factibilidad y certificar con trazabilidad inmutable y anclaje en Stellar (Soroban) los proyectos dormidos, ofreciendo a los clientes B2B confianza verificable inmediata mediante códigos QR públicos.

**En qué se diferencia de cómo lo resuelve hoy:** Al dia de hoy se solucionan con un exhaustivo seguimiento entre las diferentes areas de la compañia que pueden implicar hasta 5 o mas areas diferentes con varios implicados dentro de cada area; adicionalmente la informacion del proyecto queda fragmentada entre areas y no hay acceso a toda la informacion del proyecto desde el responsable teniendo que hacer varios reprocesos, inversion de tiempo, personal y dinero para lograrlo.

---

## 3. Flujo de usuario

> Recorrido de la persona por la solución de principio a fin, roles y puntos de interacción. Diagrama o secuencia numerada. Extensión: 150–300 palabras.

| Paso | Rol | Qué hace | Punto de interacción |
| :---: | :---: | --- | --- |
| 1 | Proyect manager | Inserta brief del proyecto. | Interfaz de la aplicacion -> crea el codigo de proyecto definitivo stellar automaticamente -> inserta el brief en un recuadro de texto -> analiza ruta critica y siguientes pasos |
| 2 | Ingeniero de R+D | Inserta formula y claims. | Inserta formula y claims |
| 3 | Director de I+D | Administra y comercializa los proyectos. | Publicacion en marketplace B2B -> compra/venta de proyectos de interes ya realizados -> transacciones mediante XLM  |

[ 1. PROJECT MANAGER ] 
       │
       ├─► Inserta Brief del Proyecto en la Interfaz de la Aplicación
       ├─► Crea el código de proyecto definitivo en Stellar de forma automática
       ├─► Inserta el brief en un recuadro de texto estructurado
       └─► Ejecuta el motor para analizar ruta crítica y siguientes pasos
       │
       ▼
[ 2. INGENIERO DE R+D ]
       │
       └─► Inserta la fórmula detallada y claims técnicos en el sistema
       │
       ▼
[ 3. DIRECTOR DE I+D ]
       │
       ├─► Administra y supervisa el portafolio global de proyectos
       ├─► Publica las fórmulas e innovaciones en el Marketplace B2B de INDUSTRIA OS
       └─► Gestiona la compra/venta de proyectos ya realizados mediante transacciones en XLM

*(Agreguen los pasos que hagan falta. Si prefieren, inserten aquí un diagrama.)*

---

## 4. Alcance del MVP

> Funcionalidad central separada de la deseable que queda fuera. Justificación de por qué el recorte sigue entregando valor. Extensión: 150–300 palabras en total.

| Dentro del MVP (funcionalidad central) | Fuera del MVP (deseable, para después) |
| --- | --- |
| Creacion automatica y asociacion del PROJECT ID en Stellar | Marketplace decentralizado de proyectos |
| Analisis de riesgo y ruta critica del proyecto | Seguimiento en la ejecucion del proyecto |
| Acciones correctivas y preventivas | Marketplace decentralizado de mps y productos|
| Motor de factibilidad y desiciones | Documental ID e informacion tecnico-legal asociada |

**Por qué el recorte sigue entregando valor:** Por que despues del analisis del mercado; las funciones integradas en el MVP en este punto es donde se encuentra la mayor friccion, limitantes y perdidas organizacionales.

---

## 5. Lean Canvas

> Lienzo de una página con el modelo del producto. Extensión: enlace (obligatorio).

**Enlace al Lean Canvas (obligatorio):** blockchain builders - SIIOC (https://github.com/users/restrepojuanm83-cloud/projects/1)

El lienzo debe cubrir: problema, segmento de usuarios, propuesta de valor única, solución, canales, métricas clave, ventaja diferencial y estructura de costos e ingresos.

---

## 6. Backlog priorizado (Kanban)

> Enlace al tablero en GitHub Projects, construido con las historias priorizadas, en columnas y con criterios de aceptación por tarjeta. Extensión: enlace al tablero (obligatorio).

**Enlace al tablero (obligatorio):** blockchain builders - SIIOC (https://github.com/users/restrepojuanm83-cloud/projects/1/views/2)

---

## 7. Arquitectura inicial

> Cómo se conectan las partes (interfaz, lógica, Stellar) y en qué punto entra la red. Diagrama simple en imagen. Extensión: 150–300 palabras en total.

**Diagrama (imagen o enlace):** 

[ CAPA 1: INTERFAZ ]         ┌───────────────────────────────────────────────┐
  (Frontend / API REST)       │            [ CAPA 2: LÓGICA INTERNA ]          |
                              │  - Project Data & Dominios (Product, etc.)    │
  - Creación de Proyecto ───► │  - Information & Feasibility Engine (3 Est.)  │
  - Inserción de Fórmula  ───► │  - EvidenceEngine & SQLite (Trazabilidad)     │
  - Solicitud de Cert.    ───► │  - Verification & Certification Engines       │
                              └──────────────────────┬────────────────────────┘
                                                     │
                                                     ▼ (Certificado 100% VERIFICADO)
                                        [ Canonicalización & SHA-256 ]
                                                     │
                                                     ▼
                             ┌───────────────────────────────────────────────┐
                             │          [ CAPA 3: RED BLOCKCHAIN ]           │
                             │                                               │
                             │    Stellar Network / Testnet (Soroban)      │
                             │   - Smart Contract almacena el Hash           │
                             │   - Inmutabilidad y Auditoría Externa         │
                             └──────────────────────┬────────────────────────┘
                                                     │
                                                     ▼
                             ┌───────────────────────────────────────────────┐
                             │          [ VERIFICACIÓN PÚBLICA ]             │
                             │   - Código QR en empaque físico               │
                             │   - Endpoint `/verify/{attestation_id}`       │
                             └───────────────────────────────────────────────┘




| Capa | Componente | Qué hace |
| :---: | --- | --- |
| Interfaz | API REST / Interfaz Web (Frontend). | Recibe los datos de entrada del usuario (briefs del proyecto, fórmulas, claims, solicitudes de certificación). |
| Lógica | Motores de Factibilidad, Decisiones y Evidencia (SQLite) | Procesa los dominios del proyecto, evalúa reglas industriales según la lógica, prioriza el valor de la información, registra la trazabilidad de eventos inmutables y emite certificados formales solo cuando los resultados están 100% verificados. |
| Stellar | Contratos Inteligentes Soroban & Testnet | Actúa como un ancla externa inalterable, almacenando de forma segura el hash del certificado. |

**En qué punto entra la red:** La red entra en acción con un certificado formal y verificado. En ese instante exacto, el sistema aplica un hash a los datos del tecnico-regulatorios, genera un Hash único como PROJECT ID, y ejecuta una transacción hacia la Testnet de Stellar (Soroban) para registrar los hash y los identificador en smart contract.

---

## 8. Uso de Stellar y justificación

> Qué componentes de Stellar usaría y por qué cada uno. Apoyado en el criterio de pertinencia del Problem Brief. Extensión: 150–300 palabras en total.

**Criterio de pertinencia (del Problem Brief):** Escriban aquí el criterio en el que se apoyan.

| Componente de Stellar | Para qué lo usamos | Por qué ese y no otra alternativa |
| --- | --- | --- |
| Soroban (Smart Contracts en Stellar Testnet / Mainnet | Almacenar y ejecutar el registro inmutable de los hashes criptográficos de los certificados y proyectos industriales. | Porque Soroban aporta la flexibilidad de contratos inteligentes con la velocidad y seguridad de la red Stellar, permitiendo auditar la veracidad del certificado frente a alteraciones locales sin la lentitud ni el costo por gas de arquitecturas como Ethereum. |
| Stellar Assets / XLM | Gestionar las transacciones económicas, la liquidación de pagos y la tokenización de los pases de lote o patentes dentro del Marketplace B2B de fórmulas y proyectos de R+D. | Porque el protocolo nativo de Stellar permite emitir, transferir y liquidar activos digitales y pagos de forma casi instantánea y con comisiones de red fracciones de céntimo, a diferencia de pasarelas de pago tradicionales o redes sobrecongestionadas, garantizando viabilidad en transacciones industriales de alto valor. |
