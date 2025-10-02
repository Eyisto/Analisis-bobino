# 🐄 Análisis Integral de la Producción Bovina en Argentina

## 📋 Descripción del Proyecto

Este proyecto presenta un análisis exhaustivo de la rentabilidad de la producción bovina en Argentina, basado en datos oficiales del Ministerio de Agricultura, Ganadería y Pesca de la Nación. El estudio abarca el período comprendido entre junio de 2018 y marzo de 2019, analizando 2,598 registros de 199 departamentos distribuidos en 13 provincias argentinas.

## 🎯 Objetivos

- **Identificar** las provincias más rentables para la producción bovina
- **Analizar** factores clave que impactan la rentabilidad por hectárea
- **Desarrollar** modelos predictivos para optimizar ingresos
- **Detectar** tendencias territoriales y oportunidades de mejora
- **Proporcionar** insights basados en datos para la toma de decisiones en el sector ganadero

## 📊 Métricas Analizadas

| Métrica | Descripción | Unidad |
|---------|-------------|--------|
| 💰 **Ingreso Neto** | Ganancia por hectárea | $/ha |
| 📊 **Eficiencia de Stock** | Productividad del ganado | % |
| 🎯 **Destete** | Tasa de supervivencia | % |
| ⚖️ **Carga Animal** | Densidad ganadera | kg/ha |
| 💸 **Costos Totales** | Gastos directos + indirectos | $/ha |

## 🔧 Metodología

### Procesamiento de Datos
- **Limpieza**: Eliminación de columnas problemáticas y valores nulos
- **Validación**: Verificación de la integridad y consistencia de los datos
- **Agregación**: Cálculo de promedios provinciales representativos

### Corrección Metodológica Importante
Durante el desarrollo del proyecto se identificó y corrigió un error conceptual crítico:
- **❌ Problema inicial**: Se calculaban sumas totales por provincia (ej: $1.4M total)
- **✅ Solución implementada**: Se cambió a promedios por hectárea (ej: $2,363/ha)
- **📈 Resultado**: Análisis estadísticamente correcto y económicamente interpretable

### Visualizaciones Implementadas
1. **Dashboard de Ingresos**: Ingresos promedio por hectárea por provincia (TOP 8)
2. **Dashboard de Costos**: Análisis completo de gastos directos e indirectos
3. **Análisis Comparativo**: Distribución de rentabilidad entre provincias
4. **Matrices de Correlación**: Relación entre múltiples variables productivas
5. **Modelos Predictivos**: Machine Learning con regresión lineal y Random Forest

### Machine Learning Aplicado
- **Modelo Simple**: Regresión lineal univariable (Eficiencia de Stock → Ingresos)
- **Modelo Avanzado**: Regresión lineal múltiple con 5 variables predictoras
- **Modelo de Ensamble**: Random Forest para capturar relaciones no lineales
- **Validación**: División Train/Test (80/20) con métricas R² y MSE
- **Feature Importance**: Identificación de variables más influyentes

## 📈 Principales Hallazgos

### 💰 Rentabilidad Provincial
- **Promedio Nacional**: $1,586/ha
- **Rango de Variación**: $205 - $5,980 por hectárea
- **Provincias Líderes**: [Se actualiza con cada ejecución del análisis]

### 💸 Análisis de Costos
- **Gastos Directos**: Identificación de provincias con mayores costos operativos
- **Costos Indirectos**: Análisis de gastos estructurales por región
- **Ratio D/I**: Eficiencia en la estructura de costos (Directos/Indirectos)
- **TOP 10 Comparativo**: Provincias más rentables vs sus estructuras de costos

### 🤖 Modelos Predictivos
- **Mejor Modelo**: Random Forest supera a Regresión Lineal
- **R² Score**: Entre 0.85-0.95 (excelente capacidad predictiva)
- **Variables Clave**: Eficiencia de stock, producción kg/ha, destete %
- **Aplicación Práctica**: Predicción de ingresos basada en indicadores operativos

### 🌎 Distribución Territorial
- **Total de Provincias**: 13 analizadas
- **Departamentos**: 199 unidades territoriales
- **Representatividad**: Cobertura significativa del territorio nacional
- **Análisis Provincial**: Error de predicción por provincia (validación regional)

## 🛠️ Tecnologías Utilizadas

### Lenguajes y Librerías
- **Python 3.x**: Lenguaje principal de análisis
- **Pandas**: Manipulación y análisis de datos
- **NumPy**: Operaciones numéricas avanzadas
- **Matplotlib/Seaborn**: Visualización de datos
- **Scikit-learn**: Machine Learning y modelado predictivo

### Herramientas de Desarrollo
- **Jupyter Notebook**: Ambiente de desarrollo interactivo
- **Git**: Control de versiones
- **VS Code**: Editor de código

## 📁 Estructura del Proyecto

```
Analisis-bobino/
├── bobino.ipynb                 # Notebook principal con análisis completo
├── produccion-de-carne-bovina.csv  # Dataset original
├── README.md                    # Documentación del proyecto
```

## 📖 Guía de Uso

### Prerrequisitos
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Ejecución
1. Clona el repositorio:
```bash
git clone https://github.com/Eyisto/Analisis-bobino.git
cd Analisis-bobino
```

2. Abre el notebook:
```bash
jupyter notebook bobino.ipynb
```

3. Ejecuta las celdas secuencialmente para reproducir el análisis completo.

## 🎓 Análisis Realizados

### 1. 📂 Exploración y Limpieza de Datos
- Carga y validación del dataset (2,598 registros)
- Análisis de valores nulos y datos faltantes
- Limpieza de columnas problemáticas
- Verificación de integridad de datos

### 2. 💰 Análisis de Rentabilidad
- **Dashboard de Ingresos**: Visualización TOP 8 provincias más rentables
- **Promedios por Hectárea**: Cálculo estadísticamente correcto
- **Distribución Geográfica**: Scatter plots de ingresos vs departamentos
- **Estadísticas Nacionales**: Promedio, mediana, y rangos de variación

### 3. 💸 Análisis de Estructura de Costos
- **Gastos Directos**: Ranking TOP 15 provincias
- **Costos Indirectos**: Análisis comparativo de gastos estructurales
- **Comparación D/I**: Costos directos vs indirectos en TOP 10
- **Ratio de Eficiencia**: Identificación de provincias con mejor estructura de costos

### 4. 🎯 Modelado Predictivo Inicial
- **Regresión Lineal Simple**: Eficiencia de Stock → Ingresos Netos
- **Visualizaciones**:
  - Datos reales vs predicciones
  - Distribución de residuos
  - Matriz de correlación ampliada (5 variables)
  - Scatter plot temporal por año
- **Métricas**: MSE, R², coeficientes de regresión

### 5. 🤖 Machine Learning Avanzado
- **Múltiples Modelos**:
  - Regresión Lineal Múltiple (5 variables con escalado)
  - Random Forest (100 árboles, max_depth=10)
- **Variables Predictoras**:
  - Eficiencia de stock (%)
  - Producción (kg/ha)
  - Destete (%)
  - Carga animal (kg/ha)
  - Gastos directos ($/ha)
- **Análisis Avanzados**:
  - Feature importance (importancia de variables)
  - Comparación de modelos (R² y MSE)
  - Validación por provincia
  - Distribución de predicciones vs valores reales

### 6. 📊 Visualizaciones Avanzadas
- **9 Paneles Integrados**: Dashboard completo de ML
- **Análisis de Residuos**: Distribución y patrones de error
- **Error Provincial**: MSE por provincia (TOP 10)
- **Correlaciones**: Heatmaps y scatter plots multivariables

## 📊 Fuente de Datos

**Dataset Original**: Análisis de ventas del sector bovino en Argentina
- **Período Específico**: 11 de junio de 2018 al 18 de marzo de 2019
- **Fuente**: Ministerio de Agricultura, Ganadería y Pesca de la Nación Argentina
- **Portal**: datos.magyp.gob.ar
- **URL**: https://datos.magyp.gob.ar/dataset/produccion-carne-bovina/archivo/cabb1226-e84b-4b0b-a1c4-6a98f854760e
- **Encoding**: Latin-1
- **Formato**: CSV
- **Registros**: 2,598 observaciones
- **Descripción**: Datos oficiales sobre producción, costos e ingresos del sector bovino argentino por departamento y provincia

## 🔄 Historial de Versiones

### v3.0 - Machine Learning y Análisis Avanzado (Octubre 2025)
- 🤖 **Machine Learning**: Implementación de Random Forest y Regresión Múltiple
- 💸 **Análisis de Costos**: Dashboard completo de gastos directos e indirectos
- 📊 **Feature Importance**: Identificación de variables más influyentes
- 🎯 **Modelos Predictivos**: Validación con Train/Test split (80/20)
- 📈 **9 Visualizaciones**: Dashboard integrado de análisis predictivo
- ✅ **Validación Provincial**: Error de predicción por región
- 🔧 **Optimización**: Mejores prácticas de ML aplicadas al sector bovino

### v2.0 - Corrección Metodológica (Octubre 2025)
- ✅ **Corrección crítica**: Cambio de sumas totales a promedios por hectárea
- ✅ **Nueva visualización**: Dashboard corregido con métricas representativas
- ✅ **Validación agregada**: Análisis detallado de la metodología de cálculo
- ✅ **Mejoras en interpretación**: Estadísticas económicamente significativas

### v1.0 - Versión Inicial
- 📊 Exploración inicial de datos
- 📈 Primeras visualizaciones
- 🧹 Limpieza básica del dataset

## 🎯 Casos de Uso

Este análisis es útil para:

1. **Productores Ganaderos**: Identificar las mejores prácticas y provincias más rentables
2. **Inversores**: Evaluar oportunidades de inversión en el sector bovino
3. **Investigadores**: Base para estudios sobre ganadería argentina
4. **Agrónomos**: Optimización de parámetros productivos
5. **Planificadores**: Políticas públicas basadas en datos reales

## 💡 Próximas Mejoras

- [ ] Análisis temporal detallado (series de tiempo)
- [ ] Modelos de Deep Learning (redes neuronales)
- [ ] Análisis de clustering para segmentación de provincias
- [ ] Dashboard interactivo con Plotly/Dash
- [ ] API REST para predicciones en tiempo real
- [ ] Integración con datos climáticos y de mercado

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Siéntete libre de hacer fork del proyecto y enviar pull requests.

### Áreas de Contribución
- 🐛 Reportar bugs o problemas
- 💡 Sugerir nuevas funcionalidades
- 📊 Agregar nuevas visualizaciones
- 🤖 Implementar nuevos modelos de ML
- 📝 Mejorar la documentación

## 📝 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 👨‍💻 Autor

**Eyisto Aguilar Trejo**
- GitHub: [@Eyisto](https://github.com/Eyisto)

## 📞 Contacto

Si tienes preguntas sobre este análisis o sugerencias de mejora, no dudes en abrir un issue en este repositorio.

---
*Análisis desarrollado con fines educativos y de investigación basado en datos públicos del gobierno argentino.*
