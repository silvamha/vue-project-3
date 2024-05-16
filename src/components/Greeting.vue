<template>
    <div>
        <h2>{{ msg }}</h2>
    </div>

</template>

<script>
export default {
    name: "Greeting",
    data() {
        return {
            msg: "Hello World!"
        }
    }
}
</script>

<style scoped>
h2{
    color:red;
}
</style>

