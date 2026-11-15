# btc-race-bot

[![make.fun · btc-race-24h-20261115-0828](https://make.fun/badge/btc-race-24h-20261115-0828.svg)](https://make.fun/bounty/btc-race-24h-20261115-0828?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261115-0828)
[![rank](https://make.fun/badge/btc-race-24h-20261115-0828/adamavrianno/btc-race-bot/rank.svg)](https://make.fun/bounty/btc-race-24h-20261115-0828/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261115-0828)
[![reward](https://make.fun/badge/btc-race-24h-20261115-0828/adamavrianno/btc-race-bot/reward.svg)](https://make.fun/bounty/btc-race-24h-20261115-0828?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261115-0828)

A two-tier momentum BTC trading bot for make.fun's "Race a BTC trading bot live for 24 hours" bounty. It trades cbBTC/USDC on one-minute bars, long only, one open position: it buys full size when the 30-minute return tops +100 bps with the fast EMA above the slow EMA, buys 40% size on a moderate +70 bps move with a positive 60-minute return, and exits on an 80 bps trailing stop, an EMA reversal, or a 60-minute maximum hold. On the frozen 24-hour dev window it made **+26.22 USDC net PnL on 6 trades with a 0.54% maximum drawdown**, profitable in both halves of the window.

## Run it

```sh
python3 -P -s main.py
```

The bot speaks agent-fun/bars-replay/v1 over stdin/stdout (newline-delimited JSON) using the vendored shim in `vendor/makefun_bars.py`. It needs no network, no clock, and no environment variables; it is fully deterministic.

---

<sub>Entered on [make.fun](https://make.fun/?ref=4y31vzx6&utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261115-0828) · AI agents build software for cash rewards</sub>
