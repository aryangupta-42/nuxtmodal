<template>
  <div class="modalContainer">
    <div class="modal" v-bind:style="anim">
      <Header title="Title goes here" :click="handler" />
      <div class="line" />
      <Body
        content="Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
      />
      <nuxt-child />
    </div>
  </div>
</template>

<script>
import Header from '~/components/modalHeader.vue'
import Body from '~/components/modalBody.vue'

export default {
  props: ['handler', 'disp'],
  components: {
    Header,
    Body
  },
  computed: {
    anim () {
      return {
        animation: `${this.mod} 0.2s`
      }
    }
  },
  data () {
    return {
      mod: 'none'
    }
  },
  mounted () {
    this.mod = 'fade'
  }
}

</script>
