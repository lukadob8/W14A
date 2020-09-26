<template>
    <div id="grid">
        <button @click="getJoke"> Click for Joke </button>
        <div></div>
        <button @click="updateType('loud')"> Click for Loud Joke </button>
        <button @click="updateType('snake')"> Click for Snake Joke </button>
        <button @click="updateType('normal')"> Click for Normal Joke </button>
        <div></div>
       
    </div>
</template>

<script>
import axios from "axios"
    export default {
        name: "joke-button",
        
        methods: {
            
            getJoke: function() {
                axios.request({
                    url: "https://geek-jokes.sameerkumar.website/api?format=json",
                    method: "GET"
                }).then((response) => {
                    console.log(response)
                    this.$store.commit('updateJoke', response.data.joke)
                }).catch((error) => {
                    console.log(error)
                    this.joke = "ERROR"
                })
            },
            updateType: function(type) {
                this.$store.commit("updateJokeType", type)
            }
        },
    }
</script>

<style scoped>


</style>