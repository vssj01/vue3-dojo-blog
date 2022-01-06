<template>
  <div class="home">
    Home
    <p>Hello my name is {{name}} and age is {{age}}</p>
    <button @click="handleClick">Click Me</button>
    <button @click="age++">Add 1 to age</button>
    <br>
    <input type="text" v-model="name">

  </div>
</template>

<script>
// @ is an alias to /src
import {ref} from 'vue'

export default {
  name: 'Home',
  setup() {
    let name = ref('mario')
    let age = ref(30)

    const handleClick = () =>{
      name.value = 'luigi'
      age.value = 40  
    }

    return {name, age, handleClick}
  
  }
}
</script>
