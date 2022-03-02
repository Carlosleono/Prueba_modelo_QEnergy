# Prueba_modelo_QEnergy

## 1.       Modelo de predicción de demanda diaria de electricidad en España:

 

Para este apartado se pide implementar un modelo de predicción del consumo diario de electricidad en España. Como contexto del apartado, el consumo de electricidad tiene estacionalidad y una fuerte dependencia de la laboralidad y la temperatura. El modelo debe predecir el consumo de electricidad del día siguiente, suponiendo una predicción de temperatura.

 

Los datos históricos de demanda de electricidad en España y otra información adicional pueden descargarse a través de la API de la página de e-sios de Red Eléctrica Española: https://www.esios.ree.es/es/pagina/api. Los datos también están disponibles en la página web de e-sios: Análisis | ESIOS electricidad · datos · transparencia (ree.es). Se puede utilizar el indicador 10027 (demanda programada P48 total). Los datos de temperatura se proporcionan en adjunto a este correo. La serie dada es la temperatura media diaria sin ponderar de los 16 municipios más poblados de España, obtenida con datos de la Agencia Estatal de Meteorología: Agencia Estatal de Meteorología - AEMET. Gobierno de España.

 

Se piden los siguientes subapartados:

 

### 1.1   Análisis exploratorio de datos

### 1.2   Definición del modelo propuesto

### 1.3   Entrenamiento, validación y test del modelo: Métricas de desempeño del modelo. Se debe reservar el año 2020 como periodo de test.

### 1.4   Comentario sobre la complejidad del modelo y el compromiso sesgo-varianza

 

## 2.       Modelo estocástico de la temperatura y aplicación para valorar una cobertura:

 

Para este apartado se pide diseñar un modelo estocástico de serie temporal para la temperatura. Este modelo se utilizará como modelo generativo de escenarios de temperatura y demanda.

 

### 2.1 Análisis exploratorio de datos

### 2.2 Definición del modelo propuesto

### 2.3 Entrenamiento, validación y test del modelo: Se debe reservar el año 2020 como periodo de test.

 

El resto de apartados consideran el problema de valorar una cobertura financiera para una comercializadora de electricidad. La valoración se hará a fecha 1 de enero de 2020.

 

Supongamos una comercializadora de electricidad que agrega un 10% de toda la demanda de España. Se asume que el consumo agregado de sus clientes en todo momento es proporcional al consumo total del país. La comercializadora compra electricidad en el mercado mayorista y la entrega a sus clientes según los contratos correspondientes. Para el mes de febrero de 2020, la comercializadora tiene en cartera un contrato forward de compra de electricidad a precio fijo por el volumen requerido y entrega la electricidad a sus clientes a un precio fijo. De esta forma, el margen de la comercializadora para febrero de 2020 solo tiene aleatoriedad en el volumen entregado, lo cual determina el riesgo de su posición financiera.

 

Supongamos un derivado cuyo subyacente es el volumen de electricidad entregado por la comercializadora en un mes, V (MWh). El derivado fija un volumen mensual mínimo K (MWh) y paga 1€/MWh por cada MWh no entregado por debajo de K. El pago del derivado para el mes en cuestión (en €) es P_K(V) = 1€/MWh * max(0, K-V).

 

### 2.4 Utilizando los dos modelos desarrollados, estimar una distribución de probabilidad del consumo de electricidad de los clientes de la comercializadora en febrero de 2020.

### 2.5 Proponer una forma de valorar la prima a pagar (a 1 de enero de 2020) por este producto.

 

## 3.       Modelo de consumo de electricidad anual en España a largo plazo basado en fundamentales.

 

En este apartado el objetivo es proponer un modelo para el consumo de electricidad anual en España basado en fundamentales, para hacer una estimación del consumo anual de España a largo plazo. Algunas variables macroeconómicas de interés pueden ser el PIB, la intensidad energética de la actividad económica, la eficiencia energética del país y los nuevos consumos de electricidad: vehículo eléctrico, electrificación de calor, sistemas de almacenamiento y otros nuevos vectores energéticos. Para este apartado se permite y recomienda el uso de cualquier fuente de datos, informe o artículo.

 

### 3.1 Con un modelo simple, hacer una estimación del consumo de electricidad en España en 2030.

### 3.2 Plantear una metodología para afinar la estimación anterior si tuvieras 40 horas.

### 3.3 Plantear una metodología para afinar la estimación anterior si tuvieras 400 horas