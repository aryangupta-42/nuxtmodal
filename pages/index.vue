<template>
  <div class="container">
    <Modal v-if="disp" :handler="close" :disp="disp" />
    <div class="btn" v-on:click="open">Open modal</div>
  </div>
</template>

<script>
import Modal from '~/components/modal.vue'

export default {
  components: {
    Modal
  },
  data () {
    return {
      disp: false
    }
  },
  methods: {
    open () {
      this.disp = true
    },
    close () {
      this.disp = false
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
  'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
}

.btn {
  height: 45px;
  width: 180px;
  border-radius: 5px;
  cursor: pointer;
  line-height: 45px;
  transition: 0.1s ease-out;
  text-transform: uppercase;
  font-weight: 700;
  border: 1px solid black;
}
.btn:hover {
  background-color: black;
  color: white;
}

</style>
