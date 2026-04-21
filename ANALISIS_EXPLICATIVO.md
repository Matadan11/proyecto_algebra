# Análisis del Embudo de Conversión de Comercio Electrónico

## 📋 Descripción General

Este proyecto realiza un análisis exploratorio de datos (EDA) sobre un **embudo de conversión de comercio electrónico**. El objetivo principal es identificar puntos clave de abandono, comprender el comportamiento del usuario a lo largo del funnel de compra y proporcionar insights accionables para optimizar la experiencia del usuario y las estrategias de marketing.

---

## 📊 Estructura de los Datos

El dataset `ecommerce_funnel.csv` contiene información a nivel de sesión de usuario con las siguientes características:

### Columnas Principales

| Columna | Descripción |
|---------|-------------|
| `session_id` | Identificador único de la sesión |
| `user_id` | Identificador del usuario |
| `session_date` | Fecha de la sesión |
| `source` | Origen del tráfico (organic, social, paid_ads, direct) |
| `device` | Tipo de dispositivo (desktop, mobile) |
| `campaign_type` | Tipo de campaña (retargeting, influencer, awareness) |
| `session_time` | Tiempo de sesión en segundos |
| `pages_viewed` | Número de páginas vistas |
| `viewed_product` | ¿Vio el producto? (0/1) |
| `added_to_cart` | ¿Agregó al carrito? (0/1) |
| `purchased` | ¿Completó la compra? (0/1) |
| `abandoned` | ¿Abandonó la sesión? (0/1) |
| `discount_seen` | ¿Vio descuento? (0/1) |
| `returning_user` | ¿Es usuario recurrente? (0/1) |
| `weekday` | Día de la semana (0-6) |

---

## 🎯 Etapas del Embudo de Conversión

El análisis sigue las etapas tradicionales del e-commerce funnel:

1. **Visitas (V)**: Todas las sesiones que llegan al sitio
2. **Visualización de Producto (P)**: Usuarios que ven detalles del producto
3. **Adición al Carrito (C)**: Usuarios que agregan artículos al carrito
4. **Compra (B)**: Usuarios que completan la transacción
5. **Abandono (A)**: Sesiones sin compra completada

### Tasas de Conversión Clave

- **Tasa V→P**: Porcentaje de visitantes que ven productos
- **Tasa P→C**: Porcentaje de quienes ven producto que lo agregan al carrito
- **Tasa C→B**: Porcentaje de quienes abandonan el carrito que lo convierten en compra
- **Tasa de Conversión General (V→B)**: Porcentaje total de visitantes que compran

---

## 🔍 Análisis Realizado

### 1. **Carga y Exploración de Datos**
   - Carga del dataset con pandas
   - Visualización de primeras filas
   - Verificación de información básica (`df.info()`)
   - Estadísticas descriptivas (`df.describe()`)
   - Detección de valores nulos

### 2. **Conteo de Eventos**
   - Total de visitas, visualizaciones, carritos y compras
   - Cuantificación de abandonos
   - Cálculo de proporciones en cada etapa

### 3. **Análisis de Tasas de Conversión**
   - Conversión entre etapas del funnel
   - Identificación de cuellos de botella
   - Comparación de rendimiento por segmento

### 4. **Segmentación de Usuarios** *(esperado)*
   - Por fuente de tráfico (organic, social, paid_ads, direct)
   - Por dispositivo (desktop vs mobile)
   - Por tipo de campaña
   - Por tipo de usuario (nuevo vs recurrente)

---

## 💡 Insights Esperados

- **Puntos de abandono críticos**: ¿Dónde pierden más usuarios?
- **Influencia del dispositivo**: ¿Mobile convierte menos que desktop?
- **Impacto de fuente de tráfico**: ¿Qué canal trae usuarios más calificados?
- **Efecto del descuento**: ¿Los descuentos impulsan compras?
- **Comportamiento de usuarios recurrentes**: ¿Convierten más?
- **Patrones temporales**: ¿Qué días/horas son mejores?

---

## 🛠️ Tecnologías Utilizadas

- **Python 3.x**
- **Pandas**: Manipulación y análisis de datos
- **NumPy**: Operaciones numéricas
- **Jupyter Notebook**: Documentación y ejecución interactiva
- **Visualización**: (matplotlib, seaborn u otros según sea necesario)

---

## 📈 Archivo Principal

- `Projecto_Algebra.ipynb`: Notebook Jupyter con todo el análisis paso a paso
- `ecommerce_funnel.csv`: Dataset de entrada
- `proyecto_Algebra.html`: Versión exportada en HTML

---

## 🎓 Conclusión

Este análisis proporciona una base sólida para entender el comportamiento de compra en e-commerce y permite identificar oportunidades de optimización en cada etapa del funnel, contribuyendo a mejorar la tasa de conversión y el ROI de inversiones en marketing.
