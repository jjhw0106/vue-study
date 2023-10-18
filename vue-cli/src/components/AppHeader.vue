<template>
  <header>
    <h1>{{ propsdata }} 입니다.</h1>
    <button v-on:click="sendEvent">send</button>
  </header>
</template>

<script>
export default {
  data: function() {
    return {
      headLine:"머릿말"
    }
  },
  props: ['propsdata'],
  methods: {
    sendEvent: function() {
      this.$emit('renew')
    }
  }
}
</script>

<style>

</style>