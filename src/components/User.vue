<template>
    <button type="button" @click="onClickAddAge">Increase Age</button>
    <button type="button" @click="onClickSubtractAge">Decrease Age</button>
    <p>The user is {{ age }} years old</p>

    <p>{{ ageDoubled }}</p>
    <p>{{ firstName }} <strong>"From User Template"</strong></p>
</template>

<script>
export default {
    name: "User",
    props: {
        age: {
            type: Number,
            required: true
        },
        firstName: {
            type: String,
        }
    },
    emits: ['add-age', 'subtract-age'],
    computed: {
        ageDoubled() {
            return this.age * 2
        }
    },
    methods: {
        onClickAddAge() {
            this.$emit('add-age', 3)
        },
        onClickSubtractAge() { // Change the method name to onClickSubtractAge
            this.$emit('subtract-age', 3)
        }
    }
}
</script>

<style lang="scss" scoped></style>
