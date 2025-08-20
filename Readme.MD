Telecom X — Análisis de Evasión de Clientes (Churn)

> Proyecto del Challenge: Telecom X: análisis de evasión de clientes  
> Objetivo: entender por qué los clientes abandonan el servicio y qué variables se asocian al churn.

 Propósito
- Explorar el dataset, limpiar/transformar variables y identificar patrones asociados a la evasión.
- Construir un EDA sólido con visualizaciones claras y insights accionables.
- (Opcional) Probar un modelo de "baseline" para estimar la probabilidad de churn.

 Estructura del repositorio

telecomx-churn/
├── data/              - datasets 
│   └── README.txt
├── images/            - figuras exportadas 
├── notebooks/
│   └── telecomx_churn_eda.ipynb   # notebook principal (Colab friendly)
├── src/
│   └── utils.py       - helpers 
└── README.md          - este archivo


 Datos
Coloca el archivo CSV del challenge en `data/` (por ejemplo `telecom_churn.csv`).  
Si usas Google Colab, puedes montar Google Drive o leer el CSV desde un enlace público.

 Cómo ejecutar
Opción A — Google Colab (recomendado)
1. Abre el notebook: `notebooks/telecomx_churn_eda.ipynb` directamente desde **Colab**.  
2. Sube el CSV a `data/` (montando *Drive* o cargando desde una URL).  
3. Ejecuta las celdas en orden.

 Opción B — Local (Jupyter)
1. Crea y activa un entorno:
   bash
   python -m venv .venv
   source .venv/bin/activate  # Windows: .venv\Scripts\activate
   pip install -U pip
   pip install -r requirements.txt  # (si lo creas) o: pip install pandas numpy matplotlib seaborn scikit-learn
   ```
2. Inicia Jupyter:
   bash
   jupyter lab  # o jupyter notebook
   
3. Abre `notebooks/telecomx_churn_eda.ipynb` y ejecuta.

 Contenido del notebook
- Carga e inspección del dataset (`head`, `info`, nulos, duplicados).
- Limpieza/transformación (casting, mapeos, outliers simples).
- EDA: "churn rate", barras, histogramas, boxplots, heatmap de correlación.
- "Insights" (sección final con conclusiones).

 Ejemplos de visualizaciones
Inserta aquí imágenes exportadas desde el notebook (guárdalas en `images/`):
- `images/churn_rate.png`
- `images/churn_por_servicio.png`
- `images/heatmap_correlacion.png`

 Reproducibilidad
Requisitos mínimos:
```
pandas
numpy
matplotlib
seaborn
scikit-learn   # opcional para baseline

> Puedes crear un `requirements.txt` con esos paquetes si lo deseas.

 Publicación en GitHub (resumen)
bash
git init
git add .
git commit -m "First version: Telecom X churn EDA"
git branch -M main
git remote add origin https://github.com/<TU_USUARIO>/telecomx-churn.git
git push -u origin main


 Insights — para completar
- Ejemplo: Los clientes con contrato mensual presentan un churn X% mayor que los de contrato anual.
- Ejemplo: Soporte técnico tardío y *tenure* bajo son los principales factores asociados al churn.
- (Reemplaza por hallazgos reales tras tu EDA.)



Autor: Cristian Sanchez O. · Licencia: MIT 