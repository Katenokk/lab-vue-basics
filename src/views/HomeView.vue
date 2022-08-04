<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Cards v-for="post in cards" :description="post.description" :title="post.title" :img="post.img">
    </Cards>
    
  </div>
  
</template>

<script>
// @ is an alias to /src

import Cards from "@/components/Cards.vue"


export default {
  name: 'HomeView',
  components: {
    
    Cards
  },
  data() {
    return {
      cards: [
        {
          title: "Titulo 1",
          description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium repellendus consectetur magnam accusamus.",
          img: "../assets/logo.png"
        },
         {
          title: "Titulo 2",
          description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium repellendus consectetur magnam accusamus.",
          img: "../assets/nio.jpg"
        },
         {
          title: "Titulo 3",
          description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium repellendus consectetur magnam accusamus.",
          img: "../assets/nio.jpg"
        }
      ]
    }
  }
}
</script>
