
# ETL - SSIS

SSIS es una plataforma para la creación de soluciones de integración de datos, como la migración de datos, la transformación de datos y la carga de datos (ETL - Extract, Transform, Load). Se utiliza principalmente en Visual Studio con SQL Server para diseñar y gestionar flujos de trabajo y tareas de integración de datos.

## Funciones y Usos Principales de SSIS

- **Extracción de Datos**: SSIS puede extraer datos desde una variedad de fuentes, incluyendo bases de datos SQL Server, archivos planos, archivos XML, bases de datos de otros sistemas, servicios web, y más.

- **Transformación de Datos**: SSIS proporciona una amplia gama de transformaciones para limpiar, modificar y preparar los datos antes de cargarlos en el destino. Esto incluye operaciones como agregaciones, conversiones de tipos de datos, fusiones, filtrado, ordenación y mucho más.

- **Carga de Datos**: SSIS puede cargar datos en múltiples destinos, como bases de datos SQL Server, archivos, bases de datos de otros sistemas, y más. Permite la configuración detallada de cómo se manejan los errores y la lógica de reintento.

- **Automatización de Tareas**: SSIS permite automatizar tareas rutinarias de administración de datos, como la copia de seguridad de bases de datos, la generación de informes y la sincronización de bases de datos.

- **Integración con Otros Sistemas**: SSIS puede integrarse con otros sistemas mediante componentes específicos para conectarse a diferentes tipos de datos y servicios.

## Requisitos previos

Para utlizar Hello SSIS, asegúrate de tener instalado lo siguiente:

- Visual studio 2022
- Almacenamiento y procesamiento de datos (Server Data Tools, Herramientas de desarrollo de .NET Framework 4.7.2)
- Extensión: SQL Server Integration Services Projects 2022
- SQL Server Management Studio 2019 (SSMS) y cambiar el estado de los protocolos Named Pipes and TCP/IP a Enabled 


## Instalación

Sigue estos pasos para instalar y configurar Hello SSIS en tu entorno local:

1. Clona el repositorio  desde GitHub:
```bash 
git clone https://github.com/david-mrios/ETL-SSIS.git
```
2. Recomendación:

    -  Realizar la instalación en la raiz del disco local C:\ 

    - Si se elige otra dirección, en el paquete importXML deberá cambiar la ubicación de cada flujo de tarea. Dentro del paquete, en el origen XML, es necesario ajustar tanto la ubicación del XML como del XSD correspondiente al nuevo destino de datos que se encuentra en la carpeta data.

    - Si lo descarga directamente sin clonarlo, enfrentará el mismo error de ubicación dentro del import XML, ya que al no clonarlo se cambia el nombre de la carpeta.

## Ejecución

- Restaurar las bases de datos "TecnoNic.bak" y "TecnoNic_DW.bak" en SQL Server Management Studio (SSMS), ten en cuenta que estas solo contienen la estructura.

- Verifica las conexiones a la base de datos. Aunque dejamos la conexión con localhost, así que no debería haber ningún problema. En caso de necesidad, modifica las conexiones a la base de datos.

- Si las direcciones del archivo XML de origen no presentan problemas, procederé a ejecutar el paquete de importación XML para rellenar el dll.

- En caso de que falle la importación XML, eliminaré la base de datos "TecnoNic.bak" y restauraré el archivo .bak desde la carpeta de respaldo completa. 

- Finalmente, ejecutaré el paquete load_Dw para completar el proceso ETL.

## Visita el repositorio para obtener más información sobre la creación del ETL en SQL Server: "

[ETL SQL SERVER](https://github.com/david-mrios/ETL-SQL-SERVER.git)

