<template>
  <div class="v-carousel-item">
    <img :src="require('../assets/' + item_data.img)">
    <p>{{item_data.text}}</p>

  </div>
</template>

<script>

export default {
  name: "second_component.vue",
  props:{
    item_data: {
      type: Object,
      default: () => {}
    }
  }
}
</script>

<style scoped>

</style>