<script setup lang="ts">
import Web3 from 'web3/dist/web3.min.js'
// import { Transaction } from "ethereumjs-tx";
import WalletConnectProvider from "@walletconnect/web3-provider";
const provider = new WalletConnectProvider({
  infuraId: "674ff902cf5046cdb78c754e27467a6f"
})

await provider.enable();
// const provider = new Web3.providers.HttpProvider(`https://rinkeby.infura.io/v3/${import.meta.env.VITE_APP_INFURA_KEY}`);
// const web3 = new Web3(provider);
// const addressFrom = "0x32a9E70324862ef7BF8bA7610AF701822ddE5364";
// const addressTo = "0x3D896D141dC4eEe51E829CcA7003939be20c280A";
// const transactionCount = await web3.eth.getTransactionCount(addressFrom);
// const newNonce = web3.utils.toHex(transactionCount);
// const txData = {
//   gasLimit: web3.utils.toHex(25000),
//   gasPrice: web3.utils.toHex(10e9),
//   to: addressTo,
//   from: addressFrom,
//   value: web3.utils.toHex(web3.utils.toWei("123", "wei"))
// }
// const transaction = new Transaction({...txData, nonce: newNonce}, {chain: "ropsten"})
// const privateKey = new Buffer(String(import.meta.env.PRIVATE_KEY), "hex");
// transaction.sign(privateKey)
// alert(newNonce);
</script>

<template>
  <main>
    aaa
  </main>
</template>
