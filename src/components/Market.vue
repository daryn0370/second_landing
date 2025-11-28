<template>
  <section class="market">
    <div class="market__coins">
      <img class="market__coin market__coin--ltc" src="../pictures/LiteCoin.png" alt="Litecoin" />
      <img class="market__coin market__coin--monero" src="../pictures/Monero.png" alt="Monero" />
      <img class="market__coin market__coin--btc" src="../pictures/Btc.png" alt="Bitcoin" />
    </div>
    <div class="market__content">
      <div class="market__left">
        <span class="market__title">Рынок криптовалют</span>
        <span class="market__subtitle">в 2021 году</span>
      </div>

      <div class="market__right">
        <p class="market__text">
          <span class="market__text-line">
            Темпы роста криптовалют ускоряются благодаря вовлечению профессиональных инвесторов с классических рынков.
          </span>
          <span class="market__text-line">
            Новым трендом является и то, что крупные компании и банки (например, Tesla, Square Inc, MicroStrategy Inc. и
            прочие) становятся держателями криптовалюты
          </span>
        </p>
      </div>

      <div class="market__stats">
        <div class="stat-card">
          <span class="stat-card__arrow"></span>
          <div class="stat-card__body">
            <span class="stat-card__label">БОЛЕЕ</span>
            <span class="stat-card__number">
              <span class="stat-card__currency">$</span>
              <span class="stat-card__value">100</span>
            </span>
            <span class="stat-card__suffix">МЛРД</span>
          </div>
          <span class="stat-card__foot">инвестировано в рынок криптовалют</span>
        </div>

        <div class="stat-card">
          <span class="stat-card__arrow stat-card__arrow--right"></span>
          <div class="stat-card__body">
            <span class="stat-card__label">на</span>
            <span class="stat-card__value stat-card__value--accent">240%</span>
          </div>
          <span class="stat-card__foot">выросла стоимость крипто активов в 2021 году</span>
        </div>

        <div class="stat-card">
          <span class="stat-card__arrow"></span>
          <div class="stat-card__body">
            <span class="stat-card__number">
              <span class="stat-card__currency">$</span>
              <span class="stat-card__value">2</span>
            </span>
            <span class="stat-card__suffix">ТРЛН</span>
          </div>
          <span class="stat-card__foot">общая стоимость цифровых активов</span>
        </div>

        <div class="stat-card stat-card--short">
          <span class="stat-card__arrow stat-card__arrow--right"></span>
          <div class="stat-card__body">
            <span class="stat-card__label">в</span>
            <span class="stat-card__value">17</span>
            <span class="stat-card__label">РАЗ</span>
          </div>
          <span class="stat-card__foot">вырос рынок криптовалют в 2021 году</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
@import '../styles/Market.css';
</style>
