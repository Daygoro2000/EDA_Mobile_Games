Markdown
# EDA: Videojuegos Convencionales vs. Industria Móvil

Análisis exploratorio de datos (EDA) que compara el rendimiento financiero y la evolución del mercado tradicional de videojuegos (consola y PC) frente al crecimiento de la industria móvil.

## Sobre el proyecto
El gaming móvil ha pasado de ser una alternativa casual a dominar los ingresos globales del sector. Este repositorio analiza y compara las ganancias de ambos mercados cruzando datos históricos de ventas tradicionales con los títulos móviles más rentables hasta la fecha, buscando patrones por género, año de lanzamiento y desarrolladora.

## Qué encontrarás en este análisis
Para poder comparar ambos mercados en igualdad de condiciones, el notebook incluye el siguiente flujo de trabajo:

1. **Limpieza y estandarización:** 
   - Tratamiento de valores nulos y ajuste de tipos de datos (fechas, enteros).
   - Estandarización de las categorías de `Género` entre ambos datasets.
   - Unificación de títulos multiplataforma clave (ej. *Grand Theft Auto V*) para reflejar sus ventas reales acumuladas.
2. **Estimación de ingresos:** 
   - El dataset tradicional mide unidades vendidas (en millones), no ingresos directos. Se calculó una columna de `Ganancias` estimando un precio medio de **$50 por copia** para poder cruzarlo directamente con el revenue móvil.
3. **Comparativa del Top 100:** 
   - Filtrado de los 100 juegos convencionales más rentables para equiparar el tamaño de la muestra con el dataset móvil (104 registros) y creación de un dataset fusionado.
4. **Visualización de datos:** 
   - Distribuciones de ganancias, comparativas por género y evolución cronológica de los ingresos en ambas plataformas.

## Datasets utilizados
Los archivos se encuentran en el directorio `./EDA/`:
* `mobile-games.csv`: Top de juegos móviles por ingresos históricos, fecha de lanzamiento, publisher y género.
* `video_games_sales.csv`: Histórico de ventas de videojuegos en consolas y PC desglosado por regiones (Norteamérica, Europa, Japón y resto del mundo).

## Requisitos y tecnologías
El análisis está desarrollado en **Python**. Para ejecutar el notebook necesitarás las siguientes librerías estándar de ciencia de datos:

* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
