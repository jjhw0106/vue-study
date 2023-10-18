<template>
  <div>
    <app-header 
    v-bind:propsdata="str"
    v-on:renew="renewStr"
    >
    </app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
  components: {
    'app-header': AppHeader
  },

  data: function() {
    return {
      str:'DeadLine'
    }
  },

  methods: {
    renewStr: function() {
      this.str = 'new DeadLine';
    }
  }
}

</script>

<style>

</style>