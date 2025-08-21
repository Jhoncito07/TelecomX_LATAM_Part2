# 🔍 Predicción de Cancelación de Clientes (Churn Analysis)

Este proyecto tiene como objetivo identificar los factores que influyen en la cancelación de clientes (churn) y construir modelos de clasificación que permitan anticipar dicha cancelación. Se aplicaron técnicas de preprocesamiento, balanceo de clases, visualización de datos y evaluación de modelos para obtener insights accionables.

---

## 📁 Estructura del Proyecto

- notebook/: Análisis exploratorio, limpieza y modelado.
- datos_tratados.csv: Informe en formato CSV.
- README.md: Documentación del proyecto.

---

## ⚙ Tecnologías Utilizadas

- Python 3.10+
- Pandas, NumPy
- Scikit-learn, XGBoost, imbalanced-learn
- Matplotlib, Seaborn

---

## 🧪 Flujo de Trabajo

1. *Preprocesamiento*
   - Codificación de variables categóricas con LabelEncoder.
   - Conversión binaria de la variable objetivo Churn.
   - Eliminación de columnas redundantes y valores nulos.

2. *Balanceo de Clases*
   - Se aplicó SMOTE para oversampling y RandomUnderSampler para undersampling.
   - Se verificó la distribución antes y después del balanceo.

3. *Modelado*
   - Modelos entrenados: Logistic Regression, Random Forest, KNN, SVM, XGBoost.
   - Se utilizó train_test_split con estratificación para mantener la proporción de clases.

4. *Evaluación*
   - Métricas: F1 Score, Matriz de Confusión, Classification Report.
   - Visualización de importancia de variables por modelo:
     - Coeficientes (Logistic Regression, SVM)
     - Permutation Importance (KNN)
     - Feature Importance (Random Forest, XGBoost)

5. *Visualizaciones Clave*
   - Boxplots: Tenure y ChargesTotal vs Churn
   - Scatterplot: Relación entre Tenure y ChargesTotal coloreado por Churn
   - Heatmap de correlación entre variables numéricas

---

## 📊 Resultados Destacados

| Modelo              | F1 Score (Churn) | Comentario                                               |
|---------------------|------------------|----------------------------------------------------------|
| Random Forest       | ~0.88            | Excelente rendimiento sin necesidad de escalado          |
| XGBoost             | ~0.87            | Precisión alta y manejo eficaz de relaciones no lineales |
| Logistic Regression | ~0.81            | Buen baseline, fácil de interpretar                      |
| SVM (lineal)        | ~0.80            | Similar a regresión, menos interpretable                 |
| KNN                 | ~0.75            | Sensible a ruido y escala                                |

---

## 🎯 Insights Estratégicos

- Clientes con menor antigüedad (Tenure) tienen mayor probabilidad de cancelar.
- Contratos mensuales y facturación baja están asociados con mayor churn.
- Métodos de pago automáticos y servicios adicionales como soporte técnico y seguridad en línea ayudan a retener clientes.

---

## 📌 Recomendaciones

- Incentivar contratos de largo plazo con beneficios exclusivos.
- Ofrecer paquetes de bienvenida a nuevos clientes.
- Promover pagos automáticos con bonificaciones.
- Usar modelos predictivos para segmentar clientes en riesgo y aplicar campañas personalizadas.

---

## 📥 Cómo Ejecutar

Puedes ejecutar este proyecto directamente en Google Colab sin necesidad de instalar nada localmente:

👉 [Abrir en Google Colab](https://colab.research.google.com/)

### Alternativamente, si prefieres ejecutarlo localmente:

```bash
# Clonar el repositorio
git clone https://github.com/Jhoncito07/TelecomX_LATAM_Part2.git

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar el notebook principal
jupyter notebook notebooks/TelecomX_LATAM_Part2.ipynb
