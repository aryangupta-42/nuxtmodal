<template>
  <div class="modalContainer">
    <div class="modal">
      <Header />
      <div class="line" />
      <Body />
    </div>
  </div>
</template>

<script>
import Header from '~/components/modalHeader.vue'
import Body from '~/components/modalBody.vue'

export default {
  components: {
    Header,
    Body
  }
}

</script>
