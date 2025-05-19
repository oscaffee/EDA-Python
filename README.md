# EDA-Python

## Pasos seguidos en el proyecto

1. **Carga de datos:**
   - Lectura del archivo `bank-additional.xlsx`.
   - Unificación de las hojas de `customer-details.xlsx`.

2. **Limpieza y transformación:**
   - Imputación de valores nulos en columnas categóricas y numéricas.
   - Conversión de tipos (`ID` a string).
   - Eliminación de duplicados.
   - Creación de tramos de edad e ingresos (`tramos_edad`, `tramos_income`).

3. **Fusión de datasets:**
   - Merge por `id_` y `ID` para generar un DataFrame final `df_cruzado`.

4. **Análisis exploratorio:**
   - Estudio de distribución de variables categóricas (`job`, `marital`, `education`, `contact`).
   - Análisis de variables numéricas (`age`, `campaign`, `income`).
   - Visualizaciones con `Seaborn` y `Matplotlib`.

5. **Exportación de datos transformados:**
   - Guardado del DataFrame procesado como `df_cruzado.csv`.

---

## Informe del análisis

### Variables categóricas

- `job`: student y retired presentan la mayor tasa de conversión, aunque representan un volumen bajo.
- `marital`: los single convierten ligeramente más.
- `education`: el grupo illiterate destaca, pero con muy pocos casos. "University.degree" también es positivo.
- `contact`: el contacto por cellular es mucho más efectivo que por telephone.

### Variables numéricas

- `campaign`: a más intentos de contacto, menor conversión.
- `age`: la gente con mas de 60 en age presentan tasas de conversión más altas, aunque representan un porcentaje bajo del total.
- `income`: la conversión es similar en todos los tramos de income, no parece ser determinante.

### Relación `age` vs `income`

- No se observa una correlación fuerte entre edad e ingresos.
- No hay un patrón claro que relacione directamente estas dos variables con el éxito de la campaña.

---

## Cómo ejecutar

1. Clona este repositorio:
git clone https://github.com/oscaffee/EDA-Python.git
