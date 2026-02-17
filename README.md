Descripción

Programa COBOL básico que lee un archivo CSV y genera un archivo .xls (formato HTML reconocido por Excel).

Archivos creados en Documents

- convert_csv_to_xls.cob : código fuente COBOL
- sample.csv              : CSV de ejemplo
- output.xls              : archivo generado al ejecutar el programa

Requisitos

- GNU COBOL (cobc). En macOS puede instalarse con Homebrew: `brew install gnu-cobol`.

Compilar

```bash
cobc -x -free -o /Users/marcelofelice/Documents/csv2xls /Users/marcelofelice/Documents/convert_csv_to_xls.cob
```

Ejecutar

```bash
/Users/marcelofelice/Documents/csv2xls
```

El programa leerá `/Users/marcelofelice/Documents/sample.csv` y escribirá `/Users/marcelofelice/Documents/output.xls`.

Notas

- El programa usa un máximo de 20 columnas por fila; celdas vacías se mantienen.
- `output.xls` es un archivo HTML que Excel abrirá como hoja de cálculo.
- Si desea usar otros nombres, edite las rutas en la sección `FILE-CONTROL` del archivo COBOL.
