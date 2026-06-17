# 📊 Lectura de Ventas — Análisis Retail 2024

Presentación final del TPI de Data Analytics (Comisión 26109), en formato de página web interactiva. Resume los hallazgos del análisis de ventas, EDA, correlación y consolidación con marketing realizado en el notebook.

🔗 **Archivo:** `presentacion_final.html`

---

## 🗂️ ¿Qué contiene?

### 1️⃣ Estadística descriptiva
Tarjetas con media, mediana, moda, desviación estándar y rango intercuartílico de `precio`, `cantidad` y `venta_total_transaccion`.

### 2️⃣ Distribución y forma de los datos (EDA)
Histograma de la venta total por transacción y boxplots comparativos de las tres variables, con la cantidad de outliers detectados.

### 3️⃣ Correlación
Mapa de calor interactivo + tabla con los coeficientes de correlación entre precio, cantidad y venta total.

### 4️⃣ Consolidación ventas-marketing
Comparación de ventas dentro y fuera de período de campaña, por categoría y por canal (Email, RRSS, TV), con el cálculo de retorno aproximado por canal.

### 5️⃣ Tendencia mensual
Evolución de las ventas totales mes a mes durante 2024.

---

## ⚙️ Cómo funciona

- Es un **único archivo HTML autocontenido**: no necesita backend ni conexión a una base de datos.
- Los datos ya calculados (estadísticas, agrupaciones, etc.) están **embebidos como JSON** dentro del propio archivo.
- Los gráficos se generan con **[Plotly.js](https://plotly.com/javascript/)** (cargado desde un CDN), por lo que son interactivos: se puede pasar el mouse sobre los puntos, filtrar series desde la leyenda y hacer zoom.
- La tipografía se carga desde Google Fonts (Fraunces, Space Mono e Inter).


## 🎨 Sobre el diseño

La estética toma como referencia un recibo/ticket de venta: fondo crema, tipografía monoespaciada para los números y acentos en mostaza y azul petróleo, en línea con la temática retail del dataset (ventas, productos, campañas).
