# Evaluación Final: Transformación de datos con Python

A continuación se describen las diferentes fases realizadas en la evaluación final correspondiente al tercer módulo del bootcamp de Data Analytics

### Archivos en el repositorio
1. Bases de datos:
    - "Customer Loyalty History": csv con información sobre los clientes de una empresa aérea canadiense 
    - "Customer Flight Activity": csv con información sobre los vuelos realizados por los clientes en los meses de 2017 y 2018
    - "Clients and Flights": csv con la unión de las 2 base de datos anteriores y con la limpieza de datos realizada que incluye, entre otros, gestión de nulos, duplicados, homogeneización de datos, etc. Esta Base de datos final contiene las siguientes variables

        - Loyalty Number: ID del cliente
        - Gender: Género del cliente
        - City: Ciudad del cliente
        - Province: Provincia del cliente
        - Country: País del cliente
        - Postal Code: Código postal del cliente
        - Education: Nivel educativo del cliente
        - Groups: Grupo del AB testing al que pertenece el cliente de acuerdo a nivel educativo
        - Marital Status: Estado civil del cliente
        - Salary: Salario del cliente
        - Loyalty Card: Tipo de tarjeta de lealtad del cliente
        - Enrollment Type: Tipo de inscripción realizada por el cliente
        - CLV: Customer Lifetime Value del cliente
        - Flights Booked: Nro de vuelos reservados por mes y año del cliente
        - Month: Mes de reserva del vuelo
        - Year: Año reserva del vuelo
        - Distance: Distancia de vuelos
        - Flights with Companions: Nro de vuelos con acompañantes
        - Total Flights: Número total de vuelos
        - Points Accumulated: Puntos acumulados por el cliente
        - Points Redeemed: Puntos canjeados por el cliente
        - Dollar Cost Points Redeemed: Coste de los puntos canjeados por el cliente

2. Archivo jupyter: Contiene el código relacionado con las siguienes fases en el tratamiento de datos:
        - Fase 1: Exploración y limpieza de datos
        - Fase 2: Visualización de datos
        - Fase 3: AB Testing 

### Fases en el análisis de datos

##### Fase 1: Exploración y limpieza

- Exploración inicial de los datos para identificar posibles problemas, como valores nulos, atípicos o - datos faltantes en las columnas relevantes
- Utilización de Pandas para obtener nformación sobre la estructura de los datos, la presencia de valores - nulos y estadísticas básicas de las columnas involucradas
- Union de las 2 bases de datos de manera eficiente
- Eliminación y tratamiento de valores nulos para asegurar que los datos estén completos.
- Verificación de la consistencia y corrección de los datos para asegurarte de que los datos se presenten - de forma coherente
- Realización de ajustes en columnas para garantizar la adecuación de los datos para el análisis - estadístico

##### Fase 2: Análisis visual
Se ha analizado de forma visual las siguientes distribuciones y relaciones de los datos:
- Distribución de la cantidad de vuelos reservados por mes durante el año
- Relación entre la distancia de los vuelos y los puntos acumulados por los clientes
- Distribución de los clientes por ciudad y provincia
- Comparación del salario promedio entre los diferentes niveles educativos de los clientes
- Análisis de la proporción de clientes con diferentes tipos de tarjetas de fidelidad
- Distribución de los clientes según su estado civil y género

##### Fase 3: AB testing
Se ha realizado un AB testing para entender si el nro. de vuelos reservados varía según el nivel educativo de los clientes. Para ello se han realizados los siguientes pasos: 
- Preparación de datos:
    Realizar los ajustes necesarios para agrupar los datos de acuerdo a los 2 grupos para nuestro AB testing:
    - Grupo de control: Clientes con un nivel educativo alto (niveles educativos: Doctor, Master, Bachelor)
    - Grupo de test: Clientes con un nivel educativo bajo (niveles educativos: High School or below, College)

- Realización de estadísticas descriptivas de nuestra métrica (KPI): Vuelos reservados
- Realización de una prueba de A/B testing para determinar si existe una diferencia significativa en el número de vuelos reservados entre los diferentes niveles educativos
- Reporte de resultados: No existen evidencias suficientes para rechazar la hipótesis nulas, 
 y por tanto podemos afirmar q no existe una diferencia significativa entre las medias de ambos grupos 
 y q por tanto, la media de vuelos reservados no difiere por nivel educativo
 