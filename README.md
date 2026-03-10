# **📊 Predicción de Cancelación de Clientes (Churn Prediction)**

Este repositorio contiene un pipeline completo de Ciencia de Datos diseñado para identificar a los clientes con alta probabilidad de cancelar sus servicios de la Empresa Telecom X. El proyecto aborda el problema del Churn mediante modelos de clasificación supervisada, permitiendo a la empresa tomar decisiones estratégicas basadas en datos.

## **🎯 Objetivo del Proyecto**
* Desarrollar modelos predictivos robustos capaces de prever la fuga de clientes antisipándoce a la cancelación mediante un análisis multivariado de factores como el tiempo de contrato, cargos mensuales y el uso de servicios adicionales.

## **🛠️ Flujo de Desarrollo**
<ol>
  <li>Preprocesamiento y Limpieza
    <ul>
      <li>Eliminación de Irrelevancias: Remoción de identificadores únicos (customerID) que no aportan valor predictivo.</li>
      <li>Encoding: Transformación de variables categóricas mediante One-Hot Encoding.</li>
      <li>Tratamiento de Desbalanceo: Aplicación de la técnica SMOTE (Synthetic Minority Over-sampling Technique) para equilibrar la clase minoritaria (Churn) y evitar sesgos en el entrenamiento.</li>
      <li>Estandarización: Uso de StandardScaler para normalizar las magnitudes de variables continuas, asegurando la convergencia de modelos basados en distancia y optimización.</li>
    </ul>
  </li>
  <li>Análisis Exploratorio de Datos (EDA)
    <ul>
      <li>Identificación del Churn: Verificación de la proporción inicial (73.5% Retención vs 26.5% Fuga).</li>
      <li>Análisis de Correlación: Generación de matrices de Pearson para identificar relaciones lineales entre el gasto, la antigüedad y la cancelación.</li>
      <li>Análisis Dirigido: Uso de Boxplots para validar que la antigüedad (tenure) y el gasto total (TotalCharges) son factores críticos de permanencia.</li>
    </ul>
  </li>
</ol>

## **🤖 Modelos Evaluados**
Se contrastaron dos arquitecturas principales para medir el balance entre interpretabilidad y complejidad:
<table>
  <tr>
    <th>Métrica</th>
    <th>Regresión Logística (Elegida)</th>
    <th>Random Forest</th>
  </tr>
  <tr>
    <td>Recall (Clase 1)</td>
    <td>76%</td>
    <td>61%</td>
  </tr>
  <tr>
    <td>Precisión (Clase 1)</td>
    <td>54%</td>
    <td>55%</td>
  </tr>
  <tr>
    <td>F1-Score</td>
    <td>0.63</td>
    <td>0.58</td>
  </tr>
  <tr>
    <td>Sensibilidad</td>
    <td>Alta (Paranoico)</td>
    <td>Baja (Conservador)</td>
  </tr>
</table>

## **🧠 Hallazgos Clave (Feature Importance)**
El análisis del "Cerebro del Modelo" reveló los siguientes factores determinantes:
<ol>
  <li>La variable personalizada Cant_Servicios demostró que la acumulación excesiva de servicios adicionales eleva el riesgo de cancelación debido al incremento en los cargos mensuales.</li>
  <li>Los contratos a largo plazo (2 años) y la antigüedad del cliente son los protectores más fuertes contra la fuga.</li>
  <li>La presencia de Soporte Técnico y Seguridad Online reduce significativamente la probabilidad de abandono.</li>
</ol>

## **📈 Conclusiones Estratégicas**
<ul>
  <li>Migración de Contratos: Incentivar el paso de contratos mensuales a anuales para estabilizar la cartera.</li>
  <li>Optimización de Paquetes: Evitar la saturación de servicios adicionales innecesarios que disparan la percepción de costo elevado.</li>
  <li>Retención Proactiva: Implementar un sistema de alertas tempranas utilizando el score de riesgo generado por la Regresión Logística.</li>
</ul>

## **🚀 Requisitos e Instalación**
Para replicar este entorno de análisis, asegúrate de tener instaladas las siguientes librerías:
<pre>pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn</pre>

