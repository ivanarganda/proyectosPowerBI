# Concesionario — Guía y documentación

Resumen corto

- Proyecto Power BI que utiliza un origen de datos local (bbdd_coches_new.xlsx) y recursos de configuración d

Estructura del repositorio

- /Settings

  - map.json — configuración de mapa (colores / proyección).

    - bbdd_coches_new_CLASSROOM.pbids — archivo de conexión que apunta a un Excel en la ruta del aula.
    - bbdd_coches_new_HOME.pbids — archivo de conexión que apunta a la ruta de desarrollo local (usuario).

- images/ — carpeta con recursos gráficos (fondos, formas) usados en el informe.
- README.md — este documento.

Requisitos

- Archivo de datos: bbdd_coches_new.xlsx (debe estar presente en la ruta indicada por .pbids o abrirse manualmente en Power BI).
- Archivos dentro de /Settings y /images disponibles en el mismo árbol del proyecto.

Cómo abrir el proyecto en Power BI Desktop

     - Abrir el archivo `.pbids` (doble clic en Windows o abrir desde Power BI -> Open).
     - Si la ruta del archivo Excel no coincide con tu equipo, edita el `.pbids` (ver abajo).

2. Si prefieres hacerlo manual:

Editar la ruta del archivo en los .pbids

- Los `.pbids` son JSON simples. Ejemplo (reemplazar la ruta por la tuya):

  ```json
  {
      "version": "0.1",
      "connections": [
          {
                    "protocol": "file",
                    "address": { "path": "C:\\ruta\\a\\tu\\bbdd_coches_new.xlsx" },
                    "authentication": null,
                    "query": null
                },
                "options": {},
                "mode": null
            }
        ]
    }
  ```

- En Windows Powe
  (Get-Content bbdd_coches_new_CLASSROOM.pbids) -replace 'c:\\users\\bigdata\\desktop\\curso-inserta-big-data\\proyectospowerbi\\concesionario\\bbdd_coches_new.xlsx','C:\\tu\\ruta\\bbdd_coches_new.xlsx' | Set-Content bbdd_coches_new_CLASSROOM.pbidsrS

  ```

  ```

- `map.json`, `change_apearance_slicers.json`: importar o copiar el JSON según el visual que lo demande (algunos visuales permiten importar temas o configuraciones).

Imágenes y assets

## Buenas prácticas

Mantener el

- Si se publica al servicio Power BI, reemplazar conexiones a archivos locales por fuentes en la nube o datasets publicados.

Solución de problemas

- Error al abrir .pbids: verificar que la ruta existe y que Power BI tiene permisos para leer el archivo.
- Visual de mapa no carga GeoJSON: comprobar formato GeoJSON y la coincidencia de campos (pr

Checklist antes de compartir el proyecto

- [ ] Actualizar .pbids con rutas relativas si es posible.
- [ ] Verificar archivos en /Settings y /images incluidos en el repositorio.
- [ ] Añadir notas de cambio en este README si se modifica el modelo.

Contacto y mantenimiento

- Incluir aquí información del responsable del proyecto o del repositorio (email / slack / equipo), o crear un ISSUE para cambios.

Licencia

Notas finales

- Este README es una plantilla básica. Si se desea, se puede ampliar con:

  - Diagrama de modelo de datos.

    - Instrucciones de despliegue en Power BI Service.

  - Lista de medidas DAX clave.
    - Flujos ETL en Power Query (paso a paso).

- Añadir fichero LICENSE si aplica (MIT/Apache/privado).
- [ ] Incluir `bbdd_coches_new.xlsx` o documentar dónde obtenerlo.opiedades) entre datos y archivo geo.

- Datos no se actualizan: abrir Power Query y comprobar pasos aplicados; refrescar conexión.

- Documentar cambios importantes en el data model (tablas añadidas, columnas calculadas) en este README.
  archivo Excel
  fuera de
  rutas temporales o sincronizadas cuando se use en producción.
- Carpeta `images` contiene fondos y formas; enlazar desde Power BI (Insert → Image) o como fondo de página.
- Mantener nombres y rutas relativas para evitar romper vínculos al mover el proyecto.

- `map.geojson`: colocarlo en la misma ruta cuando se configure un visual de mapa que requiera el GeoJSON.

Uso de la carpeta Settingshell puedes reemplazar la ruta con:

```powershell

            "details": { - Ajustar consultas en Power Query si es necesario.

- En Power BI Desktop: Home → Get data → Excel → seleccionar `bbdd_coches_new.xlsx`.

```

```

```

1. Si deseas usar la conexión automática:

- Power BI Desktop (última versión recomendada).

- PowerBIPerformanceData.json — archivo de performance (vacío/placeholder).

- .pbids

  - map.geojson — datos geográficos (GeoJSON) usados por mapas personalizados.

  - change_apearance_slicers.json — personalizaciones para slicers (apariencia).entro de la carpeta `Settings`.

- Estructura mínima del repositorio incluida en este README para facilitar apertura y despliegue del informe.
