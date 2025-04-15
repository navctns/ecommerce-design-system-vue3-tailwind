<template>
  <header class="header">
    <div class="overlay has-fade"></div>
    <nav id="header-nav" class="flex container justify-between items-center">
      <a href="#" class="header__toggle">
        <!-- <img src="images/icon-menu.svg" alt=""> -->
        <span></span>
        <span></span>
        <span></span>
      </a>
      <div class="header__logo">
        <img src="images/logo.svg" alt="" />
      </div>
      <div class="header__links hide-for-mobile">
        <ul class="flex justify-between">
          <li>
            <a href="#">Collections <span class="arrow">▼</span></a>
            <ul class="navbar-menu-dropdown">
              <li><a href="#">Web Development</a></li>
              <li><a href="#">Mobile Apps</a></li>
              <li><a href="#">SEO</a></li>
            </ul>
          </li>
          <li><a href="#">Men</a></li>
          <li><a href="#">Women</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </div>
      <div class="flex flex-a-i-c header__user">
        <div class="header__cart flex flex-j-c-e">
          <img src="images/icon-cart.svg" alt="" />
        </div>
        <div class="header__avatar flex flex-a-i-c">
          <img src="images/image-avatar.png" alt="" />
        </div>
      </div>
    </nav>
    <!--Menu for mobile-->
    <div class="header__menu">
      <a href="#">Collections</a>
      <a href="#">Men</a>
      <a href="#">Women</a>
      <a href="#">About</a>
      <a href="#">Contact</a>
    </div>
  </header>
</template>
<script setup>
// import '../assets/styles/header.scss';
</script>
<style lang="scss" scoped>
// @import "../assets/styles/header.scss"
</style>
