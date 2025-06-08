# Análisis de Datos de Ventas AluraStore Latam

Este proyecto realiza un análisis exhaustivo de los datos de ventas de AluraStore en Latinoamérica, combinando información de múltiples fuentes para obtener una visión unificada del rendimiento de la tienda. Se abordan métricas clave como la facturación, las ventas por categoría, la satisfacción del cliente y la logística de envío.

## Tabla de Contenidos

1.  [Acerca del Proyecto](#acerca-del-proyecto)
2.  [Fuentes de Datos](#fuentes-de-datos)
3.  [Análisis Realizados](#análisis-realizados)
    * [Importación y Preparación de Datos](#importación-y-preparación-de-datos)
    * [Análisis de Facturación](#análisis-de-facturación)
    * [Ventas por Categoría](#ventas-por-categoría)
    * [Calificación Promedio de la Tienda](#calificación-promedio-de-la-tienda)
    * [Productos Más y Menos Vendidos](#productos-más-y-menos-vendidos)
    * [Envío Promedio por Tienda](#envío-promedio-por-tienda)
4.  [Cómo Ejecutar el Análisis](#cómo-ejecutar-el-análisis)
5.  [Tecnologías Utilizadas](#tecnologías-utilizadas)
6.  [Resultados Clave](#resultados-clave)
7.  [Contribuciones](#contribuciones)
8.  [Licencia](#licencia)

---

## Acerca del Proyecto

El objetivo de este proyecto es consolidar y analizar los datos de ventas de AluraStore provenientes de diferentes archivos, para extraer información valiosa que pueda ayudar en la toma de decisiones comerciales. Desde la identificación de las categorías de productos más rentables hasta la evaluación del desempeño de los vendedores y los costos de envío, este análisis proporciona una base sólida para entender el negocio.

---

## Fuentes de Datos

Los datos de este proyecto provienen de cuatro archivos CSV alojados en un repositorio de GitHub, representando posiblemente diferentes fragmentos o periodos de ventas:

* `tienda_1.csv`
* `tienda_2.csv`
* `tienda_3.csv`
* `tienda_4.csv`

Cada archivo contiene información detallada de transacciones individuales, incluyendo `Producto`, `Categoría del Producto`, `Precio`, `Costo de envío`, `Fecha de Compra`, `Vendedor`, `Lugar de Compra`, `Calificación`, `Método de pago`, `Cantidad de cuotas`, `lat` y `lon`.

---

## Análisis Realizados

A continuación, se describen los pasos y análisis llevados a cabo en el notebook `AluraStoreLatam.ipynb`.

### Importación y Preparación de Datos

Se importan los cuatro archivos CSV utilizando la librería `pandas` y se concatenan en un único DataFrame llamado `tienda_completa`. Se realiza una inspección inicial del DataFrame combinado para verificar su estructura y tipos de datos.
Posteriormente, la columna `Fecha de Compra` se convierte a un formato `datetime` y se calcula una nueva columna `Total_Venta` sumando `Precio` y `Costo de envío`.

### Análisis de Facturación

* **Facturación Total:** Cálculo de la suma de todos los `Total_Venta` para obtener el ingreso bruto de todas las transacciones.
* **Valor Promedio de Transacción:** Determinación del valor monetario promedio por cada venta.
* **Facturación por Método de Pago:** Identificación del `Método de pago` que generó la mayor facturación total.

### Ventas por Categoría

* **Ventas Totales por Categoría:** Cálculo de la facturación total para cada `Categoría del Producto`.
* **Top 3 Categorías Más Vendidas:** Identificación de las tres categorías de productos que generaron mayores ingresos.

### Calificación Promedio de la Tienda

* **Calificación Promedio General:** Cálculo de la calificación promedio de todas las transacciones.
* **Calificación Promedio por Categoría:** Determinación de la calificación promedio para cada `Categoría del Producto`, permitiendo identificar qué categorías tienen productos mejor valorados.

### Productos Más y Menos Vendidos

* **Top 5 Productos Más Vendidos:** Identificación de los cinco productos individuales que se vendieron en mayor cantidad.
* **Top 5 Productos Menos Vendidos:** Identificación de los cinco productos individuales que se vendieron en menor cantidad.

### Envío Promedio por Tienda

* **Costo de Envío Promedio por Lugar de Compra:** Cálculo del costo promedio de envío asociado a cada `Lugar de Compra`, lo que podría indicar diferencias logísticas o de tarifas por región.

---

## Cómo Ejecutar el Análisis

Para replicar este análisis:

1.  Clona este repositorio en tu máquina local o abre el notebook en Google Colab.
2.  Abre el archivo `AluraStoreLatam.ipynb`.
3.  Ejecuta todas las celdas del notebook en orden. Asegúrate de que todas las librerías necesarias (`pandas`) estén instaladas (si usas Colab, ya vienen preinstaladas).

## Tecnologías Utilizadas

* **Python**
* **Pandas:** Para manipulación y análisis de datos.
* **Google Colab:** Entorno de desarrollo para la ejecución del notebook.

---

## Resultados Clave

Algunos de los hallazgos importantes de este análisis incluyen:

* **Facturación Total:** Se obtuvo el monto total de ingresos generados por todas las ventas.
* **Método de Pago Dominante:** Se identificó cuál método de pago contribuyó más significativamente a la facturación total.
* **Categorías Líderes:** Se destacaron las categorías de productos que impulsan la mayoría de las ventas.
* **Satisfacción del Cliente:** Se calculó la calificación promedio general y por categoría, ofreciendo insights sobre la percepción de los productos.
* **Rendimiento de Productos:** Se listaron los productos más y menos vendidos, lo que puede guiar decisiones de inventario y marketing.
* **Logística de Envío:** Se observaron las diferencias en los costos de envío promedio por ubicación.

*(Puedes añadir aquí los resultados específicos si quieres que el README sea más informativo, por ejemplo: "Total de facturación: $X,XXX,XXX.XX", "Método de pago con mayor facturación: Tarjeta de crédito", etc.)*

---

## Contribuciones

Las contribuciones son bienvenidas. Si tienes sugerencias para mejorar el análisis, agregar visualizaciones o refactorizar el código, no dudes en abrir un *issue* o enviar un *pull request*.

---

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.
