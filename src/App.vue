<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import LogoSVG from "./assets/logo.svg?component";
// import TopNavbar from "./components/TopNavbar.vue";
import TopNavbarTailwindHeadlessUi from "./components/TopNavbarTailwindHeadlessUI.vue";
import TopNavbarTailwind from './components/navbar/TopNavbarTailwind.vue';
import TopNavbarModel1 from './components/navbar/model-1/TopNavbarModel1.vue';
import ProductItemCard from "./components/cards/ProductItemCard.vue";
</script>

<template>
  <top-navbar-tailwind></top-navbar-tailwind>
  <top-navbar-tailwind-headless-ui></top-navbar-tailwind-headless-ui>
  <top-navbar-model-1></top-navbar-model-1>
  <header>
    <div class="wrapper">

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
  <!-- <div class="grid grid-flow-col grid-rows-3 gap-4"> -->
  <div class="grid grid-cols-4 grid-rows-3 gap-4">
    <product-item-card class="col-span-1"></product-item-card>
    <product-item-card class="col-span-1"></product-item-card>
    <product-item-card class="col-span-4"></product-item-card>
    <product-item-card class="col-span-4"></product-item-card>
  </div>

  <RouterView />
</template>

<style scoped lang="scss">
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
$primary-color: #42b983;

.box {
  color: white;
  background-color: $primary-color;
}

</style>
