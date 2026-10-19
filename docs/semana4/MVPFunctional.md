**LINK DE VIDEO Y EVIDENCIA DE FUNCIONALIDAD**
En la documentación coloquen la evidencia verificable de que todo está funcionando, por ejemplo, el enlace al producto en línea, el enlace al video público y, si usan contratos propios, los enlaces a los contratos y a sus transacciones en el explorador de testnet (es obligatorio, así verificamos que los contratos se hicieron). Cualquier persona debe poder abrirla y comprobarlo.

VIDEO DE DEMOSTRACIÓN
[https://youtu.be/9ItjQGIeiqI](https://youtu.be/9ItjQGIeiqI)

LINK - TRANSACCION STELLAR EXPERT DE EJEMPLO [https://stellar.expert/explorer/testnet/tx/3490d7525864d080b1714955a85a98d387ec1517ff67f8c8960cbfc569b6e76d](https://stellar.expert/explorer/testnet/tx/3490d7525864d080b1714955a85a98d387ec1517ff67f8c8960cbfc569b6e76d)

OTROS CREADOS DE LA MISMA FORMA:
https://stellar.expert/explorer/testnet/tx/eecf90eaebc226a2298263fd9606261be91d9d77cad5d3c52f9f4152b0a77c86
https://stellar.expert/explorer/testnet/tx/dbb8debec58d5257057959bb1b9e03f5a71e7fbafd7476ec6809dda9f950a4eb
https://stellar.expert/explorer/testnet/tx/eb2924f4eb676aac36ab91e3b402150e99cbb61ac755602a235dfc8a6633edb7

**APRENDIZAJES Y AJUSTES PRIORIZADOS**
Qué aprendió el equipo y qué cambios hará, ordenados por impacto y esfuerzo. Qué se ajusta antes del cierre y qué queda pendiente.

**¿Qué se aprendió?**
1. Rigurosidad en la Máquina Virtual de Soroban: Los contratos escritos en Rust y ejecutados en Soroban exigen precisión en el tipado desde el frontend; cualquier discrepancia en los enteros genera un fallo inmediato en la simulación de la transacción.
2. Resiliencia ante la infraestructura descentralizada: Las redes de almacenamiento auxiliar IPFS y las pasarelas públicas presentan intermitencias o caídas de red.
3. Validación de estados en la Testnet: El uso de hashes transaccionales verificables en Stellar Expert proporciona una capa de confianza inmutable esencial para la trazabilidad.

**AJUSTES**
1. Conexión exitosa con el contrato RWABatchContract en la Testnet de Stellar mediante la función emitir_lote.
2. Interfaz funcional en Next.js capaz de registrar el nombre del producto, emitir el lote en la blockchain y mostrar los identificadores de cumplimiento.
3. Visor de metadatos integrado que garantiza la visualización instantánea de los certificados sin depender de nodos IPFS externos caídos.


**RIESGOS Y PENDIENTES**
Riesgos identificados antes del cierre y qué queda por resolver.

**RIESGOS**
1. Caducidad de Estado en Soroban (Riesgo Alto): Si esta gestión se omite, los datos del lote registrados en la blockchain pueden expirar y ser archivados por la red. Es necesario programar la lógica de extensión de ledger (extend_ttl) directamente en el ciclo de vida del contrato en Rust.
2. Gestión de Llaves Privadas y Firma Local (Riesgo Alto): La solución consiste en migrar hacia la integración de monederos de usuario para que cada operador firme las transacciones desde su propia wallet.
3. Disponibilidad de Metadatos e IPFS: Se mitiga contratando un servicio de pinning dedicado (como Pinata Pro o Filecoin) que garantice la inmutabilidad de los archivos.
4. Límites de Gas y Concurrencia (Riesgo Bajo): Las fluctuaciones de tráfico en la Testnet de Stellar pueden retrasar la confirmación de bloques.

**PENDIENTES**
1. Integración de Freighter Wallet: Conectar la interfaz con la extensión de navegador para que el usuario firme las transacciones de emisión de lotes en lugar de depender de un perfil administrativo simulado.
2. Auditoría de Seguridad del Contrato Rust: Revisar vulnerabilidades lógicas en Soroban, asegurando un control de acceso estricto en la función emitir_lote y una validación rigurosa de los tipos de datos de entrada.
3. Manejo Robusto de Errores en la Interfaz: Incorporar mecanismos de reintento automático y notificaciones visuales detalladas para informar al operador ante fallos en la estimación de comisiones de gas de la red.
4. Despliegue en Mainnet: Configurar los parámetros definitivos y ejecutar los scripts de migración para llevar los contratos validados a la red principal de Stellar.



**PLAN DE VALIDACIÓN CON USUARIOS**
Cómo validarán el producto con sus usuarios a futuro: a quiénes (el usuario del Problem Brief), con qué métodos (entrevistas, pruebas con el producto, métricas, etc), qué hipótesis comprobarán y con qué criterio sabrán que se cumplen.

Ya se cuenta con entrevistas de potenciales clientes.

**Público Objetivo**
1. Empresas de desarrollo de producto y materias primas: encargadas de crear lotes de productos y materias primas farmacéuticas, cosméticas y alimenticias.
2. Gerentes de operaciones e investigación y desarrollo: Responsables de la operación de formulación y desarrollo de proyectos.

**Métodos de Validación**
1. Pruebas de usabilidad en entorno controlado: Se pedirá a los usuarios que ejecuten el flujo completo de forma autónoma durante la operación.
2. Entrevistas de retroalimentación: Sesiones enfocadas en identificar fricciones cognitivas, claridad en los estados de carga y utilidad de la visualización de metadatos.
3. Rendimiento del sistema: Medición cuantitativa de la respuesta del sistema y tasas de éxito.

**Hipótesis**
1. Hipótesis 1 (Eficiencia de Registro): La emisión de pasaportes de lotes mediante contratos inteligentes en Stellar reduce drásticamente el tiempo y la probabilidad de errores humanos en comparación con los registros tradicionales en papel o archivos locales dispersos.
2. Hipótesis 2 (Accesibilidad de Metadatos): Un visor de documentos integrado en la misma interfaz elimina la fricción generada por la inestabilidad de las pasarelas IPFS públicas, mejorando la confianza del usuario final.
3. Hipótesis 3 (Curva de Aprendizaje): Un profesional de la química cosmética sin conocimientos previos en blockchain puede operar con éxito el panel en menos de cinco minutos gracias al tipado estricto y a los mensajes de estado claros.

**Criterios de Éxito**
1. Tasa de éxito transaccional: Al menos un 95% de los lotes de prueba emitidos por los usuarios se registran y confirman sin errores en la Testnet de Stellar.
2. Tiempo de operación: El proceso completo de registro, emisión y consulta de documentos toma menos de dos minutos por lote.
3. Satisfacción de uso: Obtener una valoración positiva superior al 80% en las encuestas de facilidad de uso de la interfaz y claridad de los informes de calidad.
