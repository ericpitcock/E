<template>
  <div id="app">
    <e-logo />
  </div>
</template>

<script>
  import ELogo from '@/components/ELogo'

  export default {
    name: 'App',
    components: {
      ELogo
    }
  }
</script>

<style lang="scss">
  body {
    margin: 0;
  }
  #app {
    position: relative;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
