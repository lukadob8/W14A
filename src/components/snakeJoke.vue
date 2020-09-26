<template>
    <div>
        <h2> {{ joke }} </h2>
    </div>
</template>

<script>
    export default {
        name: "snake-joke",

        computed: {
            joke: function() {
                return this.$store.getters.snakeJoke
                
            }
        },
    }
</script>

<style scoped>

</style>