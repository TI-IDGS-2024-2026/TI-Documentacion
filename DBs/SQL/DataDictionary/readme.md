   #  DataDictionary (Diccionario de Datos) ![Mysql](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)

# 📖 Diccionario de Datos  

## 📌 Definición  
Un **diccionario de datos** es un documento o repositorio que describe en detalle los elementos de datos utilizados en un sistema de información. Contiene información como nombres de los campos, tipos de datos, restricciones, relaciones entre tablas y su propósito dentro del sistema.  

## 🔍 Importancia  

### 📌 1. Estandarización  
Garantiza que todos los usuarios y desarrolladores utilicen los mismos términos y definiciones, reduciendo ambigüedades y mejorando la coherencia en el manejo de los datos.  

### 📌 2. Facilita el Diseño de Bases de Datos  
Permite una planificación estructurada de la base de datos, asegurando la integridad y coherencia de los datos dentro del sistema.  

### 📌 3. Mejora la Comunicación  
Sirve como referencia común para **desarrolladores, analistas, administradores de bases de datos y usuarios**, promoviendo una comprensión clara de los datos y su estructura.  

### 📌 4. Documentación para Mantenimiento  
Facilita futuras modificaciones y mejoras en el sistema sin afectar la estructura ni la consistencia de los datos almacenados.  

### 📌 5. Cumplimiento de Normativas  
Contribuye a garantizar que el sistema cumpla con regulaciones de **seguridad y privacidad de datos** como **GDPR** o **HIPAA**, reduciendo riesgos legales y operativos.  


---
# 8°A IDGS - 2025 -   Caso de Estudio : Hospital
---
## 🏥 Aplicación en el Proyecto  
Dado que este proyecto está orientado a la **gestión de Recursos Humanos en un Hospital de Nivel 4**, el diccionario de datos será clave para definir correctamente atributos como:  

|*No.*|*Entidad (Tabla)* |*UDNs Dueño*|*UDNs Escritura*|*UDNs Lectura*|*Documentador*|
|----------|--------|---|-------------|---|----|
|1|Area|RM|RH|Todas|Por definir|
|2|Bitacora|PM|Todas|Todas|Marco R.|
|3|Consumible|RM|RM|Todas|Por definir|
|4|Cirugía|SM|SM,RM|Todas|Por definir|
|5|Cita Medica|SM|SM,RM,RG|Todos|Por definir|
|6|Departamento|RH|RH|Todas|Por definir|
|7|Espacio|RM|RM|Todas|Por definir|
|8|Estudio Medico|SM|SM|Por definir|Por definir|
|9|Medicamento|FR|FR|Por definir|Por definir|
|10|Nacimiento|RG|RH|Por definir|Por definir|
|11|Paciente|RG|RG|Por definir|Por definir|
|12|Persona|RG|RG|Por definir|Por definir|
|13|Personal Médico|RH|RH|Por definir|Por definir|
|14|Puesto|RH|RH|Por definir|Por definir|
|15|Rol|PM|PM|Por definir|MTI. Marco R.|
|16|Servicio Medico|SM|SM|Por definir|Por definir|
|17|Usuario|PM|PM|Todos|MTI. Marco R.|
|18|Valoración Médica|RG|RM|Todos|Por definir|


Abreviaturas de UDN's

   **RM:** Recursos Materiales
   **RH:** Recursos Humanos
   **SM:** Servicios Médicos
   **RG:** Registros Médicos
   **FR:** Farmacia



---
# 8°B IDGS - 2025 -   Caso de Estudio : Gimnasio
---
## 🏋️ Aplicación en el Proyecto  
Dado que este proyecto está orientado a la **gestión de Recursos Humanos en un Hospital de Nivel 4**, el diccionario de datos será clave para definir correctamente atributos como:  


|*No.*|*Entidad (Tabla)* |*UDNs Dueño*|*UDNs Escritura*|*UDNs Lectura*|*Documentador*|
|----------|--------|---|-------------|---|----|
|1|Bitacora|PM - Marco|Todas|Ninguna|MTI. Marco R.|
|2|Cliente|SaC|SaC, CLI|Todas|Jaime V.|
|3|Colaborador|RH|RH| Por definir|Lemuel E.|
|4|Dieta|TR|TR, CLI|Por definir|Orlando M.|
|5|Ejercicio|TR|TR|TR, SaC, CLI|Brayan G.|
|6|Equipamiento|RM|RM|Por definir|Mariano F.|
|7|Espacio|RM|RM|Por definir|Mariano. F.|
|8|Expediente Médico|TR|TR|Por definir|Julia M.|
|9|Horario|RH|RH|Por definir|Jose Luis C.|


Abreviaturas de UDN's

   **GR:** Gerencia
   **RM:** Recursos Materiales
   **RH:** Recursos Humanos



Este documento servirá como referencia fundamental para garantizar la precisión y confiabilidad de la información dentro del sistema.  


---
Creado por: [@MRVargas19](https://github.com/MRVargas19).
Corregido por: [@MTI-MarcoRH](https://github.com/MTI-MarcoRH)

