<template>
  <div class="connection-status">
    <button v-if="connected" class="mdc-button" disabled>
      <i class="material-icons mdc-button__icon">
        bluetooth_connected
      </i>
    </button>
    <button v-if="!connected" class="mdc-button" v-on:click="connect">
      Connect
    </button>
  </div>
</template>

<script>
export default {
  name: 'Connection',
  data () {
    return {
      connected: false,
      radio_api: 'http://raspberrypi.local:8080'
    }
  },
  methods: {
    connect: function (event) {
      this.$http.get(this.radio_api + '/connect').then(response => {
        this.connected = true
      }).catch(error => {
        console.log(error)
      })
    }
  }
}
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
}
</style>
