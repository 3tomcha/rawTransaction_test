<script setup lang="ts">
import Web3 from 'web3/dist/web3.min.js'
const provider = new Web3.providers.HttpProvider(`https://rinkeby.infura.io/v3/${import.meta.VITE_APP_INFURA_KEY}`);
const web3 = new Web3(provider);
console.log(web3);
</script>

<template>
  <main>
    aaa
  </main>
</template>
