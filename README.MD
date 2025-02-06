# Etherspot Prime SDK - Flare Network Integration

## Overview

This repository demonstrates the integration of Etherspot's Prime SDK with Flare Network's Coston2 testnet, implementing Account Abstraction and Paymaster functionality.

## Prerequisites

### First, Etherspot Developer Account Setup

1. Create a developer account at [Etherspot Developer Portal](https://developer.etherspot.io)
2. Generate an API key and paste it in the example/payment.ts file as `apiKey` and `bundlerApiKey`
3. Navigate to the "Paymaster" tab
4. Top-up the Sponsor Address with CST2 using the [Coston2 faucet](https://coston2-faucet.flare.network)
5. Ensure you are on the "V1" tab and click "Deploy Contract"
6. You will see functionality to "Add whitelist v1" and "Add Stake v1" and "Deposit v1" which we will use later.

### Next, Clone repository and install dependencies

1. Clone the repository

```bash
git clone https://github.com/AmadiaFlare/etherspot-flare-paymaster.git
cd etherspot-flare-paymaster
```

2. Install dependencies

```bash
npm install
```

## Configuration

Create a `.env` file in the root directory with the following variables:

```env
WALLET_PRIVATE_KEY=your_private_key
CHAIN_ID=114
```

## Run the script

```bash
./node_modules/.bin/ts-node example/payment.ts
```

## Grab EtherspotWallet Address from terminal

Grab the address of the EtherspotWallet from the terminal output of the script:

```bash
address:  0x00000001E7Df0C823C76722286134a132c486368
EtherspotWallet address: 0x010000009E38b16eeB0b1318A60d5425f8b09486
```

## Whitelist the EtherspotWallet Address, Stake, and Deposit

1. Go back to the Etherspot Developer Portal and click on the "V1" tab
2. Click on "Add whitelist v1"
3. Paste the EtherspotWallet Address into the text field
4. Click "Add"
5. Click on "Add Stake v1"
6. Paste the EtherspotWallet Address into the text field
7. Click "Add"
8. Click on "Deposit v1"
9. Paste the EtherspotWallet Address into the text field
10. Click "Add"

## Manage Sponsorship

1. Go back to the Etherspot Developer Portal and click on the "Manage Sponsorship" tab
2. Click "Create Policy"
3. Follow the instructions to create a policy and enable both endpoints

## Run the script again

```bash
./node_modules/.bin/ts-node example/payment.ts
```

After running the script, you should see the transaction hash in the terminal output.
