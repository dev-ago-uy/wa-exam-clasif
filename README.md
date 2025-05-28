Resumen Ejecutivo - Modelo de Detección de Fraudes

Se desarrolló un modelo de machine learning para identificar solicitudes de financiamiento fraudulentas a partir del análisis de canastas de productos. La base de datos mostró un 14.15% de fraudes, lo cual representaba un desbalance relevante, ya que la clase minoritaria (fraude) estaba presente en solo el 14.15% de los casos. 

Esto justifica el uso de técnicas específicas para evitar que el modelo se sesgue hacia la clase mayoritaria.

Como modelo base se eligió regresión logística por su simplicidad, interpretabilidad y velocidad. Se aplicó regularización L2 para evitar sobreajuste y se usó `class_weight='balanced'` para corregir el desbalance de clases. Las variables categóricas fueron transformadas mediante One-Hot Encoding.
La evaluación del modelo se realizó con métricas como F1-score, PR-AUC y ROC-AUC, priorizando la detección de fraudes sin sacrificar precisión. Se demostró que ajustar el umbral de decisión (por ejemplo, bajarlo a 0.3) permite aumentar la sensibilidad del modelo, detectando más fraudes con un costo aceptable de falsos positivos.
El análisis de coeficientes (betas) permitió interpretar la influencia de cada variable en la predicción. Se recomienda como mejora futura probar modelos como Random Forest para comparar rendimiento, y validar la estabilidad del pipeline.

