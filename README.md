# Online-Retail-Analysis
> **Autor:** Francisco Lombroni
> **Contacto:** linkedin.com/in/francisco-lombroni-a8133a21b

### 🥇 1. Resumen del Proyecto

Este proyecto es un análisis de portafolio enfocado en el **Análisis de Comportamiento del Cliente (Customer Behavior Analysis)** de un *dataset* de ventas de *Online Retail* del Reino Unido (2010-2011).

El objetivo principal fue aplicar la metodología de segmentación **RFM (Recencia, Frecuencia y Valor Monetario)** y cruzarla con el factor geográfico para obtener **estrategias de negocio accionables** que maximicen la rentabilidad.

---

### 🔑 2. Hallazgos Clave y Conclusiones de Negocio

El análisis segmentado reveló oportunidades de crecimiento de alto valor, confirmando el principio de Pareto en la base de clientes.

#### Base de Clientes

* **Identificación de la Élite:** Los clientes clasificados como **"Campeones"** y **"Clientes Fieles"** representan solo el 33% de la base de clientes, pero son responsables de generar el 77% de los ingresos totales. 

#### Estrategia Geográfica (UK vs. Exterior)

* **Alto Gasto Exterior:** El cliente promedio del mercado **Exterior** presenta un **Gasto (M) dos veces mayor** que el cliente del Reino Unido.
* **Concentración de Campeones:** El mercado Exterior tiene una **mayor proporción de clientes de élite** ("Campeones") que el Reino Unido.

---

### 💡 3. Recomendaciones Estratégicas

1.  **Priorizar Inversión Internacional:** La inversión debe enfocarse en el segmento **Exterior**. El alto valor de estos clientes justifica una estrategia dirigida a **aumentar su Frecuencia (F)**, por ejemplo, mediante campañas de reactivación y lealtad personalizadas.
2.  **Retención de Alto Valor:** Crear un programa de lealtad exclusivo para el 33% de clientes de élite para asegurar la retención de la principal fuente de ingresos.
3.  **Segmentación de Riesgo:** Utilizar la clasificación **"En Riesgo"** para asignar recursos de reactivación de forma eficiente, enfocándose solo en aquellos con mayor potencial de retorno y minimizando la inversión en el segmento **"Durmientes"** (clientes de bajo valor o esporadicos).

---

### 🛠️ 4. Metodología de Análisis

El proyecto se dividió en tres fases interconectadas:

#### A. Limpieza de Datos
* Eliminación de transacciones canceladas, valores nulos (`CustomerID`) y valores atípicos (cantidades/precios negativos o cero).
* Ingeniería de Características: Creación de `TotalPrice` y variables de tiempo (`InvoiceDate` convertida a *datetime* y mantenida para el RFM).

#### B. Segmentación RFM
* **Cálculo:** Se calcularon **Recencia** (usando el 10/Dic/2011 como fecha de referencia), **Frecuencia** y **Gasto** por `CustomerID`.
* **Scoring y Nivel:** Se asignaron puntuaciones (1-5) y se definieron **6 Macro-Segmentos** estratégicos: Campeones, Fieles, Nuevos Clientes, Prometedores, En Riesgo, Durmientes.

#### C. Cruce Geográfico
* Se unió la columna `Country` a la tabla RFM.

---

### 💻 5. Tecnologías y Librerías

| Categoría | Herramienta/Librería | Propósito |
| :--- | :--- | :--- |
| **Lenguaje** | Python | Base del proyecto. |
| **Manipulación** | `pandas`, `numpy` | Limpieza, Ingeniería de Características y Cálculos RFM. |
| **Visualización** | `matplotlib`, `seaborn` | Gráficos de tendencias, estacionalidad y distribución geográfica. |
| **Entorno** | Google Colab | Ejecución y *prototyping*. |

---
