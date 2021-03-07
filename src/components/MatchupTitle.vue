<template>
    <div>
        <span>{{ team1.name }}</span>
        vs
        <span>{{ team2.name }}</span>
    </div>
</template>

<script>

export default {
    props: ["team1", "team2"],
}
</script>

<style></style>