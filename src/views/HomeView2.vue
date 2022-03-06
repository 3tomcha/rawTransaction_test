<script setup lang="ts">
import Web3 from 'web3/dist/web3.min.js'
import { Transaction } from "ethereumjs-tx";
import WalletConnectProvider from "@walletconnect/web3-provider";
const provider = new WalletConnectProvider({
  infuraId: "674ff902cf5046cdb78c754e27467a6f"
})

await provider.enable();
const web3 = new Web3(<any>provider);
const addressTo = "0x3D896D141dC4eEe51E829CcA7003939be20c280A";

const send = () => {
    const txData = {
    //   gasLimit: web3.utils.toHex(25000),
    //   gasPrice: web3.utils.toHex(10e9),
      to: addressTo,
      from: "0x32a9E70324862ef7BF8bA7610AF701822ddE5364",
      value: '1000000000000000'
    //   value: web3.utils.toHex(web3.utils.toWei("123", "wei"))
    }
  web3.eth.sendTransaction(txData).then((receipt) => {
    console.log(receipt);
  })
}

const getAccount = async() => {
    const accounts = await web3.eth.getAccounts();
    if(accounts) {
        console.log(accounts[0]);
        return accounts[0];
    }
}

// const transactionCount = await web3.eth.getTransactionCount(addressFrom).catch(err => {
//     console.error(err);
// });
// const newNonce = web3.utils.toHex(Number(transactionCount));


// const privateKey = new Buffer(String(import.meta.env.PRIVATE_KEY), "hex");
// transaction.sign(privateKey)
// alert(newNonce);
// const transaction = new Transaction({...txData, nonce: newNonce}, {chain: "ropsten"})
// const res = await web3.eth.sendTransaction(txData);
// console.log(res);
</script>


<template>
    <button @click="send">bbb</button>
</template>