<template>
    <div>
      <transition name="fade">
        <h1 v-if="show">hello</h1>
      </transition>
      <button @click="showMessage">Mostar Mensagem</button>
    </div>
    
</template>

<script>
export default {
   data () {
    return {
      msg: 'Hello',
      show: false
    }
  },
  methods: {
      showMessage(){
        this.show = !this.show
      }
  }
}
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 1.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
