<template>
  <div id="app">
    <first_component :carousel_data="sliderItems"></first_component>
  </div>
</template>


<script>

import first_component from './components/first_component'

export default {
  name: 'App',
  components: {
    first_component
  },
  data() {
    return {
      sliderItems: [
        {id : 1, name: 'first', img: 'first_first.jpg', text: 'Hello! My name is Nill. This product is so good! I recommend it!'},
        {id : 2, name: 'second', img: 'second_second.jpg', text: 'Hi, I am Sara. I bought this thing seven days ago and it is still work! Well done!'},
        {id : 2, name: 'second', img: 'third_third.jpg', text: 'Aloha! I am George. This purchase is fantastic, comfortable and qualitative! '},
        {id : 2, name: 'second', img: 'four_four.jpg', text: 'Hello! I love this thing so much. I use it every day! I really recommend it!'}
      ]
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
