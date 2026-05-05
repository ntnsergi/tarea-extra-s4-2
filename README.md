# Instalación y Despliegue de CouchDB

Esta wiki detalla los pasos para instalar la base de datos NoSQL CouchDB 

---

## 1. Instalación Tradicional

### Prerrequisitos
- Descargar el instalador oficial de acuerdo a tu sistema operativo desde la página de [Apache CouchDB](https://couchdb.apache.org/#download).
<img width="395" height="92" alt="image" src="https://github.com/user-attachments/assets/358c2967-9aaa-454d-ac71-726aaa07413c" />


### Pasos para Windows
1. **Ejecutar el instalador:** Abre el archivo `.exe` o `.msi` descargado y sigue el asistente de instalación.
2. **Configuración de credenciales:** Durante el proceso, el instalador te pedirá configurar el usuario y la contraseña del administrador del gestor de base de datos:
   - **Account Name:** `admin` 
   - **Password:** `tu_contraseña`.
3. **Configuración de Servicio:** Asegurarse de marcar la opción para instalar CouchDB como un servicio de Windows, esto permitirá que la base de datos se inicie automáticamente con el sistema.
4. **Finalizar:** Haz clic en "Install" y espera a que el proceso concluya.


## 2. Levantamiento de Docker con CouchDB

### Prerrequisitos
- Tener instalado Docker Desktop [Docker](https://www.docker.com/products/docker-desktop/)
<img width="1580" height="896" alt="image" src="https://github.com/user-attachments/assets/fce8dbab-33c7-43db-be3d-efc399a21eff" />

### Levantamiento 

#### A. Ejecución del Contenedor
Se utilizó la imagen oficial de CouchDB desde Docker Hub. El comando ejecutado inicializa el motor con variables de entorno para la autenticación administrativa y el mapeo de puertos hacia el host local.

<img width="1478" height="750" alt="image" src="https://github.com/user-attachments/assets/abfee822-03cf-43c5-972a-5f033f3030d8" />


**Detalles del comando:**
- **Variables de Entorno:** Se definieron `COUCHDB_USER` y `COUCHDB_PASSWORD` como `admin`.
- **Puerto:** Mapeo del puerto estándar `5984`.
- **Modo:** `-d` (detached) para ejecución en segundo plano.

#### B. Verificación del Estado del Contenedor
Para asegurar que el servicio se encuentra activo y sin errores de ejecución, se verificó el estado de los procesos en el motor de Docker.


<img width="1475" height="162" alt="image" src="https://github.com/user-attachments/assets/5fe5d6ff-8674-41c2-b4fe-7533ec11754d" />


#### C. Acceso a la Interfaz Administrativa (Fauxton)
Finalmente, se accedió a la herramienta de gestión Fauxton a través del navegador web. Esta interfaz permite la manipulación de documentos JSON y la configuración del clúster de manera visual.

- **URL de acceso:** `http://localhost:5984/_utils/`

<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/3c49e375-29a9-47f2-8cf0-d28f278a12d3" />


