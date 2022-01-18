# Alpha KCC Dex Bot

<center><a href="https://ibb.co/XFXq7RT"><img src="https://i.ibb.co/XFXq7RT/bot-icon-1.png" alt="bot-icon-1" border="0"></a></center>


- AlphaBot is an automated trading bot for the KCC DeFi ecosystem, however it is compatible with several other EVM chains. 

- AlphaBot has the ability to scan multiple trading pairs on a Dex, grab the price in realtime and make automated trading decisions based on user settings.

**To use AlphaBot you must hold [ALPHA](https://alphadao.money) tokens (KCC) in your bot wallet.**

[**Buy ALPHA on KuSwap**](https://kuswap.finance/#/swap?outputCurrency=0x0490c1076552ed3c91876ead9f6a547b389e69d4)



### There are 3 subscription levels:

### **Tier 1:** 
     
      Beta:   1 ALPHA token (Slow speed - 6s between each price check. No mempool monitoring)

### **Tier 2:** 

      Frog King:   5 ALPHA tokens (Medium speed - 3s between each price check. No mempool monitoring)

### **Tier 3:** 

      ALPHA:    10 ALPHA tokens (Super fast speed - no delay between each price check. All features unlocked and priority support in the Alpha DAO Telegram. https://t.me/alphadao1337



## Features include:
- Dex Limit Orders
- Dex Stop Loss.
- Mempool Sniping (AlphaBot is fast enough to snipe liquidity in the same block)
- Accumulation Mode
- Take profit
- trailing take profit
- Grid trading
- Automated Rug Doc
- Front run
- Liquidity check / monitoring
- PK encryption

## Supported Dex:

- **KuSwap**
- **Koffee Swap**
- PanCake Swap
- Pink Swap
- Bakery Swap
- BiSwap
- Ape Swap
- Trader Joe
- Pangolin
- Spooky Swap
- Spirit Swap
- Quick Swap
- UniSwap

___


![image](https://i.ibb.co/6g7GpLn/Capture.png)


## Installation

You will need to have the latest version of [Pyhon](https://www.python.org/downloads/) & [Visual Studio](https://visualstudio.microsoft.com/fr/thank-you-downloading-visual-studio/?sku=Community&rel=17) installed.


### Update!! 1/18/22: You now have the option to simply run the precompiled .exe from inside the AlphaBot folder! 

If you would still like to run the bot from source please follow the instructions below 👇 

Clone this repo:

```
git clone https://github.com/cusdt-LINK/alpha-kcc-dex-bot
```

Install requirements:

```
pip install -r requirements.txt`  --> this will install all the packages needed to run AlphaBot.
```

Open **Windows Powershell** (or Mac Terminal on MacOs)

Navigate to the AlphaBot folder

```
cd path\to\alphabot\folder 

```

Run AlphaBot

```
python alphabot.py 

```

## Configuration (settings.json)

'USECUSTOMNODE':
Set it to "true" if you want to use a custom node.

'CUSTOMNODE':
If you want to use a custom node, enter here your node's address in http, wss, or RPC.

'PREAPPROVE':
Tells the bot to preapprove tokens on startup or not

'ENCRYPTPRIVATEKEYS':
Will be filled automatically when you start the bot for the first time

'UNLIMITEDSLIPPAGE':
Use this parameter if you want the bot to bypass completely the slippage setting and buy at any slippage, to avoid the "INSUFFICIENT_AMOUNT" Error 

If you select UNLIMITEDSLIPPAGE= true, AlphaBot won't take into account the SLIPPAGE parameter. 

'PASSWORD_ON_CHANGE':
Activate this option if you want the bot to ask your private key's password again when you update tokens.json
(useful if you're afraid someone could change it while the bot is running)

'VERBOSE_PRICING':
Default setting is "true", but if you set it to "false", bot will only show lines on the screen if the price is updated. 

```
"ALPHAWALLETPRIVATEKEY": "private key where $ALPHA token is held on KCC",
"ALPHAWALLETADDRESS": "wallet address where $ALPHA token is held on KCC",
"WALLETADDRESS": "wallet address to trade with on exchange",
"PRIVATEKEY": "private key of walletaddress to trade with",
"USECUSTOMNODE": "false",
"CUSTOMNODE": "put your own node here if you want and make, USECUSTOMNODE = TRUE",
"EXCHANGE": "KuSwap"

```

## tokens.json

```

[
  {

    "ENABLED": "true",

    "SYMBOL": "ALPHA",
    "ADDRESS": "0x0490c1076552ed3c91876ead9f6a547b389e69d4",
    
    "KIND_OF_SWAP": "tokens",
    "BUYAMOUNTINBASE": "0.000005",
    "BUYAMOUNTINTOKEN": "10",
    "MAX_BASE_AMOUNT_PER_EXACT_TOKENS_TRANSACTION": "0.1",

    "BUYPRICEINBASE":  "10",
    "SELLPRICEINBASE": "15",
    "STOPLOSSPRICEINBASE": "8",
    "SLIPPAGE": "5",

    "MAXTOKENS": "0.1",
    "MOONBAG": "0",

    "RUGDOC_CHECK": "true",
    "BUYAFTER_XXX_SECONDS": "0",
    "WAIT_FOR_OPEN_TRADE": "true",

    "MAX_FAILED_TRANSACTIONS_IN_A_ROW": "2",    
    "MAX_SUCCESS_TRANSACTIONS_IN_A_ROW": "2",    
    "MULTIPLEBUYS": "false",
    "BUYCOUNT": "1",
    "ALWAYS_CHECK_BALANCE": "false",

    "LIQUIDITYCHECK": "false",
    "LIQUIDITYAMOUNT": "100",
    "LIQUIDITYINNATIVETOKEN": "true",
    "USECUSTOMBASEPAIR": "false",
    "BASESYMBOL": "WKCS",
    "BASEADDRESS": "0x4446fc4eb47f2f6586f9faab68b3498f86c07521",

    "SELLAMOUNTINTOKENS": "ALL",
    "HASFEES": "false",
    "GAS": "7",
    "BOOSTPERCENT": "30",
    "GASLIMIT": "1000000",
    "GASPRIORITY_FOR_ETH_ONLY": "1.5"
    
  }
]

```

#### Website:
https://alphadao.money
