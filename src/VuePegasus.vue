<template>
  <div id="vue-pegasus"></div>
</template>

<script>
export default {
  mounted() {
    setTimeout(async function() {
      if (window.iota) {
        console.log("window.iota", window.iota);
        try {
          const isConnected = await window.iota.connect();
          console.log("isConnected", isConnected);
        } catch (err) {
          console.log("err", err);
        }
      }
    }, 3000);
  }
};
</script>

<style>
#vue-metamask {
  display: none;
}
</style>