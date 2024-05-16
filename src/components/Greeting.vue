<template>
    <div>
        <h2 v-if="age> 25">{{ msg }}</h2>
        <p v-else>You must be 25 years or older to view this message.</p>
    </div>

</template>

<script>
export default {
    name: "Greeting",
    props:["age"],
    data() {
        return {
            msg: "Hello World!"
        }
    }
}
</script>

<style scoped lang="scss">
h2:hover {
color: darken(#cc4444, 15%);
}
</style>
