<template>
    <div class="dogs">
        <h1>Dogs Page</h1>
        <ul class="breed-list">
            <li class="breed-container" v-for="breed in breeds" :key="breed.id">
                <h3>{{ breed.name }}</h3>
                <img :src="breed.image.url" alt="Image not available" />
                <router-link :to="`/dogs/${breed.id}`">Read More</router-link>
            </li>
        </ul>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import { RouterLink } from 'vue-router';
import axios from 'axios';
const breeds = ref([]);

components: {
  RouterLink
}


onMounted(async () => {
    try {
        const response = await axios.get("https://api.thedogapi.com/v1/breeds");
        breeds.value = response.data;
        console.log(response)
    } catch (error) {
        console.log(error)
    }
});
</script>

<style lang="scss" scoped>
.dogs {
  background-color: #FFFFE0;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.dogs h1 {
    text-align: center;
    margin-top: 3rem;
}

.breed-list {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    list-style: none;
}

.breed-container {
    margin: 3rem;
    width: auto;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.dogs img {
    height: 200px;
    width: auto;
    object-fit: cover;
}
</style>
