# vue-pegasus

VueJS component to connect vue applciations to the Pegasus Browser Wallet. 

Pegasus is a chrome extension that implements a wallet for the IOTA cryptocurrency. In addition, Pegasus injects the iotajs library allowing developers to interact with IOTA Tangle without paying attention on how to keep the seed safe.

[Visit Website](https://allemanfredi.github.io/pegasus-website/)
[Visit Repo](https://github.com/allemanfredi/PEGASUS)

## Install

```bash
npm install vue-pegasus
```

## Demo
![Demo](/assets/pegasus.gif)

## Setup


```bash
<script>
    import VuePegasus from 'vue-pegasus';
    export default {
        components: {
            VuePegasus,
        },
        data(){
            return {
                msg: "This is the vue-pegasus demo"
            }
        },
        methods:{
            onConnect(data){
                console.log('data:', data);
            }
        }
    }
</script>
```

```bash
<template>
  <div id="demo">
    <VuePegasus @onConnect="onConnect" />
  </div>
</template>
```