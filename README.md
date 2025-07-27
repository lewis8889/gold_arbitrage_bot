# gold_arbitrage_bot_v1

套利系统：OKX 的 `xaut-usdt-swap` 合约 与 MT5 的 `XAUUSD` 进行对冲套利与资金费套利。

---

## 🚀 功能亮点

- ✅ 双平台套利：加密合约 vs 外汇现货
- ✅ Web 前端配置界面（手数、方向、API）
- ✅ 默认以 OKX 限价挂单成交后，触发 MT5 对冲单
- ✅ 支持 50 倍杠杆，手续费控制更优
- ✅ 支持套利差价 + 资金费套利双重收益模型

---

## 💡 套利策略逻辑

1. 实时监控 OKX 和 MT5 报价
2. 当价差 > 10 美金，系统在 OKX 限价挂单（Sell）
3. 成交后立刻在 MT5 平台开多仓（Buy）
4. 收取 OKX 平台资金费收益（如每 4 小时 0.005%）
5. 价差回归平仓，获取双重收益

---

## 🛠 环境部署（Windows VPS）

1. 安装 Python 3.11 以上版本：https://www.python.org/downloads/windows/
2. 安装依赖库：
```bash
pip install -r requirements.txt
