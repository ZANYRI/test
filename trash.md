<section class="fourteen">
      <section class="fourteen1">
        <div class="container">
          <nav>NAV</nav>
          <header>HEADER</header>
          <main>MAIN</main>
          <section>SECTION</section>
          <aside>ASIDE</aside>
          <footer>FOOTER</footer>
        </div>
      </section>
      <section class="fourteen2">
        <div class="container">
          <nav>NAV</nav>
          <header>HEADER</header>
          <main>MAIN</main>
          <section>SECTION</section>
          <aside>ASIDE</aside>
          <footer>FOOTER</footer>
        </div>
      </section>
    </section>

.grid-layout .container {
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;  /* 3 колонки */
  grid-template-rows: auto auto 1fr auto;  /* 4 строки */
  gap: 10px;
  height: 100vh;
}

/* Размещение по линиям */
nav { grid-column: 1 / 2; grid-row: 1 / 4; }  /* Занимает 1-ю колонку, строки 1-3 */
header { grid-column: 2 / 4; grid-row: 1 / 2; }  /* Занимает колонки 2-4, 1-ю строку */
main { grid-column: 2 / 3; grid-row: 2 / 3; }  /* Основной контент */
section { grid-column: 2 / 3; grid-row: 3 / 4; }  /* Доп. секция */
aside { grid-column: 3 / 4; grid-row: 2 / 4; }  /* Сайдбар */
footer { grid-column: 1 / 4; grid-row: 4 / 5; }  /* Подвал на всю ширину */