<template>
  <div class="headerContainer">
    <div class="headerText">
      {{ title }}
    </div>
    <div class="headerBtn" v-on:click="click">
      X
    </div>
  </div>
</template>

<script>
export default {
  props: ['title', 'click']
}
</script>
