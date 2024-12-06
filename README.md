# **Análisis de Ofertas Relámpago - Data Science**

---

## **1. Resolución del Reto**
Este análisis tuvo como objetivo principal responder al reto planteado sobre las ofertas relámpago. Nos enfocamos en entender los patrones de comportamiento en las ventas, identificar tendencias clave y generar insights que puedan servir como base para decisiones estratégicas. 

Se realizó un análisis detallado de los datos, acompañado de visualizaciones dinámicas e interactivas que permitieron explorar diferentes aspectos del rendimiento de las ofertas.

---

## **2. Proceso de Análisis**

### **2.1 Comprensión de los Datos**

Los datos utilizados incluyen información detallada sobre:
- **Duración de las ofertas:** Inicio y fin de cada campaña.
- **Inventario involucrado y remanente:** Stock disponible antes y después de cada oferta.
- **Cantidad vendida:** Número de unidades y valor monetario vendido durante la oferta.
- **Información temporal:** Horario y día de la semana en que se lanzaron las campañas.

**Preparación de los Datos:**
1. **Limpieza de columnas irrelevantes o inconsistentes:**
   - **Columnas eliminadas:**
     - `offer_type`: Todos sus valores eran iguales.
     - `origin`: Presentaba un alto porcentaje de valores faltantes.
2. **Creación de métricas clave:**
   - **Porcentaje vendido:** Relación entre las unidades vendidas y el inventario disponible.
   - **Duración en minutos:** Tiempo total que duró cada oferta.
   - **Variables temporales:** Hora y día de la semana en que se inició cada campaña.

---

### **2.2 Visualizaciones Realizadas**

#### **Análisis de Proporciones**
**Pregunta clave:** ¿Cómo se distribuyen las ventas entre las categorías?

Se utilizó un gráfico interactivo de torta que permite visualizar las proporciones de ventas según distintas métricas:
- **Métricas disponibles:**
  - Ventas totales (`sold_amount`).
  - Cantidades vendidas (`sold_quantity`).
  - Promedio del porcentaje vendido (`sold_percentage_avg`).

**Hallazgos:**
- La categoría con mayor proporción de ventas fue **Beauty and Health**, representando el **43.5%** del total.
- Dentro de esta categoría, los productos **farmacéuticos** dominaron, con un **80%** de las ventas de la categoría.
- En esta misma categoría, el **69%** de las compras se realizaron con envío pago.
- Cambiar la métrica permitió identificar categorías con alto volumen de ventas pero bajo porcentaje de inventario vendido, lo que podría indicar potencial de mejora.

> _ _
![](001.jpeg)

---

#### **Relación entre Inventario y Ventas**
**Pregunta clave:** ¿Existe una relación entre el inventario disponible y el éxito de las ofertas?

Un gráfico de dispersión permitió explorar cómo se relacionan el inventario disponible y las ventas logradas. Los hallazgos incluyen:
- Las ofertas con una duración menor a **500 minutos** no generaron ventas significativas.
- Se detectaron datos atípicos en los que las ventas superaron significativamente al inventario disponible. Estos casos deben revisarse por posibles errores en la calidad de los datos.

> _ _
![](002.jpeg)
![](003.jpeg)

---


#### **Duración de la Oferta y Ventas**
**Pregunta clave:** ¿Influye la duración de la oferta en las ventas logradas?

Se analizó la relación entre la duración de las ofertas (en minutos) y el porcentaje de inventario vendido:
- Las ofertas más largas no siempre garantizan mejores resultados.
- Las campañas más efectivas fueron aquellas más cortas pero lanzadas en horarios estratégicos.

> _ _
![](004.jpeg)

---

#### **Inventario Restante por Categoría**
**Pregunta clave:** ¿Qué categorías tienden a quedarse con más inventario no vendido?

Un gráfico de barras permitió visualizar las categorías con mayor promedio de inventario remanente después de las ofertas. Estos resultados pueden ayudar a identificar áreas de mejora en estrategias de descuentos o manejo de inventario.

**Hallazgos:**
- La categoría con mayor inventario remanente fue **Beauty and Health**, a pesar de ser la categoría con mayores ventas tanto en valor monetario como en cantidad de unidades.

> _ _
![](005.jpeg)

---

#### **Patrones Temporales**
**Pregunta clave:** ¿Cuáles son los horarios y días más efectivos para lanzar ofertas?

**Horarios:**
- En general, las horas de mayor venta son las **13:00**, **12:00** y **19:00**.
- Sin embargo, esto varía por categoría:
  - En **Beauty and Health**, los horarios más efectivos son las **12:00**, **13:00** y **11:00**.

**Días de la semana:**
- Los días con mayores ventas son los **martes** y **miércoles**.
- En el caso de los productos farmacéuticos, los días más efectivos son los **martes** y **lunes**.

> _ _
![](006.jpeg)

---

## **3. Conclusiones y Recomendaciones**

### **Conclusiones**
1. **Beauty and Health** es la categoría más relevante:
   - Representa el mayor porcentaje de ventas (43.5%).
   - Tiene un alto porcentaje de ventas de productos farmacéuticos (80% de la categoría).
   - Sin embargo, es también la categoría con más inventario remanente, lo que podría requerir ajustes en la estrategia.

2. **Horarios y días clave:**
   - Los horarios de **13:00**, **12:00** y **19:00** son los más efectivos.
   - Los días de mayores ventas son los **martes** y **miércoles**, aunque las preferencias pueden variar según la categoría.

3. **Duración de las ofertas:**
   - Las campañas de menos de **500 minutos** no generaron ventas significativas.
   - Las ofertas más largas no siempre son efectivas. En su lugar, es preferible priorizar horarios y días estratégicos.

4. **Calidad de los datos:**
   - Se detectaron datos atípicos en los que las ventas superaron al inventario disponible. Es importante revisarlos para garantizar la calidad del análisis.

---

### **Recomendaciones**
1. **Priorizar campañas en categorías clave:**
   - Focalizar esfuerzos en **Beauty and Health**, optimizando la gestión de inventario para reducir remanentes.

2. **Optimizar lanzamientos:**
   - Diseñar campañas específicas para los horarios y días clave según categoría, como farmacéuticos los lunes y martes.

3. **Revisión de datos:**
   - Analizar y corregir los datos atípicos que afectan las métricas de ventas e inventarios.

4. **Ajustar duración de las ofertas:**
   - Reducir campañas largas y concentrarse en períodos estratégicos de alto impacto.

---
