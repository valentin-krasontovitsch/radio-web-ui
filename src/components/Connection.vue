<template>
  <div class="connection-status">
    <h1>{{ connectionStatus }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Connection',
  data () {
    return {
      connectionStatus: false
    }
  }
}
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
}
</style>
