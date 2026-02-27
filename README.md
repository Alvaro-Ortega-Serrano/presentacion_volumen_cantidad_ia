# presentacion_volumen_cantidad_ia
Uso de Azure OpenAI con modelos LLM que actuan como juez para evaluar el volumen/cantidad de 40.000 presentaciones farmacéuticas generadas por una IA, comparándolas con valores esperados del Ministerio de Sanidad.
El LLM actúa como juez, no para determinar la veracidad de los datos, sino para evaluar la concordancia entre la predicción de la IA y la referencia, gestionando diferencias de formato, unidades y tolerancias, y generando automáticamente una justificación razonada mediante prompt junto con una puntuación asociada.
La solución se ejecuta sobre SAS Viya, permitiendo escalabilidad para grandes volúmenes de datos.

El sistema genera automáticamente:
Resultados normalizados en tres formatos:
  cantidad_unidad (ej. 30 mg)
  cantidad (ej. 30)
  unidad (ej. mg)
Justificación detallada de la evaluación frente al valor esperado
Puntuación multicriterio del 1 al 10 basada en corrección factual
Estado final: correcto o incorrecto
