# 🛡️ Trading Bots - 24/7 Keep-Alive Sentinel

Repositorio centinela público de estimulación continua para bots en **Render Free**:
1. **[binance-trading-bot](https://github.com/yunseomiguelbenites-crypto/binance-trading-bot)**: `https://binance-bot-frankfurt.onrender.com`
2. **[fomo-solana-bot](https://github.com/yunseomiguelbenites-crypto/fomo-solana-bot)**: `https://fomo-solana-bot.onrender.com`

## 🎯 Propósito
Garantizar la operatividad **100% continua (24 horas al día, 7 días a la semana)** de los bots de trading alojados en el plan Free de **Render Frankfurt**.

### ¿Cómo funciona?
* Render Free suspende las aplicaciones tras 15 minutos sin tráfico HTTP.
* Este repositorio público ejecuta un flujo automatizado de **GitHub Actions** cada 5 minutos con minutos gratuitos e ilimitados.
* Cada ejecución emite pulsos HTTP continuos hacia los endpoints `/health` y `/ping` de:
  - `https://binance-bot-frankfurt.onrender.com`
  - `https://fomo-solana-bot.onrender.com`
* Esto impide que Render entre en modo reposo nocturno o muestre la pantalla de carga (*"Iniciando..."*).
