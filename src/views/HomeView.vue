<script setup lang="ts">
import Web3 from 'web3/dist/web3.min.js'
const provider = new Web3.providers.HttpProvider(`https://rinkeby.infura.io/v3/${import.meta.env.VITE_APP_INFURA_KEY}`);
const web3 = new Web3(provider);
const sender = "0x32a9E70324862ef7BF8bA7610AF701822ddE5364";
const transactionCount = await web3.eth.getTransactionCount(sender);
const newNonce = web3.utils.toHex(transactionCount);
alert(newNonce);
</script>

<template>
  <main>
    aaa
  </main>
</template>
