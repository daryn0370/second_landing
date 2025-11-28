<template>
  <section class="plan">
    <div class="plan__inner">
      <div class="plan__heading">
        <span class="plan__accent"></span>
        <div class="plan__title">
          <span class="plan__title-main">Инвестиционные планы</span>
          <span class="plan__brand">
            Avantis <span class="plan__brand-stroke">Trust</span>
          </span>
        </div>
      </div>

      <div class="plan__table">
        <div class="plan__row plan__row--head">
          <div class="plan__cell plan__cell--head">Депозит, USD</div>
          <div class="plan__cell plan__cell--head">50 дней,% за день</div>
          <div class="plan__cell plan__cell--head">100 дней,% в день</div>
          <div class="plan__cell plan__cell--head">365 дней,% в день</div>
        </div>
        <div class="plan__row">
          <div class="plan__cell">100-2000</div>
          <div class="plan__cell">0,3-0,4</div>
          <div class="plan__cell">0,5-0,6</div>
          <div class="plan__cell">0,7-0,8</div>
        </div>
        <div class="plan__row">
          <div class="plan__cell">2001-5000</div>
          <div class="plan__cell">0,4-0,5</div>
          <div class="plan__cell">0,7-0,8</div>
          <div class="plan__cell">0,9-1</div>
        </div>
        <div class="plan__row">
          <div class="plan__cell">5001-25000</div>
          <div class="plan__cell">0,6-0,7</div>
          <div class="plan__cell">1-1,1</div>
          <div class="plan__cell">1,2-1,3</div>
        </div>
        <div class="plan__row">
          <div class="plan__cell">25001 и выше</div>
          <div class="plan__cell">0,8-0,9</div>
          <div class="plan__cell">1,2-1,3</div>
          <div class="plan__cell">1,6-1,8</div>
        </div>
      </div>

      <div class="plan__note">
        *Первоначальные инвестиции возвращаются в конце срока действия тарифа
      </div>
      <div class="plan__cta">Рассчитай свою потенциальную прибыль</div>

      <div class="plan__calc">
        <div class="calc-card">
          <h3 class="calc-title">Выберите период</h3>
          <div class="calc-periods">
            <button
              v-for="period in periods"
              :key="period.value"
              :class="['calc-period', { 'calc-period--active': period.value === selectedPeriod }]"
              type="button"
              @click="selectPeriod(period.value)"
            >
              {{ period.label }}
            </button>
          </div>

          <div class="calc-input">
            <label class="calc-input__label">Введите сумму инвестиций</label>
            <input
              class="calc-input__field"
              type="text"
              :value="displayAmount"
              @input="onInputChange"
              inputmode="numeric"
            />
            <span class="calc-input__note">*Минимальная сумма инвестиций 100 USD</span>
          </div>

          <div class="calc-slider">
            <span class="calc-slider__label">Быстрый выбор суммы</span>
            <div class="calc-slider__value">{{ displayAmount }}</div>
            <input
              class="calc-slider__range"
              type="range"
              :min="minAmount"
              :max="maxAmount"
              :value="amount"
              @input="onSliderChange"
            />
            <div class="calc-slider__scale">
              <span>100 USD</span>
              <span>1 000 000 USD</span>
            </div>
          </div>

          <button class="calc-submit" type="button">Инвестировать сейчас</button>
        </div>

        <div class="calc-visual">
          <img src="../pictures/investnow.png" alt="Инвестиционный калькулятор" />
        </div>
      </div>

      <div class="plan__extra">
        <img class="plan__vector-line" src="../pictures/Vector 3.png" alt="" />
        <div class="plan__extra-body">
          <div class="plan__extra-left">
            <div class="plan__extra-heading">
              <span class="plan__extra-accent"></span>
              <span class="plan__extra-text">Все в одном месте</span>
            </div>

            <div class="plan__features plan__features--left">
              <div class="plan__feature">
                <img class="plan__feature-icon" src="../pictures/1 click.png" alt="1 клик" />
                <span class="plan__feature-text">Пополняй и выводи<br />в 1 клик</span>
              </div>
              <div class="plan__feature">
                <img class="plan__feature-icon" src="../pictures/control.png" alt="Контроль структуры" />
                <span class="plan__feature-text">Следи за оборотом<br />своей структуры</span>
              </div>
              <div class="plan__feature">
                <img class="plan__feature-icon" src="../pictures/refbonus.png" alt="Реферальные бонусы" />
                <span class="plan__feature-text">Получай реферальные<br />бонусы</span>
              </div>
            </div>
          </div>

          <div class="plan__extra-phone">
            <img src="../pictures/phone.png" alt="Мобильное приложение" />
          </div>

          <div class="plan__features plan__features--right">
            <div class="plan__feature">
              <img class="plan__feature-icon" src="../pictures/finance.png" alt="Управляй финансами" />
              <span class="plan__feature-text">Управляй своими<br />финансами</span>
            </div>
            <div class="plan__feature">
              <img class="plan__feature-icon" src="../pictures/support2.png" alt="Поддержка" />
              <span class="plan__feature-text">Поддержка 24/7</span>
            </div>
            <div class="plan__feature">
              <img class="plan__feature-icon" src="../pictures/notification.png" alt="Уведомления" />
              <span class="plan__feature-text">Ежедневные уведомления</span>
            </div>
            <div class="plan__feature">
              <img class="plan__feature-icon" src="../pictures/instruction.png" alt="Инструкции" />
              <span class="plan__feature-text">Подробные инструкции</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { computed, ref } from 'vue';

const minAmount = 100;
const maxAmount = 1000000;

const periods = [
  { label: '50 дней', value: 50 },
  { label: '100 дней', value: 100 },
  { label: '365 дней', value: 365 },
];

const selectedPeriod = ref(periods[0].value);
const amount = ref(252);

const displayAmount = computed(() => `${amount.value.toLocaleString('ru-RU')} USD`);

const clampAmount = (value) => Math.min(maxAmount, Math.max(minAmount, value));

const selectPeriod = (value) => {
  selectedPeriod.value = value;
};

const onSliderChange = (event) => {
  const newValue = Number(event.target.value) || minAmount;
  amount.value = clampAmount(newValue);
};

const onInputChange = (event) => {
  const raw = event.target.value || '';
  const numeric = parseInt(raw.replace(/\D+/g, ''), 10);
  amount.value = clampAmount(Number.isNaN(numeric) ? minAmount : numeric);
};
</script>

<style scoped>
@import '../styles/Plan.css';
</style>
