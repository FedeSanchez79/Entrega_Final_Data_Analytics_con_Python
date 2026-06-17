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
- Los datos a nivel de transacción (cada venta individual, ya cruzada con las campañas de marketing) están **embebidos como JSON** dentro del propio archivo.
- Tiene un **panel de filtros estilo Power BI** fijo arriba de la página: categoría de producto, canal de marketing, mes y estado de campaña. Al elegir cualquier combinación, todos los gráficos, las tarjetas de estadística, la tabla de correlación y los insights de texto se recalculan al instante en el navegador (sin recargar la página).
- Los gráficos se generan con **[Plotly.js](https://plotly.com/javascript/)**, y la librería completa está **embebida directamente en el HTML** (no se carga desde un CDN externo). Esto hace que el archivo pese unos 5 MB, pero garantiza que los gráficos siempre rendericen, incluso sin conexión a internet o en redes que bloqueen CDNs externos (algo que pasó al publicar la primera versión en GitHub Pages).
- La tipografía sí se carga desde Google Fonts; si no hay conexión, el navegador usa una tipografía de reemplazo y el resto de la página funciona igual.

### Filtros disponibles
- **Categoría**: Decoración / Electrodomésticos / Electrónica
- **Canal de marketing**: Email / RRSS / TV
- **Mes**: Enero a diciembre
- **Estado de campaña**: dentro o fuera de período de campaña

Los filtros se combinan entre sí (AND). Si una combinación no tiene transacciones, se muestra un aviso en lugar de gráficos vacíos. El botón "Limpiar filtros" vuelve a la vista completa.

## 🚀 Cómo publicarla

Al ser un solo archivo HTML, se puede subir tal cual a:

- **GitHub Pages** → subir el archivo al repo (renombrado a `index.html` si va en la raíz) y activar Pages en la configuración del repositorio.
- **Vercel** → arrastrar la carpeta o el archivo al deploy de Vercel.
- **Google Sites** → insertar el contenido embebido o linkear el archivo alojado.

No requiere build ni instalación de dependencias: abrir el `.html` en cualquier navegador también funciona en local.

## 🎨 Sobre el diseño

La estética toma como referencia un recibo/ticket de venta: fondo crema, tipografía monoespaciada para los números y acentos en mostaza y azul petróleo, en línea con la temática retail del dataset (ventas, productos, campañas).
