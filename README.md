# Modelización de Datos Categóricos: Miocardiopatía Arritmogénica

**Autora:** Carla Martín Pérez

## Resumen
Análisis de datos reales de pacientes con miocardiopatía arritmogénica con afectación del ventrículo izquierdo (MCAVI) y grupo control sano, aplicando modelos log-lineales y logit en R.  
El objetivo fue estudiar la asociación entre la presencia de extrasístoles ventriculares con morfología de bloqueo de rama derecha (EV-BRD) y la enfermedad, considerando factores de riesgo como edad, sexo y hábito de fumar.  
Los resultados muestran que EV-BRD está fuertemente asociada a MCAVI, mientras que sexo, fumar y edad no presentan asociación estadísticamente significativa.  
Se generó un informe en PDF, un RMarkdown con el análisis completo y una presentación tipo PowerPoint.

## Objetivo
Estudiar la dependencia y asociación entre variables categóricas relacionadas con la enfermedad MCAVI, evaluando si la presencia de EV-BRD se asocia con la enfermedad y otros factores de riesgo.

## Datos
- Datos de pacientes reales bajo seguimiento entre febrero y junio de 2023  
- Total: 63 pacientes con MCAVI y 20 pacientes sanos  
- Variables:
  1. **Grupos:** 0 = MCAVI / 1 = Sano  
  2. **Fumar:** 0 = No / 1 = Sí  
  3. **EV-BRD:** 0 = No / 1 = Sí  
  4. **Sexo:** 0 = Mujer / 1 = Hombre  
  5. **Edad:** estratificada en 7 categorías (0-14, 15-20, 21-30, 31-40, 41-50, 51-60, >61)

> Nota: Los datos no se comparten por motivos de confidencialidad médica.

## Metodología
- Software: **R**  
- Modelos utilizados: **Log-lineal** y **Logit**  
- Procedimiento:
  - Ajuste del modelo log-lineal usando **método backward** para seleccionar el modelo más parsimonioso  
  - Ajuste del modelo logit para interpretar asociaciones entre variables  
  - Resultados presentados en tablas y gráficos, con interpretación estadística en términos de cocientes de ventajas (odds)

## Resultados
- El modelo log-lineal seleccionado (GB, FB, BS, FBS, GFES) muestra buen ajuste a los datos (p-valor > 0.05).  
- Presencia de EV-BRD: pacientes con MCAVI tienen **aprox. 12 veces mayor probabilidad** de presentar EV-BRD que individuos sanos.  
- Sexo, hábito de fumar y edad: no presentan asociación significativa con EV-BRD.  
- Limitaciones: tamaño reducido de la muestra, algunas celdas con pocas observaciones, posibles errores tipo II.

## Conclusiones
- EV-BRD está fuertemente asociada a MCAVI.  
- Otros factores (sexo, fumar, edad) no muestran evidencia significativa de asociación.  
- Los modelos log-lineales y logit permiten interpretar relaciones entre variables categóricas en estudios clínicos.

## Contenido del repositorio
- `notebooks/` → RMarkdown con el análisis completo  
- `pdf/` → Informe final en PDF  
- `presentation/` → Presentación tipo PowerPoint  
