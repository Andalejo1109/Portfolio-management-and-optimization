# Apéndice — DCA mensual vs lump sum (core 2013–hoy)

> Apéndice al análisis de [Portfolio-management-and-optimization](https://github.com/Andalejo1109/Portfolio-management-and-optimization).  
> Material educativo. No es consejo de inversión. Rentabilidades pasadas no predicen resultados futuros.

## Pregunta

Con el **mismo capital total aportado** al core long-only, ¿el DCA mensual supera al lump sum en valor terminal y riesgo entre 2013 y hoy?

## Parámetro clave: aporte mensual

| Parámetro | Valor | Flag |
|-----------|------:|------|
| **Aporte mensual (DCA)** | **USD 200** | [DEFAULT] |
| Capital inicial (DCA) | USD 1,000 | [DEFAULT] |
| Capital total aportado (ambas estrategias) | USD 33,800 | Calculado en muestra |
| Lump sum día 1 | USD 33,800 | Paridad de capital aportado |

El aporte de **USD 200/mes** es el default documentado de la tesis Phase 1 (aportes periódicos, sin market timing).

## Asignación [DEFAULT]

| Ticker | Peso |
|--------|-----:|
| SPYG | 0.31 |
| SMH | 0.22 |
| BRK.B | 0.20 |
| IEMG | 0.20 |
| VTI | 0.07 |

- Long-only, sin apalancamiento, un activo ≤ 50 %.
- Costos: 5 bps por lado en rebalance (sensibilidad 0 / 5 / 15 bps).
- Rebalance: mensual el primer día hábil, al cierre.
- Datos: Adjusted Close (yfinance), 2013-01-02 → 2026-09-28.

## Hallazgos (corrida real, 5 bps)

CAGR = TWR (aportes excluidos del retorno). La comparación de **riqueza** es el valor terminal.

| Estrategia | Capital aportado | Valor terminal | CAGR (TWR) | Max DD | Sharpe rf=0 |
|---|---:|---:|---:|---:|---:|
| DCA mensual (USD 200/mes) | $33,800 | $139,683 | 17.29% | −31.21% | 0.94 |
| Lump sum B&H | $33,800 | $300,128 | 17.30% | −31.21% | 0.94 |

- DCA: 4.13× lo aportado (cagr_on_contributed ≈ 10.9 %).
- Lump sum: 8.88× lo aportado (≈ 17.3 %).

### Sensibilidad de costos

| bps | DCA TV | Lump TV | DCA CAGR | Lump CAGR |
|----:|-------:|--------:|---------:|----------:|
| 0 | $139,899 | $300,835 | 17.31% | 17.31% |
| 5 | $139,683 | $300,128 | 17.29% | 17.30% |
| 15 | $139,252 | $298,720 | 17.25% | 17.27% |

## Lectura

En el bull 2013–2026, el lump sum gana en valor terminal con el mismo capital (más tiempo invertido). El TWR del core es casi idéntico. En estrés corto (2020, 2022) el DCA puede ganar en TV sin cambiar el TWR — coherente con la política de aportes de **USD 200/mes**.

## Relación con el notebook original

El README principal del repo documenta una simulación 2020–2025 con aporte mensual **USD 200** y pesos distintos. Este apéndice extiende la misma pregunta al horizonte 2013–hoy con los pesos vivos de la tesis (31/22/20/20/7) y paridad de capital aportado entre DCA y lump sum.

## Autor

Andrés Alejandro Rodríguez Lozano — economista y científico de datos.  
[andalejo1109.github.io](https://andalejo1109.github.io) — eToro [@Andalejo1109](https://www.etoro.com/people/andalejo1109)

## Licencia

MIT — uso educativo. No es recomendación de inversión.
