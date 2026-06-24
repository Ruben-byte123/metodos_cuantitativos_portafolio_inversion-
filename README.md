# metodos_cuantitativos_portafolio_inversion-

Este proyecto implementa un sistema de optimización de portafolios utilizando programación cuadrática con CVXPY. El sistema permite descargar datos financieros, calcular métricas de riesgo y retorno, y construir la frontera eficiente para un conjunto de activos.

## Características principales

- **Descarga de datos**: Obtención automática de precios ajustados de Yahoo Finance
- **Cálculo de métricas**: Rendimientos logarítmicos, medias anuales y matriz de covarianza
- **Optimización de portafolios**: 
  - Portafolio de mínima varianza
  - Frontera eficiente usando CVXPY
  - Portafolio de máximo ratio Sharpe
- **Visualización**: Gráfica de la frontera eficiente con puntos destacados
- **Benchmarking**: Comparación contra el índice IPC México

## Estructura del proyecto

### Funciones principales

1. **`download_adj_close()`**: Descarga datos históricos de precios ajustados
2. **`compute_log_returns()`**: Calcula rendimientos logarítmicos y métricas anualizadas
3. **`min_variance_weights()`**: Calcula pesos del portafolio de mínima varianza
4. **`portfolio_metrics()`**: Calcula retorno, volatilidad y ratio Sharpe
5. **`show_results()`**: Optimiza y visualiza la frontera eficiente

### Activos incluidos

El proyecto analiza un portafolio diversificado con los siguientes activos mexicanos:
- GAPB, GMEXICOB, KOFUBL, ALSEA, OMAB
- CHDRAUIB, FNOVA17, BBAJIOO, GFINBURO

## Resultados destacados

### Portafolio óptimo
- **Retorno esperado**: 19.98% anual
- **Volatilidad**: 11.38% anual  
- **Ratio Sharpe**: 1.10

### Portafolio de máximo Sharpe
- **Retorno**: 24.45% anual
- **Riesgo**: 13.20% anual
- **Ratio Sharpe**: 1.28

### Comparativa vs Benchmark (IPC México)
- **Volatilidad IPC**: 16.02%
- **Reducción de volatilidad**: 28.97% vs el portafolio optimizado

## Requisitos

```bash
pip install yfinance numpy pandas cvxpy matplotlib
```

## Uso

1. Ejecutar las celdas en orden para descargar datos
2. Calcular métricas y optimizar portafolios
3. Visualizar la frontera eficiente
4. Comparar resultados contra benchmark

## Metodología

- **Periodo de análisis**: Mayo 2020 - Mayo 2025
- **Tasa libre de riesgo**: 7.51%
- **Optimización**: Restricción de no ventas en corto
- **Método**: Programación cuadrática con CVXPY

## Archivos generados

- Datos descargados en directorio `stock_data/`
- Gráfica de frontera eficiente
- Tabla completa de resultados de optimización

Este proyecto demuestra la aplicación práctica de teoría moderna de portafolios para construir carteras eficientes en el mercado mexicano.
