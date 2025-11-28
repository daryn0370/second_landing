<template>
  <section class="referral">
    <div class="referral__inner">
      <div class="referral__headline">
        <span class="referral__accent"></span>
        <h2 class="referral__title">Referral program</h2>
      </div>

      <div class="referral__content">
        <div class="referral__text">
          <p>
            Каждый из вас способен создать собственную команду, которая ориентирована на достижение высокого результата
            в направлении активного заработка онлайн. Вы можете создавать свою партнерскую структуру сразу после
            регистрации, при инвестировании минимального депозита.
          </p>
          <p>
            Реферальная программа Avantis Trust имеет линейную структуру на 4 уровня в глубину. Каждому партнеру
            сервиса присваивается статус, который зависит от общей суммы инвестиций. Статус влияет на размер
            выплачиваемых процентов.
          </p>
        </div>

        <div class="referral__statuses">
          <div class="referral__card">
            <div class="referral__card-title">Basic</div>
            <div class="referral__card-range">от $100<br />до $2000</div>
          </div>
          <div class="referral__card">
            <div class="referral__card-title">Standard</div>
            <div class="referral__card-range">от $2001<br />до $5000</div>
          </div>
          <div class="referral__card">
            <div class="referral__card-title">Premium</div>
            <div class="referral__card-range">от $5001<br />до $25 000</div>
          </div>
          <div class="referral__card referral__card--vip">
            <div class="referral__card-title">VIP</div>
            <div class="referral__card-range">от $25001<br />и выше</div>
          </div>
        </div>
      </div>

      <div class="referral__table">
        <div class="referral__table-head">
          <div>Уровни</div>
          <div>Basic</div>
          <div>Standart</div>
          <div>Premium</div>
          <div>VIP</div>
        </div>
        <div class="referral__table-row">
          <div>1</div>
          <div>8%</div>
          <div>10%</div>
          <div>12%</div>
          <div>14%</div>
        </div>
        <div class="referral__table-row">
          <div>2</div>
          <div>2%</div>
          <div>3%</div>
          <div>4%</div>
          <div>5%</div>
        </div>
        <div class="referral__table-row">
          <div>3</div>
          <div>1%</div>
          <div>1%</div>
          <div>2%</div>
          <div>2%</div>
        </div>
        <div class="referral__table-row">
          <div>4</div>
          <div></div>
          <div></div>
          <div>0,5%</div>
          <div>1%</div>
        </div>
      </div>

      <div class="partners">
        <div class="partners__table">
          <div class="partners__table-head">
            <div>Общий оборот структуры, $</div>
            <div>Partners Bonus</div>
          </div>
          <div class="partners__table-row">
            <div>100 000$</div>
            <div>5 000$</div>
          </div>
          <div class="partners__table-row">
            <div>250 000$</div>
            <div>15 000$</div>
          </div>
          <div class="partners__table-row">
            <div>500 000$</div>
            <div>40 000$</div>
          </div>
          <div class="partners__table-row">
            <div>750 000$</div>
            <div>75 000$</div>
          </div>
          <div class="partners__table-row">
            <div>1 000 000$</div>
            <div>150 000$</div>
          </div>
        </div>

        <div class="partners__info">
          <div class="partners__headline">
            <span class="referral__accent"></span>
            <h3 class="partners__title">Partners bonus</h3>
          </div>
          <p class="partners__text">
            Партнерская программа Avantis Trust позволяет каждому партнеру нашей компании получать дополнительный доход
            с общего оборота структуры. Привлекайте новых инвесторов и зарабатывайте вместе с ними до 150 000$ от
            общего оборота структуры.
          </p>
        </div>
      </div>

      <div class="start-bonus">
        <img class="start-bonus__badge" src="../pictures/Group 97.png" alt="Start Bonus Badge" />
        <div class="start-bonus__info">
          <div class="start-bonus__headline">
            <span class="referral__accent"></span>
            <h3 class="start-bonus__title">Start Bonus</h3>
          </div>
          <p>
            Компания ценит вашу оперативность. Поэтому в качестве дополнительного поощрения вы можете получить
            стартовый бонус. Это вознаграждение, которое зависит от суммы продаж в первой линии в течение 14-ти дней
            после вашего входа в компанию.
          </p>
          <p>
            Это единовременное вознаграждение, которое назначается, исходя из максимального достижения в указанный
            период. Ранговый бонус выплачивается на 15-й день после регистрации на платформе.
          </p>
        </div>

        <div class="start-bonus__table">
          <div class="start-bonus__head">
            <div>Объем депозитов в вашей первой линии, $</div>
            <div>Start Bonus</div>
          </div>
          <div class="start-bonus__row">
            <div>500$</div>
            <div>200$</div>
          </div>
          <div class="start-bonus__row">
            <div>15 000$</div>
            <div>500$</div>
          </div>
          <div class="start-bonus__row">
            <div>35 000$</div>
            <div>3 000$</div>
          </div>
          <div class="start-bonus__row">
            <div>50 000$</div>
            <div>5 000$</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
@import '../styles/Referral.css';
</style>
