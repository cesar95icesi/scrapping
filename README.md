# README

## Descripción

Este script automatiza la descarga de datos de municipios desde el sitio web de [CHIP](https://www.chip.gov.co/schip_rt/index.jsf). Utiliza Selenium para interactuar con la página web y Pandas para manipular los datos. El script realiza las siguientes tareas:

1. Carga un archivo CSV con información de municipios.
2. Genera una nueva columna con el formato "IdEntidad - Municipio".
3. Itera sobre cada municipio y descarga los datos correspondientes desde el sitio web de CHIP.
4. Guarda los archivos descargados en una carpeta específica.
5. Registra los municipios que no pudieron ser procesados en un archivo CSV.

## Requisitos

- Python 3.x
- Pandas
- Selenium
- Un navegador Chrome instalado
- El driver de Chrome correspondiente a la versión del navegador (chromedriver)

## Instalación

1. Clona este repositorio o descarga los archivos.
2. Instala las dependencias necesarias ejecutando:

    ```bash
    pip install pandas selenium
    ```

3. Asegúrate de tener el driver de Chrome (chromedriver) en tu PATH o en el mismo directorio del script.

## Uso

1. Coloca el archivo CSV con los municipios en la carpeta `municipios` y asegúrate de que se llame `Municipios_Chip.csv`.
2. Modifica las rutas de destino y de descarga en el script según tus necesidades.
3. Ejecuta el script:

    ```bash
    python script.py
    ```

    4. (Opcional) Crea un entorno virtual para aislar las dependencias del proyecto. Puedes hacerlo ejecutando:

        ```bash
        python -m venv venv
        ```

        Activa el entorno virtual:

        - En Windows:

            ```bash
            .\venv\Scripts\activate
            ```

        - En macOS y Linux:

            ```bash
            source venv/bin/activate
            ```

    5. Instala las dependencias desde el archivo `requirements.txt`:

        ```bash
        pip install -r requirements.txt
        ```

4. Los archivos descargados se guardarán en la carpeta especificada en `destination_dir`.
5. Si hay municipios que no pudieron ser procesados, se guardarán en un archivo CSV llamado `municipios_no_procesados.csv`.

## Notas

- Asegúrate de que el sitio web de CHIP esté accesible y que los elementos de la página no hayan cambiado, ya que esto podría afectar el funcionamiento del script.
- Puedes ajustar los tiempos de espera (`time.sleep`) según la velocidad de tu conexión y el rendimiento del sitio web.

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para discutir cualquier cambio que desees realizar.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.
