<template>
    <!-- This is the template section where we define the structure of the component -->
    <div>
        <h3>Hey!</h3>
        <p><strong>{{ age }}</strong></p>

        <!-- This line renders the Greeting component and passes the age and firstName props to it -->
        <greeting :firstName="firstName" :age="age"></greeting>

        <!-- This line renders the User component and passes the age and firstName props to it -->
        <!-- It also listens for the 'add-age' and 'subtract-age' events emitted by the User component -->
        <user :firstName="firstName" :age="age" @add-age="updateAge" @subtract-age="age--"></user>
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
            age: 20,
            firstName: "John",
        }
    },
    methods: {
        // This method is called when the 'add-age' event is emitted by the User component
        // It updates the age property by adding the value passed as an argument
        updateAge(num) {
            return this.age += num
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

div {
    display: flex;
    flex-direction: column;
    margin: auto;
}
</style>