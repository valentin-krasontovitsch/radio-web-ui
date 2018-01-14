<template>
  <div id="app">
    <Connection/>
  </div>
</template>

<script>
import Connection from './components/Connection'
import * as mdc from 'material-components-web'

export default {
  name: 'App',
  components: {
    Connection
  },
  mounted: function () {
    mdc.autoInit()
  }
}
</script>

<style>
</style>
