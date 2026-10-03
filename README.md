# 🛡️ Binance Trading Bot - 24/7 Keep-Alive Sentinel

Repositorio hermano público de [binance-trading-bot](https://github.com/yunseomiguelbenites-crypto/binance-trading-bot).

## 🎯 Propósito
Garantizar la operatividad **100% continua (24 horas al día, 7 días a la semana)** del bot de trading alojado en el plan Free de **Render Frankfurt**.

### ¿Cómo funciona?
* Render Free suspende las aplicaciones tras 15 minutos sin tráfico HTTP.
* Este repositorio público ejecuta un flujo automatizado de **GitHub Actions** cada 5 minutos con minutos gratuitos e ilimitados.
* Cada ejecución emite pulsos HTTP continuos hacia los endpoints `/health` y `/ping` de:
  `https://binance-bot-frankfurt.onrender.com`
* Esto impide que Render entre en modo reposo nocturno o muestre la pantalla de carga (*"Iniciando..."*).
