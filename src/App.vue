<script setup>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <Header />
  <RouterView />
  <Footer />
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Exo+2:ital@1&family=Oswald&family=Rubik:wght@300&display=swap');
* {
  font-family: "Rubik", sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #6495ED;
  padding: 1rem;
}

.nav-img {
  height: 100px;
  width: 100px;
  border-radius: 100%;
  object-fit: cover;
  margin: auto 1rem;
}

.branding {
  display: flex;
  align-items: center;
  margin-left: 2rem;
}

.nav-h1 {
  margin-left: 2rem;
  font-size: 2.5rem;
  color: #333333;
}

.nav-routes {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  margin-right: 3rem;
}

.nav-link {
  margin: auto 2rem;
  color: #1b1b1b;
  font-size: 2.5rem;
  text-decoration: none;
}

.nav-link:hover {
  font-weight: bold;
  text-decoration: underline;
}

.main {
  background-color: #FFFFE0;
  height: auto;
}

.main h1 {
  text-align: center;
  padding: 3rem;
  font-size: 4rem;
  color: rgb(227, 45, 45);
}

.main h2 {
  margin: 1rem auto;
  text-align: center;
}

.main p {
  text-align: center;
  max-width: 50%;
  margin: 1rem auto;
}

.home-images {
  margin-top: 3rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.home-images img {
  height: 400px;
  width: 400px;
  object-fit: cover;
  margin: 1rem;
  border-radius: 100%;
}



footer {
  display: flex;
  align-items: center;
  justify-content: space-around;
  background-color: #6495ED;
  padding: 1rem;
}
</style>
