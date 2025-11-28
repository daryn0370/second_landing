<script setup>
import appStore from '../pictures/appstore.png';
import googlePlay from '../pictures/googleplay.png';
import qrImage from '../pictures/qr.png';
import vectorIcon from '../pictures/Vector.png';
import phones from '../pictures/phones.png';
import coinBtc from '../pictures/Bitcoin-2 1.png';
import coinLtc from '../pictures/LiteCoin-3 1.png';
import coinXmr from '../pictures/Monero-1 1.png';
import supportIcon from '../pictures/support.png';
</script>

<template>
  <section class="home">
    <div class="home__content">
      <div class="home__left">
        <div class="home__brand">
          <span class="brand__title">Avantis</span>
          <span class="brand__subtitle">Trust</span>
        </div>
        <p class="home__text">
          Уникальный инвестиционный проект, объединяющий капитал частных инвесторов, знания и опыт
          лучшей команды аналитиков в сфере криптовалют.
        </p>
        <div class="home__actions">
          <div class="home__actions-list">
            <button class="home__btn" type="button">
              <img :src="appStore" alt="App Store" />
              <span class="home__btn-label">
                <span class="home__btn-sub">Загрузить в</span>
                <span class="home__btn-title">App Store</span>
              </span>
            </button>
            <button class="home__btn" type="button">
              <img :src="googlePlay" alt="Google Play" />
              <span class="home__btn-label">
                <span class="home__btn-sub">Загрузить в</span>
                <span class="home__btn-title">Google Play</span>
              </span>
            </button>
            <p class="home__qr-note">
              *Наведите камеру и<br />
              отсканируйте QR код чтобы<br />
              скачать приложение
            </p>
          </div>
          <div class="home__actions-qr">
            <div class="qr-card">
              <img class="qr-card__image" :src="qrImage" alt="QR код для скачивания приложения" />
              <div class="qr-card__footer">
                <img class="qr-card__icon" :src="vectorIcon" alt="Скачать на смартфон" />
                <span class="qr-card__label">Скачать на смартфон</span>
              </div>
            </div>
          </div>
        </div>
        <div class="home__stats">
          <div class="stat-col">
            <div class="stat stat--primary">
              <div class="stat__value stat__value--main">
                <span class="stat__currency">$</span>
                <span class="stat__number">100</span>
              </div>
              <div class="stat__label">инвестиции от</div>
            </div>
            <div class="stat stat--automation">
              <div class="stat__label stat__label--strong">Автоматизированная работа</div>
            </div>
          </div>
          <div class="stat-col">
            <div class="stat stat--feature">
              <div class="stat__label stat__label--strong">Удобный функционал бота</div>
            </div>
            <div class="stat stat--plans">
              <div class="stat__value stat__value--plans">12</div>
              <div class="stat__label stat__label--alt">инвестиционных планов</div>
            </div>
          </div>
          <div class="stat-col">
            <div class="stat stat--rate">
              <div class="stat__value stat__value--rate">0,3-1,8%</div>
              <div class="stat__label">доходность в день</div>
            </div>
          </div>
        </div>
      </div>

      <div class="home__visuals">
        <img class="home__phones" :src="phones" alt="Мобильное приложение Avantis Trust" />
        <img class="home__coin coin--btc" :src="coinBtc" alt="Bitcoin" />
        <img class="support-icon" :src="supportIcon" alt="Support" />
        <img class="home__coin coin--ltc" :src="coinLtc" alt="Litecoin" />
        <img class="home__coin coin--xmr" :src="coinXmr" alt="Monero" />
      </div>
    </div>
  </section>
</template>

<style scoped>
@import '../styles/HomePage.css';
</style>
