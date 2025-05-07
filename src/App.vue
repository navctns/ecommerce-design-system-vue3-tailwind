<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import LogoSVG from "./assets/logo.svg?component";
// import TopNavbar from "./components/TopNavbar.vue";
import TopNavbarTailwindHeadlessUi from "./components/TopNavbarTailwindHeadlessUI.vue";
import TopNavbarTailwind from './components/navbar/TopNavbarTailwind.vue';
import TopNavbarModel1 from './components/navbar/model-1/TopNavbarModel1.vue';
import ProductCards from "./views/ProductCards.vue";
import CustomerRatingItem from './components/cards/CustomerRatingItem.vue';
import RadioButtonsTagDesign from './components/forms/radio-button-group/RadioButtonsTagDesign.vue';
import RadioButtonCircle from './components/forms/radio-button-group/RadioButtonCircle.vue';
import CountSetter from "./components/buttons/CountSetter.vue";
// import PriceRangeSelectorBar from './components/forms/price-range-selector/PriceRangeSelectorBar.vue';
import PriceRangeSlider from './components/forms/price-range-selector/PriceRangeSlider.vue';
import AccordionDesign1 from './components/accordion/AccordionDesign1.vue';
import SimplePagination from "./components/pagination/SimplePagination.vue";
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
  <div class="container px-8">
    <h5>Work Card Item</h5>
    <ProductCards></ProductCards>
    <h5>Rating Cards</h5>
    <div class="tab-slider flex overflow-x-auto pb-8 gap-6">
      <customer-rating-item></customer-rating-item>
    </div>
    <h5 class="mb-4">Button Designs</h5>
    <h6>Plain Button</h6>
    <button class="border border-gray-300 text-black text-sm px-6 py-2 rounded-full hover:bg-gray-100 transition">
      View All
    </button>
    <h6 class="mb-4">Dark Button</h6>
    <button class="bg-black text-white text-sm px-8 py-3 rounded-full hover:bg-gray-800 transition">
      Add to Cart
    </button>
    <h5 class="mb-4">Radio Buttons</h5>
    <h6>Radio buttons tag design</h6>
    <h6>Design 1</h6>
    <RadioButtonsTagDesign/>
    <h6>Design 2</h6>
    <RadioButtonCircle/>
    <h5>Count Setter</h5>
    <p>Sets count for an item to add to cart or checkout</p>
    <CountSetter/>
    <h5 class="my-3">Price Range Selector bar</h5>
    <!-- <price-range-selector-bar></price-range-selector-bar> -->
    <price-range-slider></price-range-slider>
    <h5>Accordions</h5>
    <div class="tab-slider flex overflow-x-auto pb-8 gap-6">
    <accordion-design-1>
      <ul>
        <li>Nike</li>
        <li>Addidas</li>
        <li>My Designation</li>
        <li>Bolerk</li>
      </ul>
    </accordion-design-1>

  </div>
  <h5 class="mt-4">Simple Pagination</h5>
  <SimplePagination/>
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
