# Resumen para la prueba – ADMI140 Finanzas Corporativas (Dra. Roxana Pincheira, UACh)

Fuentes del repositorio:
- `PRESENTACIÓN RIESGO RETORNO (2).pptx` (teoría, 22 diapositivas)
- `BASE DE DATOS IPSA FINALIZADA (1).xlsx`, `Base de datas Precios ADIDAS (1).xlsx`, `Hecho por la profe.xlsx` (ejercicios en Excel)
- `EJERCICIO INSTRUMENTO RENTA VARIABLE ACCIONES (1).docx` (valoración de acciones del retail: Mall Plaza, Cencosud Shopping, Parque Arauco)

> Los resultados numéricos de los ejemplos y del ejercicio de valoración los calculé yo a partir de los datos. Los supuestos van indicados; compáralos con lo que se hizo en clase.

---

## 1. Relación riesgo-retorno (conceptos)

- Las inversiones ofrecen rendimientos muy distintos. Las **acciones son más riesgosas que los bonos** y, como compensación, rinden más en promedio.
- Si una inversión es riesgosa, tiene **varios rendimientos posibles** según la situación económica.
- **Tasa libre de riesgo (rf):** retorno de un activo sin riesgo (ej. bonos del Tesoro).
- **Premio por riesgo:** retorno adicional sobre rf que recibe el inversionista por asumir riesgo. Regla general: más riesgo, más retorno exigido.
- **Retorno:** incremento porcentual del valor por cada peso invertido. Se usa porque permite comparar activos con precios, dividendos y tamaños distintos.
- **Riesgo:** posibilidad de que el retorno real difiera del esperado, incluso perdiendo parte o toda la inversión.

Datos de mercado que aparecen:
- EE.UU.: NYSE fundada en 1792, NASDAQ en 1971 (más de 230 años de mercado de capitales).
- Chile: Bolsa de Comercio de Santiago (BCS) desde 1893; Bolsa Electrónica de Chile (BEC) desde 1989.
- Más del 90% de las acciones transadas en Chile pasa por la BCS. La BEC complementa en renta fija y operaciones entre bancos.

---

## 2. Enfoque con probabilidades (escenarios)

Se definen escenarios, se asigna una probabilidad a cada uno y se pondera.

| Medida | Fórmula |
|---|---|
| Retorno esperado | E[R] = Σ pᵣ · R |
| Varianza | Var(R) = Σ pᵣ · (R − E[R])² |
| Desviación estándar | SD(R) = √Var(R) |
| Índice de Sharpe | Sharpe = (E[R] − rf) / SD |

- Si el retorno nunca se desvía de su media, Var = 0. Mientras mayores las desviaciones, mayor la varianza.
- E[R] es lo que se ganaría **en promedio** si se repitiera la inversión muchas veces. No está garantizado.
- **Sharpe** (William F. Sharpe, 1966, "Mutual Fund Performance"): retorno adicional sobre rf por cada unidad de riesgo total. Sirve para comparar inversiones con retornos y riesgos distintos. **Mayor Sharpe = mejor.**

### Ejemplos de clase resueltos (rf = 2,1%)

**Ejemplo 1**

| R | p |
|---|---|
| −20% | 25% |
| 10% | 50% |
| 40% | 25% |

- E[R] = 0,25(−20) + 0,5(10) + 0,25(40) = **10%**
- Var = 0,25(−30)² + 0,5(0)² + 0,25(30)² = 450 %² = **0,045**
- SD = **21,21%**
- Sharpe = (10 − 2,1) / 21,21 = **0,37**

**Ejemplo 2**

| Escenario | R | p |
|---|---|---|
| Optimista | 15% | 30% |
| Neutral | 7% | 50% |
| Pesimista | −5% | 20% |

- E[R] = 4,5 + 3,5 − 1 = **7%**
- Var = 0,3(8)² + 0,5(0)² + 0,2(−12)² = 48 %² = **0,0048**
- SD = **6,93%**
- Sharpe = (7 − 2,1) / 6,93 = **0,71**

**Conclusión:** el Ejemplo 1 rinde más, pero el Ejemplo 2 entrega más retorno por unidad de riesgo (Sharpe 0,71 > 0,37).

---

## 3. Enfoque con datos históricos

### 3.1 Retornos

- Sin dividendos: **R = (P₁ − P₀) / P₀**
- Con dividendos: **R = (P₁ + D₁ − P₀) / P₀**
- Retorno anual a partir de subperíodos: **(1 + R_anual) = (1 + R₁)(1 + R₂)…(1 + Rₙ)**

**Ejemplo de la diapositiva 13:**

| Fecha | Precio | Dividendo | Retorno del tramo |
|---|---|---|---|
| 31/12/2022 | 2,79 | – | – |
| 21/02/2023 | 2,80 | 0,14 | (2,80 + 0,14 − 2,79)/2,79 = 5,38% |
| 22/08/2023 | 2,97 | 0,14 | (2,97 + 0,14 − 2,80)/2,80 = 11,07% |
| 30/12/2023 | 3,33 | – | (3,33 − 2,97)/2,97 = 12,12% |

R anual 2023 = 1,0538 × 1,1107 × 1,1212 − 1 = **31,23%**

### 3.2 Media aritmética vs. geométrica

- **Aritmética:** R̄ = (1/T)(R₁ + R₂ + … + R_T). Promedia los años como independientes y **no considera el efecto compuesto**. Si la distribución de retornos es estable en el tiempo, sirve como estimación del retorno esperado.
- **Geométrica:** 1 + R_geo = ⁿ√[(1 + R₁)(1 + R₂)…(1 + Rₙ)]. Refleja el **efecto compuesto** (retorno acumulado). **Siempre ≤ aritmética** cuando hay variabilidad.

Ejercicio de la diapositiva 15 (2010–2014):

| Activo | Aritmética | Geométrica | SD |
|---|---|---|---|
| S&P500 | 19,38% | 18,34% | 16,65% |
| GM | 9,36% | 7,31% | 21,66% |
| Bonos | 5,20% | 5,20% | 0,47% |

Mientras más volátil el activo, mayor la brecha entre aritmética y geométrica (GM es el caso más claro; en los bonos casi no hay diferencia).

### 3.3 Riesgo histórico (muestral, se divide por T − 1)

- **Var(R) = [1/(T − 1)] Σ (R_t − R̄)²**
- **SD(R) = √Var(R)**
- Las acciones pequeñas muestran más dispersión que las grandes. Las grandes varían menos, pero más que los bonos corporativos.

### 3.4 Error de estimación e intervalo de confianza

- Solo tenemos una muestra. No conocemos el retorno ni la volatilidad verdaderos de la población.
- **Error estándar: SE = SD / √n** (n = número de observaciones, ej. años).
- **Intervalo de confianza: R̄ ± Z × SE**, con Z = 1,96 (95%) o Z = 2,58 (99%).
- Mientras más datos (n), menor SE y más preciso el intervalo.

### 3.5 Retornos logarítmicos

¿Por qué no basta el retorno simple? Está acotado a la izquierda (no se puede perder más de −100%) pero no tiene límite a la derecha. Eso lo hace asimétrico, no sigue una distribución normal, y el SE y los intervalos pierden precisión.

**Solución:** R_ln = ln(P_t / P_{t−1}) = ln(1 + R_simple), que es un retorno compuesto continuamente.

Propiedades:
- **Simetría.**
- **Aditividad temporal:** el retorno anual ln es la **suma** de los retornos mensuales ln. Con retornos simples, en cambio, hay que **multiplicar** (1 + R).

---

## 4. Paseo aleatorio y eficiencia de mercado

- **Paseo aleatorio (random walk):** los cambios de precio de un día a otro son impredecibles y no dependen del pasado. Los retornos son **iid**: independientes e idénticamente distribuidos (misma media y volatilidad).
- El historial sirve de referencia, pero la variabilidad es alta: se gestionan probabilidades, no certezas.
- **Hipótesis de Mercados Eficientes (EMH, Fama 1970):** los precios reflejan toda la información disponible. No se pueden obtener retornos ajustados por riesgo sobre el promedio de forma consistente.
  - **Débil:** los precios incorporan la información de precios pasados (t − i).
  - **Semifuerte:** además, toda la información pública.
  - **Fuerte:** toda la información, pública y privada.
  - En la práctica, los mercados tienden a la forma débil o semifuerte.
- **Modelo con tendencia:**
  - p_t = α + p_{t−1} + ε_t
  - p_T = α + p₀ + ε₁ + ε₂ + … + ε_T
  - El precio es el precio inicial más una tendencia (α) más la suma de shocks (noticias no anticipadas).

---

## 5. Procedimiento en Excel (lo que hacen las planillas)

Pasos de la diapositiva 22, aplicados al IPSA 2010–2025 (mensual), a Adidas 2023–2025, y a CMIG4 y OIBR4 2015–2022 (planilla de la profe):

1. Ordenar fecha y precio.
2. Retorno simple: `=(B5-B4)/B4`. Columna auxiliar `=C5+1`. Retorno ln: `=LN(B5/B4)`.
3. Retorno **anual** por año:
   - Simple: `=PRODUCT(D5:D15)-1` (producto de los 1 + R del año).
   - Ln: `=SUM(E5:E15)` (suma de los ln del año).
4. Estadísticos sobre los retornos anuales:
   - Retorno esperado: `=AVERAGE(...)`
   - Varianza: `=VAR.S(...)`
   - SD: `=SQRT(var)`
   - SE: `=SD/SQRT(n)` (IPSA n = 15, CMIG/OIBR n = 8, Adidas n = 3)
   - IC 95%: `=media ± 1.96*SE`
5. **Simulación del paseo aleatorio** (24 meses en adelante, 5 escenarios):
   - Shock mensual: `=NORM.INV(RAND(); media; SD)`, usando la media y SD de los retornos mensuales.
   - Precio simulado: `=P_anterior*EXP(shock)`, partiendo del último precio real. Luego se arrastra la fórmula.

Resultados de las planillas que conviene recordar:

| Serie | E[R] anual | SD anual | SE | IC 95% |
|---|---|---|---|---|
| IPSA simple (2010–2024) | 4,91% | 15,66% | 4,04% | [−3,02%; 12,83%] |
| IPSA ln (2010–2024) | 3,77% | 14,68% | 3,79% | [−3,65%; 11,20%] |
| CMIG4 ln (2015–2022) | 5,05% | 39,52% | 13,97% | [−22,33%; 32,44%] |
| OIBR4 ln (2015–2022) | −28,32% | 76,81% | 27,16% | [−81,54%; 24,91%] |

Lectura: todos los intervalos incluyen el 0. Con pocos años y alta volatilidad, **no se puede afirmar con 95% de confianza que el retorno esperado sea positivo**. OIBR4 es mucho más riesgosa que CMIG4.

---

## 6. Valoración de acciones (documento Word, industria retail)

Supuesto: tasa exigida por los inversionistas **rE = 13%**. Los montos de los estados financieros están en miles de CLP.

### 6.1 Modelo de Dividendos Descontados (MDD / Gordon)

- **P₀ = D₁ / (rE − g)**
- **D₁ = D₀ (1 + g)**
- **D₀ = UPA × Payout**, donde **UPA = Utilidad neta / N° de acciones**
- **g = b × ROE**, con b = 1 − Payout (tasa de retención). El documento entrega "Rentabilidad sobre Activos", así que usé esa tasa como rentabilidad del capital reinvertido.

| | Mall Plaza | Cencosud Shopping |
|---|---|---|
| Utilidad neta TTM | 161.093.419 | 204.040.958 |
| Acciones | 1,96 B | 1,71 B |
| UPA | $82,19 | $119,32 |
| Payout | 40,44% | 76,10% |
| D₀ | $33,24 | $90,80 |
| g = (1 − payout) × ROA | 2,64% | 1,10% |
| D₁ | $34,11 | $91,80 |
| **P₀ = D₁/(13% − g)** | **$329** | **$772** |
| Precio de mercado | $2.101,10 | $1.398,80 |

Con estos supuestos, ambas acciones quedan sobrevaloradas por el mercado según MDD. Si en clase usaron ROE (Utilidad / Patrimonio) en vez de ROA, g sube y P₀ también.

### 6.2 Flujo de Caja Libre Descontado (datos de Mall Plaza)

- **FCL = Utilidad neta + Depreciación − CAPEX − ΔCapital de trabajo**
- Depreciación del año = Dep. acumulada 2022 − Dep. acumulada 2021 = 2.100.207 − 1.825.227 = **274.980** (miles $)
- CAPEX 2022 = 1.030.239 (miles $)
- ΔCT = (Activo corriente − Pasivo corriente)₂₀₂₂ − (Activo corriente − Pasivo corriente)₂₀₂₁
- Valor = FCL₁ / (r − g). Al resultado se le suma la caja y se resta la deuda (si se descontó a nivel empresa), y se divide por el número de acciones.

No calculé el número final porque depende de la convención usada en clase (FCL del accionista o de la empresa, y tratamiento del capital de trabajo). Revisa ese paso con tus apuntes.

### 6.3 Empresas comparables (múltiplos) para valorar Parque Arauco

Se calculan los múltiplos de las comparables (Mall Plaza y Cencosud Shopping), se promedian y se aplican a Parque Arauco.

- **P/E** = Precio / UPA (o Capitalización / Utilidad neta)
- **P/B** = Precio / Valor libro por acción (Patrimonio / acciones)
- **EV/EBITDA**, donde **EV = Capitalización + Deuda − Caja**
- Capitalización = Precio × N° de acciones

| Múltiplo | Mall Plaza | Cencosud Shopping | Promedio |
|---|---|---|---|
| P/E | 25,56 | 11,72 | 18,64 |
| P/B | 2,28 | 0,89 | 1,58 |
| EV/EBITDA* | 24,83 | 14,54 | 19,68 |

\*Para el EV usé los pasivos totales como deuda. Cencosud Shopping tiene caja de 122,32 B. A Mall Plaza no se le entrega dato de caja, así que usé caja = 0.

Datos de Parque Arauco:
- Utilidad neta 78.569.881
- Patrimonio 1.144.928.854
- EBITDA 198.860.323
- Pasivos 1.582.145.524
- Caja 337,31 B
- Acciones 905,72 M

Con esos datos: UPA = $86,75 y valor libro por acción = $1.264,11.

| Método | Precio implícito Parque Arauco |
|---|---|
| P/E: 18,64 × 86,75 | **≈ $1.617** |
| P/B: 1,58 × 1.264,11 | **≈ $2.003** |
| EV/EBITDA: (19,68 × EBITDA − Pasivos + Caja) / acciones | **≈ $2.948** |

Los métodos entregan valores distintos. Por eso se suele reportar un rango, o un promedio, y se compara con el precio de mercado.

---

## 7. Checklist rápido para la prueba

- [ ] Calcular E[R], Var, SD y Sharpe con escenarios y probabilidades.
- [ ] Retorno con y sin dividendos; encadenar retornos para obtener el anual.
- [ ] Diferencia entre media aritmética y geométrica, y por qué la geométrica es ≤ la aritmética.
- [ ] Varianza muestral (T − 1), SE = SD/√n, IC = media ± 1,96·SE.
- [ ] Por qué usar retornos ln (simetría, aditividad); retorno anual ln = suma de los mensuales.
- [ ] Paseo aleatorio (iid) y las 3 formas de la EMH.
- [ ] Simulación en Excel: NORM.INV(RAND(); μ; σ) y P_t = P_{t−1}·e^ε.
- [ ] MDD: P₀ = D₁/(r − g), con g = (1 − payout) × rentabilidad.
- [ ] FCL = UN + Dep − CAPEX − ΔCT.
- [ ] Múltiplos P/E, P/B y EV/EBITDA, y cómo despejar el precio de la empresa objetivo.

Bibliografía citada en la presentación:
- Bodie, Kane y Marcus (2019), *Investments*
- Elton y Gruber (2010), *Modern Portfolio Theory and Investment Analysis*
- Sharpe (1966), "Mutual Fund Performance"
- Fama (1970), "Efficient Capital Markets"
- Malkiel (2019), *A Random Walk Down Wall Street*
