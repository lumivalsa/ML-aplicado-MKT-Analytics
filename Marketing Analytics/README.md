# Market Analytics


## Contexto
>Nos encontramos con una base de datos de marketing donde se han realizado ciertas camapañas de marketing para incrementar las ventas. Por ello en este trabajo realizaremos un analisis profundo y utilizaremos técnicas de Machine Learning para 

> Enlace de Kaggle: 
https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign

## Objetivos
- Segmentar a nuestro cliente 
- Seleccion que tipo de producto se adecuan más a nuestro cliente según su perfil

## Sección 01: Análisis exploratorio de datos
- Importamos las librerias necesarias
- Cargamos la data
- Realizamos un primer analisis de la información
- Eliminamos valores nulos 
- Transformamos las fechas

## Sección 02: Análisis estadístico
- Compras realizadas
- Cantidad de profesionales que realizan la compra
- Visualizamos los estados civiles para poder saber quienes son nuestros mayores clientes.
- Aceptaciones por campaña
- Valores atipicos
- Creación de nuevas columnas 
- Visualizamos Numero de compras vs Numero de visitas por mes

## Sección 03: Preprocesamiento de datos 

- Limpieza de la información
- Selección de las Feature Importance
- Aplicamos un get dummies al estado civil 

## Sección 04: Segmentacion de mercado (Clustering)
- Modelo 1 Kmeans con Cluster 5 con estandarizacion robusta
- Modelo 2 Kmeans con Cluster 4 con Standart Scaler

## Sección 06: Seleccion que tipo de producto se adecuan más a nuestro cliente según su perfil
- Evaluamos el total de compras y realizamos una prediccion 
- Preddicion Random Forest para el producto
## Sección 05: Conclusiones


## Columnas
AcceptedCmp1 - 1 si el cliente aceptó la oferta en la 1.ª campaña, 0 en caso contrario
AcceptedCmp2 - 1 si el cliente aceptó la oferta en la 2.ª campaña, 0 en caso contrario
AcceptedCmp3 - 1 si el cliente aceptó la oferta en la 3.ª campaña, 0 en caso contrario
AcceptedCmp4 - 1 si el cliente aceptó la oferta en la 4.ª campaña, 0 en caso contrario
AcceptedCmp5 - 1 si el cliente aceptó la oferta en la 5.ª campaña, 0 en caso contrario
Response (objetivo) - 1 si el cliente aceptó la oferta en la última campaña, 0 en caso contrario
Quejar - 1 si el cliente se quejó en los últimos 2 años
DtCliente - fecha de inscripción del cliente en la empresa
Education - nivel de educación del cliente Civil -
estado civil del cliente
Kidhome: número de niños pequeños en el hogar del cliente
Teenhome: número de adolescentes en el hogar del cliente
Income: ingreso anual del hogar del cliente
MntFishProducts: cantidad gastada en productos pesqueros en los últimos 2 años
MntMeatProducts: cantidad gastada en productos cárnicos en los últimos 2 años
MntFruits: cantidad gastado en productos de frutas en los últimos 2 años
MntSweetProducts - cantidad gastada en productos dulces en los últimos 2 años
MntWines - cantidad gastada en productos de vino en los últimos 2 años
MntGoldProds - cantidad gastada en productos de oro en los últimos 2 años
NumDealsPurchases - número de compras hecho con descuento
NumCatalogPurchases - número de compras hechas usando el catálogo
NumStorePurchases - número de compras realizadas directamente en las tiendas
NumWebPurchases - número de compras realizadas a través del sitio web de la empresa
NumWebVisitsMonth - número de visitas al sitio web de la empresa en el último mes
Recency - número de días desde la última compra

Desarrollamos nuevas columnas(Feature Engineering)

- Join_year: el año en que esa persona se convirtió en cliente, que se puede diseñar a partir de "Dt_Customer"
- Join_month: el mes en que esa persona se convirtió en cliente, que se puede diseñar desde "Dt_Customer"
- Join_weekday: el día de la semana en que la persona se convirtió en cliente, que se puede diseñar desde "Dt_Customer"
- Minorhome: La cantidad total de menores en su familia, que pueden ser adquiridas sumando por Kidhome y Teenhome.
- Total_Mnt: Monto total gastado en los últimos dos años, que se puede adquirir sumando todas las columnas relacionadas con "Mnt"
- Total_num_purchase: Número total de compras en los últimos dos años, que se puede adquirir sumando todas las columnas relacionadas con "Num"
- Total_accept: monto total que un cliente aceptó la oferta en la campaña de marketing, que se puede adquirir sumando todas las columnas relacionadas con "Aceptado" y la columna "Respuesta"
- "AOV": AOV representa el volumen de pedido promedio de cada cliente, que se puede diseñar dividiendo Total_Mnt por Total_num_purchase

Conclusiones:

Según el clustering hemos podido dividir a nuestro cliente en 5 grupos y realizar un analisis de los productos y del cliente promedio
Cliente Promedio
- tiene un ingreso anual de 52200 dolares
- había comprado hace 49 días
- tiene un AOV de 26,8 dólares
- ha gastado 605 dolares
- ha comprado 20 veces
- se hizo cliente a mediados de junio
- se hizo cliente el jueves
- gastó más en vinos (300 dólares) y luego en productos cárnicos (165 dólares)
- gastó menos en frutas (26 dólares) y productos dulces (27 dólares

Caracteristicas a considerar en un campaña de Mk: 
- Años
- Ingresos
- Cuantos menores hay en casa
- Fecha de Registro
- Productos de: carne, vino, pescado, frutas, productos dulces.
- Canales: Numero de ventas, Compras por catalogo, Compras por la tienda
- Total: Volumen del pedido promedio, Numero de compras, Total de monto gastado. 