<template>
    <div>
        <div>{{score}}</div>
        <button @click="addPoint">+</button>
        <button @click="substractPoint">-</button>
    </div>
</template>

<script>

export default {
    props: ["score"],
    methods: {
        addPoint() {
            this.$emit("add-point")
            // return score + 1
        },
        substractPoint() {
            this.$emit("substract-point")
            // return score - 1
        }
    }
}
</script>

<style>

</style>