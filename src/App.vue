<template>
    <div>
          <h3>Hey!</h3>
    <p><strong>{{ age }}</strong></p>
    <button type="button" @click="age++">Increase Age</button>
    <button type="button" @click="age--">Decrease Age</button>
    <greeting :age="age"></greeting>
    <user :age="age"></user>  
    </div>

</template>


<script>
import Greeting from "./components/Greeting.vue"
import User from "./components/User.vue"

export default {
    name: "App",
    components: {
        Greeting,
        User
    },
    data() {
        return {
            age: 20
        }
    }
}
</script>

<style lang="scss">
button {
    display: block;
    width: 150px;
    height: 30px;
    margin: 5px;
    border-radius: 5px;
    border-style: solid;
    border-width: 1px;
    color: brown;
    font-weight: 600;
}

div{
    display: flex;
    flex-direction: column;
    margin: auto;
}
</style>
