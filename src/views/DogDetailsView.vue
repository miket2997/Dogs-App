<template>
    <div>
        <h1>{{ breed }}</h1>
    </div>
</template>

<script setup props="breed">
import { onMounted } from "vue";

onMounted(() => {
    console.log(breed)
})
</script>

<style lang="scss" scoped>

</style>

