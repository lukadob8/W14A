<template>
    <div>
        <h2> {{ joke }} </h2>
    </div>
</template>

<script>
    export default {
        name: "normal-joke",

        computed: {
            joke: function() {
                return this.$store.getters.normalJoke
                
            }
        },
        
    }
</script>

<style scoped>

</style>