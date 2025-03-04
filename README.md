# Volume bot on EVM chains

## Supported chains
BSC, Ethereum mainnet, (Any EVM chains)

## Technology

Languange: Typescript, Solidity
Type: Bot

## How to use?

- You should install node modules by
```
npm i
```

- Edit some content in the `.env` file. I already sent you the project with `.env` file.

You should input your wallet address and privatekey there.
```
ETH_BASE_WALLET_ADDRESS="Your wallet address"
ETH_BASE_WALLET_ADDRESS="The private key of your base wallet"
```
There are rpc addresses in thge`.env` file and they are not paid version.

If you have good one you can replce them with yours.

- Then you should see the `config.json` file. I has the main configurations for running the bot. I added comments for your good understanding.
```
//Random amount for wallet.
export const amountMax = 0.003; //Ether balance
export const amountMin = 0.001; //Should be more than 0.001

//Fee balance that must be remaining in the wallet
export const fee = 0.001; //Must be greater than 0.001
```

I recommend that you should increase `fee` for the successful transaction. ex: 0.05, 0.06.

Before that you should have enough BNB in your base wallet.

For example if you set config values like this...
```
//Random time interval of buy and sell
export const maxInterval = 30000 //millisecond
export const minInterval = 5000//millisecond

//Random amount for wallet.
export const amountMax = 0.03; //Ether balance
export const amountMin = 0.01; //Should be more than 0.001

//Fee balance that must be remaining in the wallet
export const fee = 0.005; //Must be greater than 0.001

//Number of sub wallets.
export const subWalletNum = 20;

//ChainId : Sepolia, BSC, Ethereum
export const CHAINID:ChainId = ChainId.BSC;
```

Your wallet should have `(0.03 + 0.005) * 20 = 0.7 (BNB/ETH);

I Recommend that you should use much fee value like 0.01 so that you can gather funds if you have some error while running the bot.

While you are running the bot there will be a new json file to save the wallets you generated, so you can withdraw funds if there is a problem.

I will add automatic fund-gathering function later if you want.


Then you can run the bot
```
npm run dev
```


## Features
- Generating random wallets
- Funding wallets that will trade as real traders
- Random trade with funded wallets
- Gathering funds after work

## Example


https://github.com/user-attachments/assets/ac6e55f6-7ece-4cad-8dc7-883423c32f4e

## Tx links
https://bscscan.com/tx/0x581cda788080b52fbd5db8c4d3500c22a6c136a07b73e2311d1fc29330d48fe5
https://bscscan.com/tx/0x8c870cf1721c2c765b45d2b13731bf384ec2e8020552aafb0436c01ded98f2ab
https://bscscan.com/tx/0xb46d289c48d04dc6cc74849ecd9ef4fff6bf86aa3b16fc231d019b82c7789bc2

## Future
- Randomizing trading amount
- Randomizing trading frequency (Buy/Sell)
- Randomizing the pool

## How to contact
Telegram: [@midaBricoll](https://t.me/midaBricoll)

Twitter: [@dieharye](https://x.com/dieharye)
