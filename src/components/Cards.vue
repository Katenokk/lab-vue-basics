<template>
  <div>
    <h1>{{title}}</h1>
    <p>{{description}}</p>
    <img :src="img" alt="quiero saber por que no se ve!!">
    
  </div>
</template>

<script>
export default {
    props: {
        title: String,
        description: String,
        img: String
    },
    data() {
        return {
            cards: [],
        }
    }
}
</script>

<style>

</style>