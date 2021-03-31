<template>
  <div class="wrapper">
    <div class="v_carousel" :style="{'margin-left': '-' + (100 * counter) + '%'}">
      <second_component v-for="item in carousel_data"
                        :key="item.id"
                        :item_data="item"></second_component>
    </div>
    <button v-on:click="prevSlide">prev</button>
    <button v-on:click="nextSlide">next</button>
  </div>
</template>

<script>
import second_component from "@/components/second_component";

export default {
  name: "first_component",
  components: {
    second_component
  },
  props:{
  carousel_data:{
    type: Array,
    default: () => []
    }},
    data(){
    return{
      counter: 0,
    }
    },
    methods: {
    prevSlide: function(){
      if(this.counter > 0){
        this.counter--
        console.log(this.counter)
      }
    },
      nextSlide: function(){
      if(this.counter >= this.carousel_data.length - 1){
        this.counter = 0
      }
      else{
        this.counter++
        console.log(this.counter)
      }
      }
    }

}
</script>

<style scoped>
.wrapper{
  max-width: 225px;
  overflow: hidden;
  margin: 0 auto;

}
.v_carousel{
  display: flex;
  transition: all ease .5s;
}

</style>