**NOTA: ESTA ES LA MÍNIMA ARQUITECTURA DE LA SECCIÓN DONDE INTERVIENE STELLAR, Y SE HA OMITIDO LA MAYOR PARTE DE LA ESTRUCTURA, ALGORITMO, ENTRE OTRAS COSAS PARA EVITAR LA DIVULGACIÓN; PERO SE MANTIENE EN ESENCIA LA FUNCIONALIDAD DE STELLAR DENTRO DEL PROYECTO.**

# Industria OS - Pasaporte de Lote / RWA

Este repositorio contiene el prototipo y flujo principal del MVP para la gestión y trazabilidad de activos del mundo real (RWA) mediante contratos inteligentes en la red de Stellar (Soroban) e interfaz web en Next.js.

---

## Requisitos Previos

Antes de ejecutar el proyecto, asegúrate de tener instalado en tu equipo:

* **Node.js**
* **npm**
* **Rust & Soroban CLI**

---

## Configuración de Variables de Entorno

El proyecto incluye un archivo `.env` en la raíz preconfigurado con las variables necesarias para interactuar con la **Stellar Testnet**:

> ⚠️ **Nota:** Las claves y credenciales incluidas corresponden exclusivamente a la red de pruebas (*Testnet*) para facilitar la evaluación directa del MVP.


## Instalación y Ejecución Local

Sigue estos pasos para ejecutar la aplicación web en el entorno local:

### PASOS
1. Clonar el repositorio
git clone -b mis-cambios [https://github.com/restrepojuanm83-cloud/SIIOC/tree/mis-cambios/semana3](https://github.com/restrepojuanm83-cloud/SIIOC/tree/mis-cambios/semana3)
Abrir la carpeta del proyecto
cd SIIOC
2. Instalar las dependencias del Frontend
npm install
3. Iniciar el servidor de desarrollo
npx next dev -H localhost
4. Abrir la aplicación
Abre el navegador e ingresa a http://localhost:3000 para interactuar con las pantallas del flujo principal.

-> SE INTRODUCE EL NOMBRE DEL PRODUCTO O PROYECTO
-> SE PRESIONA EL BOTÓN "EMITIR LOTE"
-> SE CREA AUTOMÁTICAMENTE LA TRANSACCIÓN EN STELLAR, LA CUAL ASOCIA EL CÓDIGO DEL PROYECTO Y SU DOCUMENTACIÓN TÉCNICA PARA TRAZABILIDAD Y POSTERIOR COMERCIALIZACIÓN.
**NO SE INCLUYE LA SECCIÓN DE ANÁLISIS DE RIESGOS DE PROYECTOS, NI LOS MOTORES, NI LA INTERFAZ REAL DE LA APLICACIÓN, NI LA SECCIÓN DE COMERCIALIZACIÓN; ESTO SE ILUSTRA A MODO DE DEMOSTRACIÓN**


# Soroban Project

## Project Structure

This repository uses the recommended structure for a Soroban project:

```text
.
├── contracts
│   └── hello_world
│       ├── src
│       │   ├── lib.rs
│       │   └── test.rs
│       └── Cargo.toml
├── Cargo.toml
├── AGENTS.md
└── README.md
```

- New Soroban contracts can be put in `contracts`, each in their own directory. There is already a `hello_world` contract in there to get you started.
- If you initialized this project with any other example contracts via `--with-example`, those contracts will be in the `contracts` directory as well.
- Contracts should have their own `Cargo.toml` files that rely on the top-level `Cargo.toml` workspace for their dependencies.
- Frontend libraries can be added to the top-level directory as well. If you initialized this project with a frontend template via `--frontend-template` you will have those files already included.
