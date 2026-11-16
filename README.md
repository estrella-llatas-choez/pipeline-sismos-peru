# Pipeline de Sismos en el Perú 1960 al 2025

## Objetivo
Pasar de datos crudos a información útil y fácil de leer

Realizar el proceso ETL a los datos, guardarlos en bases de datos y mostrarlos en un dashboard

## Datos
### Origen 
Plataforma Nacional de datos abiertos (Perú)

### Nombre del dataset 
Datatset del Catálogo Sísmico desde 1960 al 2025 - [Instituto Geofísico del Perú - IGP]

### Descripción
> Para este catálogo, se ha considerado los parámetros hipocentrales publicados desde el Centro Sismológico Nacional (CENSIS) usando datos de la Red Sismica Nacional (RSN) a cargo del IGP. Esta red, se ha incrementado después del año 2000 logrando mejor cobertura a nivel nacional y el registro de un numero mayor de sismos. Para mas información visitar el siguiente enlace:  https://ultimosismo.igp.gob.pe/descargar-datos-sismicos

## Herramientas
- GitHub
- Google Colab
- Python
- Pandas
- PostgreSQL
- Power BI

## Columnas

| Variable | Descripción | Tipo de Dato | Formato |
| :---: | :---: | :---: | :---: |
| FECHA_CORTE | Fecha peruana en la que se cargaron los datos de sismos (por confirmar) | Numérico | aaaammdd |
| FECHA_UTC | Fecha universal, es la fecha peruana más 5 horas | Numérico | aaaammdd |
| HORA_UTC | Hora universal, es la hora peruana más 5 horas | Numérico | hhmmss |
| LATITUD | Distancia en grados, minutos y segundos con respecto al paralelo principal (Ecuador). Puede ser norte o sur | Float | |
| LONGITUD | Distancia en grados, minutos y segundos con respecto al meridiano principal (meridiano de Greenwich) | Float | |
| PROFUNDIDAD | Es la distancia debajo de la superficie donde sucedió el sismo | Numérico | |
| MAGNITUD | Cantidad de energía liberada por el sismo en magnitud momento Mw | Float | |

## Problemas detectados y dudas
- FECHA_CORTE: Tiene formato mezclado (ejemplos 20231910 y 20260528)
- Posible hueco en FECHA_UTC entre2023 y 2025 (por confirmar)
- HORA_UTC pierde los cero s de la izquierda (000530 queda como 530)
- El diccionario dice 1960-2023, pero el dataset tiene hasta 2025

## Preguntas
Preguntas:
1. ¿Cuándo suceden los sismos con mayor frecuencia o mayormente?
2. ¿Dónde  estan sucediendo la mayor cantidad de sismos?
3. ¿Qué tan fuertes son mayormente los sismos?
4. ¿A que profundidad ocurren la mayoria de sismos?