<div align="center">
  <img src="logo.png" alt="Quantum Engine V10" width="160" height="160">

  <h1>QUANTUM ENGINE V10</h1>
  <h3>Systematic Mean-Reversion Strategy with Strict Risk Control</h3>

  <p>
    <img src="https://img.shields.io/badge/MetaTrader-5-blue?style=for-the-badge&logo=metatrader" alt="MT5">
    <img src="https://img.shields.io/badge/Systematic-Trading-8B5CF6?style=for-the-badge" alt="Systematic">
    <img src="https://img.shields.io/badge/Status-90--Day%20Forward%20Testing-F59E0B?style=for-the-badge" alt="Status">
  </p>

  <p>
    <strong>🌍 <a href="#-english-version">English</a> &nbsp;|&nbsp; <a href="#-versión-español">Español</a></strong>
  </p>
</div>

---

## 🇬🇧 English Version

<br>

## ⚡ System Overview

**Quantum Engine V10** is a systematic trading algorithm running on MetaTrader 5. It is built strictly around Mean Reversion principles, targeting specific volatility extremes on GBPJPY and NZDUSD on the M15 timeframe.

**Transparency Notice:** We do not market "holy grails". This algorithm is the result of rigorous historical optimization (In-Sample testing) over 5 years of data. We are fully aware of the risks of curve-fitting (overfitting) in algorithmic development. Therefore, the system is currently undergoing a strict **90-Day Out-of-Sample Forward Testing phase** on a live account with real spreads and slippage before any commercial deployment.

---

## ⚠️ System Limitations & Vulnerabilities

In the spirit of radical transparency, we explicitly disclose the known weaknesses of this algorithm. It is not designed to win in every market condition.

*   **Regime Dependence:** The system works exponentially better in ranging markets than in strong trends.
*   **High Volatility Vulnerability:** It can suffer continuous drawdowns during prolonged, high-volatility, unidirectional market regimes (e.g., severe macroeconomic shifts).
*   **Pair Optimization Risk:** The parameters are highly optimized specifically for the historical behavior of GBPJPY and NZDUSD. Applying this system to other pairs or expecting these two pairs to perfectly repeat their 2020-2024 behavior carries inherent risk.

---

## 🛡️ Advanced Risk Management & Real-World Defenses

To mitigate the vulnerabilities listed above, V10 defends capital using hard-coded risk architecture:

*   **Market Regime Filter (ADX):** The system dynamically identifies ranging vs. trending environments and avoids entering trades during strong, unidirectional trends.
*   **Volatility Cap (ATR Filter):** Blocks new positions during periods of extreme volatility spikes, drastically reducing vulnerability to macro shocks.
*   **Multi-Timeframe Confirmation:** Validates entry signals on a higher timeframe (H1) to ensure the trade aligns with the broader market structure.
*   **No Martingale / No Grid:** The system never averages down on losing trades. Every entry has a strict, dynamic Stop Loss calculated in real-time using ATR (Average True Range).
*   **Daily Kill Switch (Black Swan Defense):** A hard-coded daily loss limit (3.3%) acts as an absolute circuit breaker. If an unprecedented event occurs, the bot physically stops trading for the day.
*   **News Filter (Macroeconomics):** The system pauses operations around high-impact events (such as NFP) to avoid extreme institutional slippage.
*   **Weekend Close:** The bot is prohibited from trading on Friday afternoons, preventing exposure to catastrophic weekend opening gaps.

---

## 📊 Historical Backtest Data (In-Sample)

> **Disclaimer:** The following metrics represent 5 years of historical *optimized* data (Jan 2020 – Dec 2024). Past performance in an optimized backtest does not guarantee future live results.

<br>

### 🛡️ PROP FIRM Profile — 0.33% Risk Per Trade

| Metric | Historical Result |
|--------|-------------------|
| 📅 Average Annual Return | **+45.00% / Year** |
| 📉 Max Historical Drawdown | **9.52%** |
| 🎯 Win Rate | **42.09%** |
| 📈 Profit Factor | **> 1.36** |
| ❌ Max Consecutive Losses | **7** |
| 💰 Expectancy per trade | **+$34.00** |

<br>

### 🚀 PERSONAL Profile — 1.0% Risk Per Trade

| Metric | Historical Result |
|--------|-------------------|
| 📅 Average Annual Return | **+522.98% / Year** |
| 📉 Max Historical Drawdown | **27.78%** |
| 🎯 Win Rate | **42.09%** |
| 📈 Profit Factor | **> 1.53** |
| ❌ Max Consecutive Losses | **7** |
| 💰 Expectancy per trade | **+$395.00** |

*Note: We assume real-world live drawdown could reach up to 1.5x - 2.0x the historical backtest drawdown due to shifting market regimes and slippage scaling.*

---

## 📈 Live Track Record (Forward Testing)

**Status: Currently in 90-Day Live Forward Testing — Day 0.**

To prove this algorithm is not merely curve-fitted to the past, it is actively running on a live environment to measure real-world execution, slippage, and performance.

> 🔗 **Verified Live Account on MyFxBook — Results are updated in real-time as they accumulate:**
>
> [![MyFxBook](https://img.shields.io/badge/MyFxBook-Live%20Verified%20Account-1a6e37?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNkYPhfDwAChwGA60e6kgAAAABJRU5ErkJggg==&logoColor=white)](https://www.myfxbook.com/members/cristiandortizg/cristian-ortiz--quantum-trading/12053900)
>
> ⚠️ *The account currently has **0 days** of live trading data. Results will be reflected here automatically as forward testing progresses.*

---

## 🚀 Future Deployment (Copy Trading Model)

Pending successful forward testing, access to the algorithm will be strictly managed via a **Copy Trading / Master Account architecture**. 

To protect the intellectual property, the `.exe` software is not distributed. Trades will be executed on our master servers and replicated to client accounts.

---

<br><br>

## 🇪🇸 Versión Español

<br>

## ⚡ Visión General del Sistema

**Quantum Engine V10** es un algoritmo de trading sistemático para MetaTrader 5. Está construido estrictamente sobre principios de Reversión a la Media, buscando extremos específicos de volatilidad en GBPJPY y NZDUSD en la temporalidad M15.

**Aviso de Transparencia:** No vendemos "santos griales". Este algoritmo es el resultado de una rigurosa optimización histórica sobre 5 años de datos. Somos plenamente conscientes de los riesgos de sobreajuste (overfitting). Por lo tanto, el sistema se encuentra actualmente en una estricta **fase de Forward Testing de 90 días en vivo** (con spreads y slippage reales) antes de cualquier despliegue comercial.

---

## ⚠️ Limitaciones y Vulnerabilidades del Sistema

En un esfuerzo de transparencia radical, revelamos explícitamente las debilidades conocidas de este algoritmo. No está diseñado para ganar en todas las condiciones de mercado.

*   **Dependencia de Régimen:** El sistema funciona exponencialmente mejor en mercados en rango que en tendencias fuertes.
*   **Vulnerabilidad a Alta Volatilidad:** Puede sufrir rachas de pérdidas continuas durante regímenes de mercado unidireccionales y de alta volatilidad (ej. shocks macroeconómicos severos).
*   **Riesgo de Optimización de Pares:** Los parámetros están altamente optimizados específicamente para el comportamiento histórico de GBPJPY y NZDUSD. Aplicar este sistema a otros pares o esperar que estos dos repitan perfectamente su comportamiento de 2020-2024 conlleva un riesgo inherente.

---

## 🛡️ Gestión de Riesgo y Defensas del Mundo Real

Para mitigar las vulnerabilidades mencionadas, el V10 defiende el capital usando una arquitectura de riesgo estricta:

*   **Filtro de Régimen de Mercado (ADX):** Identifica dinámicamente si el mercado está en rango o en tendencia, y evita operar durante tendencias fuertes.
*   **Filtro de Volatilidad (ATR):** Bloquea nuevas operaciones durante picos extremos de volatilidad, reduciendo drásticamente la vulnerabilidad a shocks macroeconómicos.
*   **Confirmación Multi-Timeframe:** Valida las señales de entrada en una temporalidad superior (H1) para asegurar que la operación esté alineada con la estructura mayor.
*   **Cero Martingala / Cero Grid:** El sistema jamás promedia a la baja. Cada entrada tiene un Stop Loss duro y dinámico calculado en tiempo real mediante el ATR.
*   **Kill Switch Diario (Defensa de Cisnes Negros):** Un límite de pérdida diaria (3.3%) actúa como un cortacorriente absoluto. Si ocurre un evento extremo, el bot suspende toda operativa por el resto del día.
*   **Filtro de Noticias (Macroeconomía):** El sistema pausa la operativa alrededor de eventos de alto impacto (como NFP) para evitar deslizamientos letales.
*   **Cierre de Fin de Semana:** El bot tiene prohibido operar los viernes por la tarde, evitando la exposición catastrófica a gaps de apertura el domingo.

---

## 📊 Datos Históricos de Backtest (In-Sample)

> **Aviso:** Las siguientes métricas representan 5 años de datos históricos *optimizados* (Ene 2020 – Dic 2024). Los rendimientos pasados en un backtest optimizado no garantizan resultados futuros en vivo.

<br>

### 🛡️ Perfil FONDEO — 0.33% de Riesgo por Operación

| Métrica | Resultado Histórico |
|---------|---------------------|
| 📅 Rendimiento Anual Promedio | **+45.00% / Año** |
| 📉 Drawdown Máximo Histórico | **9.52%** |
| 🎯 Win Rate | **42.09%** |
| 📈 Profit Factor | **> 1.36** |
| ❌ Máximas Pérdidas Consecutivas | **7** |
| 💰 Expectativa por Operación | **+$34.00** |

<br>

### 🚀 Perfil PERSONAL — 1.0% de Riesgo por Operación

| Métrica | Resultado Histórico |
|---------|---------------------|
| 📅 Rendimiento Anual Promedio | **+522.98% / Año** |
| 📉 Drawdown Máximo Histórico | **27.78%** |
| 🎯 Win Rate | **42.09%** |
| 📈 Profit Factor | **> 1.53** |
| ❌ Máximas Pérdidas Consecutivas | **7** |
| 💰 Expectativa por Operación | **+$395.00** |

*Nota: Asumimos que el Drawdown en vivo puede llegar a ser entre 1.5x y 2.0x el drawdown del backtest debido a cambios de régimen de mercado y escalado de slippage.*

---

## 📈 Track Record en Vivo (Forward Testing)

**Estado: Actualmente en fase de Forward Testing en vivo de 90 días — Día 0.**

Para demostrar que este algoritmo no está simplemente "ajustado a la curva" del pasado, actualmente se está ejecutando en un entorno en vivo para medir la ejecución real y el rendimiento en los regímenes actuales.

> 🔗 **Cuenta en Vivo Verificada en MyFxBook — Los resultados se actualizan en tiempo real:**
>
> [![MyFxBook](https://img.shields.io/badge/MyFxBook-Cuenta%20Verificada%20en%20Vivo-1a6e37?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mNkYPhfDwAChwGA60e6kgAAAABJRU5ErkJggg==&logoColor=white)](https://www.myfxbook.com/members/cristiandortizg/cristian-ortiz--quantum-trading/12053900)
>
> ⚠️ *La cuenta actualmente tiene **0 días** de datos de trading en vivo. Los resultados se verán reflejados aquí automáticamente conforme avance el forward testing.*

---

## 🚀 Despliegue Futuro (Modelo Copy Trading)

Pendiente del éxito del Forward Testing, el acceso se gestionará a través de una **arquitectura de Copy Trading**.

Para proteger la propiedad intelectual, el software `.exe` no se distribuye. Las operaciones se ejecutarán en nuestros servidores maestros y se replicarán a las cuentas de los clientes.

---

## 📬 Contacto para Desarrolladores

<div align="center">

**Para consultas técnicas o unirse a la lista de espera del programa Beta (Forward Testing):**

[![WhatsApp](https://img.shields.io/badge/WhatsApp-Developer%20Contact-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/584247062011)

</div>

---

<div align="center">
  <br>
  <sub>Systematic Algorithmic Development · Forward-Tested Infrastructure</sub>
</div>
