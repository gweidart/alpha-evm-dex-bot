# Alpha KCC Dex Bot

<center><a href="https://ibb.co/XFXq7RT"><img src="https://i.ibb.co/XFXq7RT/bot-icon-1.png" alt="bot-icon-1" border="0"></a></center>

![](https://img.shields.io/github/last-commit/cusdt-LINK/alpha-kcc-dex-bot) ![](https://img.shields.io/github/forks/cusdt-LINK/alpha-kcc-dex-bot) ![](https://img.shields.io/github/stars/cusdt-LINK/alpha-kcc-dex-bot) ![](https://img.shields.io/github/license/cusdt-LINK/alpha-kcc-dex-bot) ![](https://img.shields.io/github/issues/cusdt-LINK/alpha-kcc-dex-bot?style=plastic)


- AlphaBot is an automated trading bot for the KCC DeFi ecosystem, however it is compatible with several other EVM chains. 

- AlphaBot has the ability to scan multiple trading pairs on a Dex, grab the price in realtime and make automated trading decisions based on user settings.

- AlphaBot uses web3.py and a custom wrapper to DIRECTLY interact with the smart contracts of the exchange. Thus avoiding slow web interfaces and Metamask, enabling AlphaBot to have the fastest throughput possible.  

- All of this is done LOCALLY on your machine. AlphatBot NEVER has access to read or store your private keys. 

- Private keys are encrypted with a password during initial bot setup.

#### **To use AlphaBot you must hold [ALPHA](https://alphadao.money) tokens (KCC) in your bot wallet.**

##### [**Buy ALPHA on AlphaSwap**](https://swap.alphadao.money/#/swap?outputCurrency=0x0490c1076552ed3c91876ead9f6a547b389e69d4)

### There are 3 subscription levels:

### **Tier 1: BETA** 
     
      46 ALPHA tokens (Slow speed - 6s between each price check.)

### **Tier 2: FROG KING** 

     69 ALPHA tokens (Medium speed - 3s between each price check.)

### **Tier 3: ALPHA** 

     90 ALPHA tokens (Super fast speed - no delay between each price check. All features unlocked and priority support.)


### Features
- Dex Limit Orders
- Dex Stop Loss
- Dex trailing stop loss
- real time trade notifications via Apprise. See below for more info!
- Mempool Sniping (AlphaBot is fast enough to snipe liquidity in the same block)
- Pink Sale Sniping 
- Accumulation Mode
- Take profit
- trailing take profit
- multi pair / multi wallet trading
- multi pair monitoring 
- Grid trading
- Automated Rug Doc
- Front run
- Liquidity check / monitoring
- Private key encryption
- Supports EIP 1559
- Custom exchange wrappers
- Trade any pair combination 
- Supports fully automated strategies (requires advanced configuration)

## Supported Dex:

- **AlphaSwap**
- **Kuswap**
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
- Various other Dexs on Harmony, Chronos, Metis 

## Fees:
AlphaBot does **NOT** and will **NEVER** charge its users trading fees. 


## Installation:

#### You can either simply run the precompiled .exe or run from source.

**You will need to have the latest version of [Pyhon](https://www.python.org/downloads/) & [Visual Studio](https://visualstudio.microsoft.com/fr/thank-you-downloading-visual-studio/?sku=Community&rel=17) installed.**

If you would still like to run the bot from source please follow the instructions below 👇 

**Clone this repo:**

```
git clone https://github.com/cusdt-LINK/alpha-kcc-dex-bot
```

**Install requirements:**

```
pip install -r requirements.txt 
this will install all the packages needed to run AlphaBot.
```

### **Enable ANSI colors in terminal:**
```
run the "EnableTerminalColors.bat" --> I highly suggest doing this. It makes reading the bot ui 10x easier. Certain bot actions are color coded.

```

**Open Windows Command Prompt or Powershell** (or Bash / Terminal on Linux / MacOs)

**Navigate to the AlphaBot folder:**

```
cd path\to\alphabot\folder 

```

**Run AlphaBot:**

```
python alphabot.py 

```

## Configuration

#### settings.json

```
[
	{
		"ALPHAWALLETPRIVATEKEY": "do not enter it manually, open the bot : it will encrypt it",
		"ALPHAWALLETADDRESS": "wallet address where you hold your ALPHA tokens",
		"WALLETADDRESS": "wallet address you want to trade on : can be different from ALPHA wallet",
		"PRIVATEKEY": "do not enter it manually, open the bot : it will encrypt it",
		"WALLETADDRESS2": "null",
		"PRIVATEKEY2": "null",
		"WALLETADDRESS3": "null",
		"PRIVATEKEY3": "null",
		"WALLETADDRESS4": "null",
		"PRIVATEKEY4": "null",
		"WALLETADDRESS5": "null",
		"PRIVATEKEY5": "null",
		"USECUSTOMNODE": "false",
		"CUSTOMNODE": "put your own node here",
		"EXCHANGE": "kuswap",
		"EXCHANGEVERSION": "2",
		"PREAPPROVE": "true",
		"UNLIMITEDSLIPPAGE": "false",
		"PASSWORD_ON_CHANGE": "false",
		"VERBOSE_PRICING": "true",
		"SLOW_MODE": "false"
	}
]

```

##### EXCHANGEVERSION:
```
Only applies to PancakeSwap. Otherwise just leave it alone. 
```
##### ALPHAWALLETPRIVATEKEY / PRIVATEKEY:
```
Private key of the wallet holding your ALPHA tokens. & Private key of the wallet the bot will trade to / from. 
	( not the 12 words seed phrase)
```
##### USECUSTOMNODE:
```
Set to "true" if you want to use a custom node.
```
##### CUSTOMNODE:
```
If you want to use a custom node, enter here your node's address in http, wss, or IPC
	example: (https://rpc-mainnet.kcc.network or  wss://rpc-mainnet.kcc.network )
```
##### PREAPPROVE:
```
Tells the bot to preapprove tokens on startup or not.
```
##### ENCRYPTPRIVATEKEYS:
```
Will be set automatically when you initialize the bot for the first time. 
```
##### UNLIMITEDSLIPPAGE:
```
Whethter or not you want the bot to completely bypass the slippage settings.
	If TRUE the bot will buy at any slippage.
	This can help avoid the "INSUFFICIENT_AMOUNT" error.
```
##### PASSWORD_ON_CHANGE:
```
Activate this option if you want the bot to ask your private key's password again when you update tokens.json
```
##### VERBOSE_PRICING:
```
Self explanatory. 
Default setting is "true". If you set this to "false", the bot will only show lines on the screen when the price updates.
```
##### SLOW_MODE:
```
Changes how often the bot queries for price. If "true" the bot will check every 0.5s.
(If you are using a public node provider, consider using SLOW-MODE if you are getting rate limited).
```

#### tokens.json

```
[
  {

    "ENABLED": "true",

    "SYMBOL": "ALPHA",
    "ADDRESS": "0x0490c1076552ed3c91876ead9f6a547b389e69d4",
    
    "KIND_OF_SWAP": "tokens",
    "BUYAMOUNTINBASE": "0.5",
    "BUYAMOUNTINTOKEN": "10",
    "MAX_BASE_AMOUNT_PER_EXACT_TOKENS_TRANSACTION": "0.5",

    "BUYPRICEINBASE":  "10",
    "SELLPRICEINBASE": "15",
    "STOPLOSSPRICEINBASE": "8",
    "SLIPPAGE": "25",

    "MAXTOKENS": "100",
    "MOONBAG": "0",

    "RUGDOC_CHECK": "false",
    "BUYAFTER_XXX_SECONDS": "0",
    "WAIT_FOR_OPEN_TRADE": "false",

    "MAX_FAILED_TRANSACTIONS_IN_A_ROW": "2",    
    "MAX_SUCCESS_TRANSACTIONS_IN_A_ROW": "null",    
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
    "GAS": "BOOST",
    "BOOSTPERCENT": "1",
    "GASLIMIT": "1000000",
    "GASPRIORITY_FOR_ETH_ONLY": "1.5"
    
  }
]

```
[========]

##### ENABLED:
```
Enable / Disable trading 
	(if false, the bot won't try to buy tokens)
```
##### SYMBOL:
```
Ticker of the token you want to trade.
	(example: ALPHA)
```
##### ADDRESS:
```
Contract address of the token you want to trade.
```
##### KIND_OF_SWAP:
```
1/ "KIND_OF_SWAP": "base"   --> you want to swap with an amount of Base tokens
	(example : I want to buy 1 KCS of ALPHA token)

2/ "KIND_OF_SWAP": "tokens"  --> you want to swap an exact amount of tokens
	(example : I want to buy 50 ALPHA tokens)
```
##### BUYAMOUNTINBASE:
```
(used with "KIND_OF_SWAP": "base")

Enter the amount of tokens in the base symbol that you want the bot to place a buy order with.
```
##### BUYAMOUNTINTOKEN:
```
(used with "KIND_OF_SWAP": "tokens")

Enter the amount of tokens that you want the bot to buy 
```
##### MAX_BASE_AMOUNT_PER_EXACT_TOKENS_TRANSACTION:
```
(used with "KIND_OF_SWAP": "tokens")
Enter the maximum amount of KCS / ETH / FTM... that you want the bot to use, if you're swapping per tokens. 
	(This option avoids you spending too much to buy the tokens you're trading for).
```
##### BUYPRICEINBASE:
```
(used with "KIND_OF_SWAP": "base")

Buy price of 1 token in the base symbol. (If the price of 1 token is < or = to this price, the bot will place a buy order.

If you want the bot to never buy, set BUYPRICEINBASE = 0
```
##### SELLPRICEINBASE: 
```
Sell price of 1 token in the base symbol : if the price of 1 token is > or = to this price, the bot will sell.

	(it will sell at the Market price, not at your price)

	If you want the bot to never sell, set SELLPRICEINBASE = 99999999
```
##### STOPLOSSPRICEINBASE:
```
Set your Stop Loss price in the base symbol . 
	Bot will sell if token price < STOPLOSSPRICEINBASE
```
##### SLIPPAGE:
```
Slippage you want to use (Denominated in %).
```
##### USECUSTOMBASEPAIR:
```
Must be TRUE or FALSE

"false" : the bot uses native token (KCS / ETH / MATIC / BNB / FTM / MATIC)  to trade.
 	You only need to hold this native token
"true" : bot uses the BASE pair you've entered.

	Please note: 
		By using this option, the bot needs to route your transaction through several routes 
		(Custom base token  --> Native token -->  Token you're sniping)
		and one of these routes could have low liquidity.
```
##### BASESYMBOL:
```
Symbol of the token you want to trade with if you selected USECUSTOMBASEPAIR = True
(in this example : I want to buy ALPHA with the KCS I have in my wallet)
```
##### BASEADDRESS:
```
Contract address of the token you want to trade with if you selected
	USECUSTOMBASEPAIR = True
```
##### LIQUIDITYINNATIVETOKEN:
```
Must be TRUE or FALSE.

TRUE: the bot will always route thru the NATIVE TOKEN liquidity pool. 
	(KCS / ETH / MATIC / BNB / FTM / MATIC) 

FALSE: the bot will always use the most direct route.
	(MIM / USDT / USDC / BUSD/etc.)

Use this option if you want to trade with liquidity in a stable coin. 
	(MIM / USDT / USDC / BUSD/etc.)

	Please note : When using the LIQUIDITYINNATIVETOKEN option, if you set up the
	wrong configuration, the bot will trade the wrong pair.
```
##### MAXTOKENS:
```
This parameter is used to make the bot stop buying once a certain balance is obtained.

The bot ALWAYS checks MAXTOKENS before placing a buy order. 
	(BALANCE >= MAXTOKENS, the bot will not place buy orders.)
```
##### MOONBAG:
```
Minimal amount of token you want to keep in your wallet.
	(If you don't want to keep any token, enter "0".)
```
##### RUGDOC_CHECK:
```
Call RugDoc's API to check if a contract is a honeypot.
	(Please take note RugDoc is not 100% reliable!)
```
https://rugdoc.io/honeypot/

##### BUYAFTER_XXX_SECONDS:
```
Ask the bot to wait for XXX seconds before placing a BUY order.
	(Useful if you want to avoid anti-bot protection.)
```
##### WAIT_FOR_OPEN_TRADE:
```
This option is for tokens where liquidity is added, but the dev team enables trading with a special function.
	("EnableTrading")

Several scenerios:
	 "WAIT_FOR_OPEN_TRADE": "true" --> the bot will scan pending transactions and wait for the price to move simultainiously.
	 "WAIT_FOR_OPEN_TRADE": "mempool" --> the bot will only scan pending transactions.
	 "WAIT_FOR_OPEN_TRADE": "true_after_buy_tx_failed" --> same as "true", but the bot will try to place BUY orders as soon as it detects liquidity, and launch wait_for_open_trade if txn fails.
	 "WAIT_FOR_OPEN_TRADE": "mempool_after_buy_tx_failed" --> same as "mempool", but the bot will try to place BUY orders as soon as it detects liquidity, and launch wait_for_open_trade if the txn fails.
	 "WAIT_FOR_OPEN_TRADE": "pinksale" --> PinkSale Sniping!


To make "WAIT_FOR_OPEN_TRADE": "true"  work, you need to snipe on the same liquidity pair that is being added.

Why? Because if you try to snipe in USDT and liquidity is in KCS, the price will move because of the volatility between USDT and KCS.

Examples:
	Liquidity is in KCS :
use LIQUIDITYINNATIVETOKEN = true / USECUSTOMBASEPAIR = false

	Liquidity is in USDT:
 use LIQUIDITYINNATIVETOKEN = false / USECUSTOMBASEPAIR = true / BASEADDRESS = 0x4446fc4eb47f2f6586f9faab68b3498f86c07521

Please note: there are many ways to enable trading, so it is very difficult for the bot to detect all scenerios. I will keep this function as updated as possible, so be sure to update your bot regularly. 
```
##### MAX_FAILED_TRANSACTIONS_IN_A_ROW:
```
Tells the bot to stop trading after XXX failed transactions.
```
##### MAX_SUCCESS_TRANSACTIONS_IN_A_ROW :
```
Tells the bot to stop trading after XXX success transactions
```
##### MULTIPLEBUYS:
```
AlphaBot is able to create up to 5 different trades with 5 different wallets at the same time! 
	(Useful for tokens where trading is limited to a maximum amount per wallet).
```
##### BUYCOUNT:
```
Must be set if MULTIPLEBUYS = true
	Tells the bot how many orders to place at once.
```
##### ALWAYS_CHECK_BALANCE:
```
To optimize AlphaBot's speed, by default, your balance is checked only initially at launch. 
Set this to TRUE, If you would like the bot to detect your wallet's balance while the bot is trading, to sell the tokens as quickly as possible
	(Please note: if TRUE, this does slightly decrease performace speed).
```
##### SELLAMOUNTINTOKENS:
```
Enter the amount of token that you would like the bot to sell.
```
##### HASFEES:
```
Select "TRUE" if you want to trade a token with additional fees.
	(automatic transfer to liquidity when you buy / additional taxes / rebase / etc.)
```
##### GAS / BOOSTPERCENT:
```
Two scenerios :
	Set your own fixed Gas price --> simply set Gas price in "GAS" parameter.
	("GAS": "200")

	Let the bot calculate Gas price via web3 in real time + BOOST.
	(recommended setting is 1000000 to avoid to "out of Gas" errors)
```
##### GASPRIORITY_FOR_ETH_ONLY:
```
This is for ETH only : sets Max Priority Gas.
	(The max priority fee, also referred to as the "miner tip", goes to the miner or validator, 	and incentivizes them to prioritize your transaction. Most often, the value you put in 		for "max priority fee" will be the amount you pay.)
```
##### MINIMUM_LIQUIDITY_IN_DOLLARS:
```
Use this option if you want the bot to set the minimal amount of liquidity you require in the Liquidity Pool before an order is placed. 
	(Please note liquidity amount is set in $).
```
##### PINKSALE_PRESALE_ADDRESS:
```
enter the PRESALE ADDRESS (not the token address) :

Please note: if you are sniping on PinkSale you must set:

	WAIT_FOR_OPEN_TRADE: "pinksale",
```

#### What is Apprise ?

It's an API that allows you to receive Push notifications via SMS / iMessage / in-browser / Telegram / Discord / ... basically everywhere!

--> you can now receive real-time notifications when Alpha Bot executes a trade!! <--

How to use it
1). Check out the Apprise Github. Read their documentation! : https://github.com/caronc/apprise#popular-notification-services
2). Configure your settings.json :
```
"ENABLE_APPRISE_NOTIFICATIONS": "true",
"APPRISE_PARAMETERS": [put your parameters here : you can put several notifications at the same time]
```

Example:

you are using a Windows computer and would like to receive notifications to your desktop
register with [PushSafer](https://www.pushsafer.com/) --> copy and paste your PushSafer key into settings.json & set "ENABLE_APPRISE_NOTIFICATIONS" to "true".
-->
```
settings.json :
"ENABLE_APPRISE_NOTIFICATIONS": "true",
"APPRISE_PARAMETERS": ["windows://", "psafers://eFhoOW0gh0vwvOCqDPlB"] // eFhoOW0gh0vwvOCqDPlB is your PushSafer key
```

Please note: Apprise notifications are **only enabled if you run the bot from source**. The precompiled .exe has apprise notifications disabled due to a bootloader compatibility issue. A fix for this will be released shortly : )
