<script setup>
import ipadImg from '../pictures/ipad.png';
import bgLine from '../pictures/backgroundline.png';
import icon1 from '../pictures/в 17 раз.png';
import icon2 from '../pictures/в 17 раз-1.png';
import icon3 from '../pictures/в 17 раз-2.png';
import icon4 from '../pictures/в 17 раз-3.png';
import icon5 from '../pictures/в 17 раз-4.png';
import icon6 from '../pictures/в 17 раз-5.png';

const leftPros = [
  {
    title: 'Лучшие трейдеры и аналитики',
    text: 'Avantis проводит тщательный отбор всех сотрудников, HR совместно с нашим отделом андеррайтинга исследуют каждого кандидата по более 100 параметрам.',
    icon: icon1,
  },
  {
    title: 'Прозрачность',
    text: 'Мы предоставляем обширную документальную базу, где объяснены все юридические аспекты взаимодействия Avantis и ее партнеров.',
    icon: icon2,
  },
  {
    title: 'Удобство пользовательского интерфейса',
    text: 'Мы отказались от платформ. В связи с ненадобностью наших инвесторов непосредственно участвовать в торгах, команда Avantis создала Telegram-бот, который будет иметь все необходимые инструменты для контроля своих финансов.',
    icon: icon3,
  },
];

const rightPros = [
  {
    title: 'Низкие транзакционные издержки',
    text: 'Децентрализация процесса обмена крипто активами позволяет снизить комиссии, благодаря исключению посредников.',
    icon: icon4,
  },
  {
    title: 'Быстрые финансовые операции',
    text: 'Операции в блокчейне используются практически мгновенно, а системы смарт контрактов автоматизируют остальные процессы.',
    icon: icon5,
  },
  {
    title: 'Диверсификация рисков',
    text: 'Avantis Trust позволяет вложить свои средства не в одну стратегию, а в несколько. Таким образом распределение (диверсификация) дает возможность получать большую прибыль и снижает риск проседания капитала.',
    icon: icon6,
  },
];
</script>

<template>
  <section class="pros">
    <img class="pros__bg-line" :src="bgLine" alt="" />
    <div class="pros__content">
      <div class="pros__col pros__col--left">
        <div v-for="(item, idx) in leftPros" :key="`l-${idx}`" class="pros__item">
          <div class="pros__icon-wrap">
            <img class="pros__icon" :src="item.icon" :alt="item.title" />
          </div>
          <div>
            <div class="pros__item-title">{{ item.title }}</div>
            <div v-if="item.text" class="pros__item-text">{{ item.text }}</div>
          </div>
        </div>
      </div>

      <div class="pros__center">
        <div class="pros__tablet">
          <img class="pros__ipad" :src="ipadImg" alt="iPad" />
          <div class="pros__tablet-content">
            <span class="pros__accent-line"></span>
            <div class="pros__tablet-text">
              <span class="pros__tablet-line">Преимущества</span>
              <span class="pros__tablet-line">инвестирования</span>
              <span class="pros__tablet-line">вместе с</span>
              <span class="pros__tablet-brand">
                Avantis <span class="pros__tablet-brand-stroke">Trust</span>
              </span>
            </div>
          </div>
        </div>
      </div>

      <div class="pros__col pros__col--right">
        <div v-for="(item, idx) in rightPros" :key="`r-${idx}`" class="pros__item pros__item--right">
          <div class="pros__icon-wrap">
            <img class="pros__icon" :src="item.icon" :alt="item.title" />
          </div>
          <div>
            <div class="pros__item-title">{{ item.title }}</div>
            <div v-if="item.text" class="pros__item-text">{{ item.text }}</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
@import '../styles/Pros.css';
</style>
