# Guía rápida para armar el dashboard en Power BI

## 1. Cargar datos
1. Abre Power BI Desktop.
2. Inicio → Obtener datos → Excel.
3. Selecciona `Soportes_PowerBI_Base.xlsx`.
4. Marca la tabla `Soportes`.
5. Cargar.

Alternativa: usar `soportes_powerbi.csv`.

## 2. Revisar tipos de datos
En Vista de datos:
- `Fecha`: tipo Fecha.
- `Estado`, `Empresa`, `Canal`, `Asignado A`: Texto.
- `Id Soporte`: Número entero.

## 3. Crear medidas
1. En la tabla `Soportes`, clic derecho → Nueva medida.
2. Copia las medidas del archivo `medidas_powerbi_soportes.dax`.
3. Crea una medida por bloque.

## 4. Diseño recomendado de la página

### Encabezado
Título:
`Dashboard de Soportes - Junio 2026`

Filtros superiores:
- Fecha
- Estado
- Empresa
- Asignado A
- Canal

### KPIs superiores
Usar tarjetas:
- Total Soportes
- Soportes Pendientes
- Soportes En Atención
- Soportes En Proceso
- Soportes En Espera
- Soportes Finalizados
- Soportes Atrasados

### Gráficos
- Gráfico de barras: `Estado` vs `Total Soportes`
- Gráfico de barras: `Empresa` vs `Total Soportes`
- Gráfico de barras: `Asignado A` vs `Total Soportes`
- Gráfico de dona: `Canal` vs `Total Soportes`

### Tabla operacional
Columnas:
- Estado
- Fecha
- Empresa
- Usuario Solicitante
- Canal
- Asignado A
- Descripción del Problema
- Comentarios

## 5. Diseño visual
Importa `tema_powerbi_soportes.json`:
Ver → Temas → Examinar temas.

Colores sugeridos para estado:
- PENDIENTE: rojo
- EN ATENCIÓN: amarillo
- EN PROCESO: azul
- EN ESPERA: naranjo
- FINALIZADO: verde

## 6. Actualización futura
Cuando tengas nuevos datos:
- Mantén la tabla con los mismos encabezados.
- Reemplaza el Excel o conecta Power BI directo al archivo final.
- Presiona Actualizar en Power BI Desktop.