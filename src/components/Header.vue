<script setup>
import googlePlay from '../pictures/googleplay.png';
import appStore from '../pictures/appstore.png';
</script>

<template>
  <header class="header">
    <div class="header__inner">
      <div class="header__brand">
        <span class="brand__title">Avantis</span>
        <span class="brand__subtitle">Trust</span>
      </div>

      <nav class="header__nav">
        <a href="#about">О нас</a>
        <a href="#advantages">Преимущества</a>
        <a href="#pricing">Тарифы и калькулятор</a>
        <a href="#features">Функционал</a>
        <a href="#referral">Реферальная программа</a>
      </nav>

      <div class="header__actions">
        <button class="lang-btn" type="button">EN</button>
        <button class="store-btn" type="button">
          <img :src="googlePlay" alt="Google Play" />
        </button>
        <button class="store-btn" type="button">
          <img :src="appStore" alt="App Store" />
        </button>
      </div>
    </div>
  </header>
</template>

<style scoped>
@import '../styles/Header.css';
</style>
