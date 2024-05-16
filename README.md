# My notes

```shell
alex@DESKTOP-UKE5TJQ:~/challenge-0-simple-nft0-with-scaffold-eth-2$ yarn deploy
Nothing to compile
No need to generate any newer typings.
deploying "YourCollectible" (tx: 0xc77b6162607d7990a9d12fcb01454d40dcd7d1540d5846c3d5c3b681b3160b98)...: deployed at 0x75708c16FccC1b8f02E439eC734B771FDE4d84a3 with 1758855 gas
📝 Updated TypeScript contract definition file on ../nextjs/contracts/deployedContracts.ts
```

```shell
alex@DESKTOP-UKE5TJQ:~/challenge-0-simple-nft0-with-scaffold-eth-2$ yarn vercel
Vercel CLI 32.7.2
> > No existing credentials found. Please log in:
? Log in to Vercel github
> Success! GitHub authentication complete for opendev.top@gmail.com
? Set up and deploy “~/challenge-0-simple-nft0-with-scaffold-eth-2/packages/nextjs”? [Y/n] y
? Which scope do you want to deploy to? open-dev-top's projects
? Link to existing project? [y/N] n
? What’s your project’s name? challenge-0-simple-nft0
? In which directory is your code located? ./
Local settings detected in vercel.json:
- Install Command: yarn install
Auto-detected Project Settings (Next.js):
- Build Command: next build
- Development Command: next dev --port $PORT
- Output Directory: Next.js default
? Want to modify these settings? [y/N] n
🔗  Linked to open-dev-tops-projects/challenge-0-simple-nft0 (created .vercel)
🔍  Inspect: https://vercel.com/open-dev-tops-projects/challenge-0-simple-nft0/H3c2KtjWheELFwNH4ce6r8cLvhmt [2s]
✅  Preview: https://challenge-0-simple-nft0-op9zzic1i-open-dev-tops-projects.vercel.app [2s]
📝  Deployed to production. Run `vercel --prod` to overwrite later (https://vercel.link/2F).
💡  To change the domain or build command, go to https://vercel.com/open-dev-tops-projects/challenge-0-simple-nft0/settings
alex@DESKTOP-UKE5TJQ:~/challenge-0-simple-nft0-with-scaffold-eth-2$
```

```shell
alex@DESKTOP-UKE5TJQ:~/challenge-0-simple-nft0-with-scaffold-eth-2/packages/hardhat$ yarn hardhat test

  🚩 Challenge 0: 🎟 Simple NFT Example 🤓
    YourCollectible
          🛰  Contract deployed on 0x5FbDB2315678afecb367f032d93F642f64180aa3
      ✓ Should deploy the contract
      mintItem()
          🧑‍🏫 Tester Address:  0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266
          ⚖️ Starting balance:  0
          🔨 Minting...
          🏷  mint tx:  0x8bf55ecf838cb89538421f988d10eded7cd9e7f497bb3ccee39dc3a9168abe1c
          ⏳ Waiting for confirmation...
          🔎 Checking new balance:  0
        ✓ Should be able to mint an NFT
        ✓ Should track tokens of owner by index

·--------------------------------|---------------------------|-------------|-----------------------------·
|      Solc version: 0.8.17      ·  Optimizer enabled: true  ·  Runs: 200  ·  Block limit: 30000000 gas  │
·································|···························|·············|······························
|  Methods                                                                                               │
····················|············|·············|·············|·············|···············|··············
|  Contract         ·  Method    ·  Min        ·  Max        ·  Avg        ·  # calls      ·  eur (avg)  │
····················|············|·············|·············|·············|···············|··············
|  YourCollectible  ·  mintItem  ·          -  ·          -  ·     232597  ·            2  ·          -  │
····················|············|·············|·············|·············|···············|··············
|  Deployments                   ·                                         ·  % of limit   ·             │
·································|·············|·············|·············|···············|··············
|  YourCollectible               ·          -  ·          -  ·    1758855  ·        5.9 %  ·          -  │
·--------------------------------|-------------|-------------|-------------|---------------|-------------·

  3 passing (697ms)

alex@DESKTOP-UKE5TJQ:~/challenge-0-simple-nft0-with-scaffold-eth-2/packages/hardhat$
```

```shell
alex@DESKTOP-UKE5TJQ:~/challenge-0-simple-nft0-with-scaffold-eth-2$ yarn verify --network sepolia
failed to get chainId, falling back on net_version...
already verified: YourCollectible (0x75708c16FccC1b8f02E439eC734B771FDE4d84a3), skipping.
alex@DESKTOP-UKE5TJQ:~/challenge-0-simple-nft0-with-scaffold-eth-2$
```

```shell
alex@DESKTOP-UKE5TJQ:~/challenge-0-simple-nft0-with-scaffold-eth-2$ yarn vercel --prod
Vercel CLI 32.7.2
🔍  Inspect: https://vercel.com/open-dev-tops-projects/challenge-0-simple-nft0/6MgMwqQJz3z7yFkPUA1KNMTqgVHt [5s]
✅  Production: https://challenge-0-simple-nft0-ihmd41bxi-open-dev-tops-projects.vercel.app [5s]
╭──────────────────────────────────────────────────────────╮
│                                                          │
│           Update available! v32.7.2 ≫ v34.2.0            │
│   Changelog: https://github.com/vercel/vercel/releases   │
│         Run `yarn add vercel@latest` to update.          │
│                                                          │
╰──────────────────────────────────────────────────────────╯

alex@DESKTOP-UKE5TJQ:~/challenge-0-simple-nft0-with-scaffold-eth-2$
```

# 🚩 Challenge #0: 🎟 Simple NFT Example

![readme-0](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/375b7797-6839-43cd-abe5-fca94d88e300)

📚 This tutorial is meant for developers that already understand the [ 🖍️ basics ](https://www.youtube.com/watch?v=MlJPjJQZtC8).

🧑‍🏫 If you would like a more gentle introduction for developers, watch our 15 video [🎥 Web2 to Web3](https://www.youtube.com/playlist?list=PLJz1HruEnenAf80uOfDwBPqaliJkjKg69) series.

---

🎫 Create a simple NFT:

👷‍♀️ You'll compile and deploy your first smart contracts. Then, you'll use a template React app full of important Ethereum components and hooks. Finally, you'll deploy an NFT to a public network to share with friends! 🚀

🌟 The final deliverable is an app that lets users purchase and transfer NFTs. Deploy your contracts to a testnet, then build and upload your app to a public web server. Submit the url on [SpeedRunEthereum.com](https://speedrunethereum.com)!

💬 Meet other builders working on this challenge and get help in the [Challenge 0 Telegram](https://t.me/+Y2vqXZZ_pEFhMGMx)!

## Checkpoint 0: 📦 Environment 📚

Before you begin, you need to install the following tools:

- [Node (>= v18.17)](https://nodejs.org/en/download/)
- Yarn ([v1](https://classic.yarnpkg.com/en/docs/install/) or [v2+](https://yarnpkg.com/getting-started/install))
- [Git](https://git-scm.com/downloads)

Then download the challenge to your computer and install dependencies by running:

```sh
git clone https://github.com/scaffold-eth/se-2-challenges.git challenge-0-simple-nft
cd challenge-0-simple-nft
git checkout challenge-0-simple-nft
yarn install
```

> in the same terminal, start your local network (a local instance of a blockchain):

```sh
yarn chain
```

> in a second terminal window, 🛰 deploy your contract (locally):

```sh
cd challenge-0-simple-nft
yarn deploy
```

> in a third terminal window, start your 📱 frontend:

```sh
cd challenge-0-simple-nft
yarn start
```

📱 Open [http://localhost:3000](http://localhost:3000) to see the app.

---

## Checkpoint 1: ⛽️ Gas & Wallets 👛

> ⛽️ You'll need to get some funds from the faucet for gas.

![gas&wallet](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/912d0d4b-db34-49d3-bd7d-7ca0ab18eb66)

> 🦊 At first, **don't** connect MetaMask. If you are already connected, click **Disconnect**:

<p>
  <img src="https://github.com/scaffold-eth/se-2-challenges/assets/80153681/2c7a1e40-50ad-4c20-ba3e-a56eff4b892b" width="33%" />
  <img src="https://github.com/scaffold-eth/se-2-challenges/assets/80153681/1bcf9752-e8ae-4db6-a0a6-5dc774abe46c" width="33%" />
</p>

> 🔥 We'll use burner wallets on localhost.

> 👛 Explore how burner wallets work in 🏗 Scaffold-ETH 2 by opening a new incognito window and navigate to http://localhost:3000. You'll notice it has a new wallet address in the top right. Copy the incognito browser's address and send localhost test funds to it from your first browser (using the **Faucet** button in the bottom left):

![icognito&webBrowser](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/fd191447-a31f-4c03-a36f-936bfb70c2a1)

> 👨🏻‍🚒 When you close the incognito window, the account is gone forever. Burner wallets are great for local development but you'll move to more permanent wallets when you interact with public networks.

---

## Checkpoint 2: 🖨 Minting

> ✏️ Mint some NFTs! Click the **MINT NFT** button in the `My NFTs` tab.

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/74cf02f2-4c1b-4278-9841-f19f668e0b1e)

👀 You should see your NFTs start to show up:

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/63dabceb-ad42-4c09-8e5d-a0139939e32d)

👛 Open an incognito window and navigate to http://localhost:3000

🎟 Transfer an NFT to the incognito window address using the UI:

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/3b92fb50-d43f-48a8-838c-c45c443b0b71)

👛 Try to mint an NFT from the incognito window.

> Can you mint an NFT with no funds in this address? You might need to grab funds from the faucet to pay for the gas!

🕵🏻‍♂️ Inspect the `Debug Contracts` tab to figure out what address is the owner of YourCollectible?

🔏 You can also check out your smart contract `YourCollectible.sol` in `packages/hardhat/contracts`.

💼 Take a quick look at your deploy script `00_deploy_your_contract.js` in `packages/hardhat/deploy`.

📝 If you want to edit the frontend, navigate to `packages/nextjs/app` and open the specific page you want to modify. For instance: `/myNFTs/page.tsx`. For guidance on [routing](https://nextjs.org/docs/app/building-your-application/routing/defining-routes) and configuring [pages/layouts](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts) checkout the Next.js documentation.

---

## Checkpoint 3: 💾 Deploy your contract! 🛰

🛰 Ready to deploy to a public testnet?!?

> Change the defaultNetwork in `packages/hardhat/hardhat.config.ts` to `sepolia`.

![chall-0-hardhat-config](https://github.com/scaffold-eth/se-2-challenges/assets/55535804/f94b47d8-aa51-46eb-9c9e-7536559a5d45)

🔐 Generate a deployer address with `yarn generate`. This creates a unique deployer address and saves the mnemonic locally.

> This local account will deploy your contracts, allowing you to avoid entering a personal private key.

![chall-0-yarn-generate](https://github.com/scaffold-eth/se-2-challenges/assets/2486142/133f5701-e575-4cc2-904f-cdc83ae86d94)

👩‍🚀 Use `yarn account` to view your deployer account balances.

![chall-0-yarn-account](https://github.com/scaffold-eth/se-2-challenges/assets/2486142/c34df8c9-9793-4a76-849b-170fae7fd0f0)

⛽️ You will need to send ETH to your deployer address with your wallet, or get it from a public faucet of your chosen network.

> Some popular faucets are [https://sepoliafaucet.com/](https://sepoliafaucet.com/) and [https://www.infura.io/faucet/sepolia](https://www.infura.io/faucet/sepolia)

> ⚔️ Side Quest: Keep a 🧑‍🎤 [punkwallet.io](https://punkwallet.io) on your phone's home screen and keep it loaded with testnet eth. 🧙‍♂️ You'll look like a wizard when you can fund your deployer address from your phone in seconds.

🚀 Deploy your NFT smart contract with `yarn deploy`.

> 💬 Hint: You can set the `defaultNetwork` in `hardhat.config.ts` to `sepolia` **OR** you can `yarn deploy --network sepolia`.

---

## Checkpoint 4: 🚢 Ship your frontend! 🚁

> ✏️ Edit your frontend config in `packages/nextjs/scaffold.config.ts` to change the `targetNetwork` to `chains.sepolia` :

![chall-0-scaffold-config](https://github.com/scaffold-eth/se-2-challenges/assets/55535804/3b50c7a7-b9cc-4af3-ab2a-11be4f5d2235)

> You should see the correct network in the frontend (http://localhost:3000):

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/50eef1f7-e1a3-4b3b-87e2-59c19362c4ff)

> 🦊 Since we have deployed to a public testnet, you will now need to connect using a wallet you own or use a burner wallet. By default 🔥 `burner wallets` are only available on `hardhat` . You can enable them on every chain by setting `onlyLocalBurnerWallet: false` in your frontend config (`scaffold.config.ts` in `packages/nextjs/`)

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/f582d311-9b57-4503-8143-bac60346ea33)

> 💬 Hint: For faster loading of your transfer page, consider updating the `fromBlock` passed to `useScaffoldEventHistory` in [`packages/nextjs/app/transfers/page.tsx`](https://github.com/scaffold-eth/se-2-challenges/blob/challenge-0-simple-nft/packages/nextjs/app/transfers/page.tsx#L12) to `blocknumber - 10` at which your contract was deployed. Example: `fromBlock: 3750241n` (where `n` represents its a [BigInt](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt)). To find this blocknumber, search your contract's address on Etherscan and find the `Contract Creation` transaction line.

🚀 Deploy your NextJS App

```shell
yarn vercel
```

> Follow the steps to deploy to Vercel. Once you log in (email, github, etc), the default options should work. It'll give you a public URL.

> If you want to redeploy to the same production URL you can run `yarn vercel --prod`. If you omit the `--prod` flag it will deploy it to a preview/test URL.

⚠️ Run the automated testing function to make sure your app passes

```shell
yarn test
```

#### Configuration of Third-Party Services for Production-Grade Apps.

By default, 🏗 Scaffold-ETH 2 provides predefined API keys for popular services such as Alchemy and Etherscan. This allows you to begin developing and testing your applications more easily, avoiding the need to register for these services.  
This is great to complete your **SpeedRunEthereum**.

For production-grade applications, it's recommended to obtain your own API keys (to prevent rate limiting issues). You can configure these at:

- 🔷`ALCHEMY_API_KEY` variable in `packages/hardhat/.env` and `packages/nextjs/.env.local`. You can create API keys from the [Alchemy dashboard](https://dashboard.alchemy.com/).

- 📃`ETHERSCAN_API_KEY` variable in `packages/hardhat/.env` with your generated API key. You can get your key [here](https://etherscan.io/myapikey).

> 💬 Hint: It's recommended to store env's for nextjs in Vercel/system env config for live apps and use .env.local for local testing.

---

## Checkpoint 5: 📜 Contract Verification

You can verify your smart contract on Etherscan by running (`yarn verify --network network_name`) :

```shell
yarn verify --network sepolia
```

> It is okay if it says your contract is already verified. Copy the address of YourCollectable.sol and search it on sepolia Etherscan to find the correct URL you need to submit this challenge.

## Checkpoint 6: 💪 Flex!

👩‍❤️‍👨 Share your public url with a friend and ask them for their address to send them a collectible :)

![gif](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/547612f6-97b9-4eb3-ab6d-9b6d2c0ac769)

## ⚔️ Side Quests

### 🐟 Open Sea

> 🐃 Want to see your new NFTs on Opensea? Head to [Testnets Opensea](https://testnets.opensea.io/)

> 🎫 Make sure you have minted some NFTs on your Vercel page, then connect to Opensea using that same wallet.

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/c752b365-b801-4a02-ba2e-62e0270b3795)

> You can see your collection of shiny new NFTs on a testnet!

(It can take a while before they show up, but here is an example:) https://testnets.opensea.io/assets/sepolia/0x17ed03686653917efa2194a5252c5f0a4f3dc49c/2

---

> 🏃 Head to your next challenge [here](https://github.com/scaffold-eth/se-2-challenges).

> 💬 Problems, questions, comments on the stack? Post them to the [🏗 scaffold-eth developers chat](https://t.me/joinchat/F7nCRK3kI93PoCOk)
