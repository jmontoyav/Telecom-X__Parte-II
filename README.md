# **📊 Predicción de Cancelación de Clientes (Churn Prediction)**

Este repositorio contiene un pipeline completo de Ciencia de Datos diseñado para identificar a los clientes con alta probabilidad de cancelar sus servicios de la Empresa Telecom X. El proyecto aborda el problema del Churn mediante modelos de clasificación supervisada, permitiendo a la empresa tomar decisiones estratégicas basadas en datos.

## **🎯 Objetivo del Proyecto**
* Desarrollar modelos predictivos robustos capaces de prever la fuga de clientes antisipándoce a la cancelación mediante un análisis multivariado de factores como el tiempo de contrato, cargos mensuales y el uso de servicios adicionales.

## **🛠️ Flujo de Desarrollo**
<ol>
  <li> Preprocesamiento y Limpieza
    <ul>
      <li>Eliminación de Irrelevancias: Remoción de identificadores únicos (customerID) que no aportan valor predictivo.</li>
      <li>Encoding: Transformación de variables categóricas mediante One-Hot Encoding.</li>
      <li>Tratamiento de Desbalanceo: Aplicación de la técnica SMOTE (Synthetic Minority Over-sampling Technique) para equilibrar la clase minoritaria (Churn) y evitar sesgos en el entrenamiento.</li>
      <li>Estandarización: Uso de StandardScaler para normalizar las magnitudes de variables continuas, asegurando la convergencia de modelos basados en distancia y optimización.</li>
    </ul>
  </li>
</ol>





