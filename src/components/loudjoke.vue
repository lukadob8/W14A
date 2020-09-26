<template>
    <div>
        
        <h2> {{ loudJoke }} </h2>
    </div>
</template>

<script>
    export default {
        name: "loud-joke",
        
        computed: {
            loudJoke: function() {
                return this.$store.getters.loudJoke
                
            }
        },
    }
</script>

<style scoped>

</style>