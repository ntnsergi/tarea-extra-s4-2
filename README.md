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


