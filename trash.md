<div class="layout-container">
  <div class="layout-column">
    <div class="content-container">
      <nav>NAV</nav>
      <header>HEADER</header>
      <main>MAIN</main>
      <div>CONTENT</div> <!-- Бывшая SECTION -->
      <aside>ASIDE</aside>
      <footer>FOOTER</footer>
    </div>
  </div>
  <div class="layout-column">
    <div class="content-container">
      <nav>NAV</nav>
      <header>HEADER</header>
      <main>MAIN</main>
      <div>CONTENT</div> <!-- Бывшая SECTION -->
      <aside>ASIDE</aside>
      <footer>FOOTER</footer>
    </div>
  </div>
</div>

/* Общие стили для всей страницы */
body {
  background: #e6e6e6;
  margin: 0;
  font-family: Arial, sans-serif;
}

/* Контейнер макета */
.layout-container {
  display: flex;
  gap: 20px;
  padding: 20px;
  max-width: 1600px;
  margin: 0 auto;
}

/* Колонки (бывшие fourteen1 и fourteen2) */
.layout-column {
  flex: 1;
}

/* Стили для первого варианта сетки (числовые grid-области) */
.layout-column:first-child .content-container {
  display: grid;
  grid-template-columns: 200px 1fr 1fr;
  grid-template-rows: 100px 150px 150px 100px;
  gap: 10px;
  width: 800px;
  margin: 0 auto;
}

.layout-column:first-child header {
  grid-column: 2 / 4;
  grid-row: 1 / 2;
  background: #2196f3;
}

.layout-column:first-child nav {
  grid-column: 1 / 2;
  grid-row: 1 / 5;
  background: #2196f3;
}

.layout-column:first-child main {
  grid-column: 2 / 3;
  grid-row: 2 / 3;
  background: #2196f3;
}

.layout-column:first-child .content-block { /* бывшая section */
  grid-column: 2 / 3;
  grid-row: 3 / 4;
  background: #2196f3;
}

.layout-column:first-child aside {
  grid-column: 3 / 4;
  grid-row: 2 / 4;
  background: #2196f3;
}

.layout-column:first-child footer {
  grid-column: 2 / 4;
  grid-row: 4 / 5;
  background: #2196f3;
}

/* Стили для второго варианта сетки (именованные grid-области) */
.layout-column:last-child .content-container {
  display: grid;
  grid-template-columns: 200px 1fr 1fr;
  grid-template-rows: 100px 150px 150px 100px;
  gap: 10px;
  grid-template-areas:
    "nav header header"
    "nav main aside"
    "nav content-block aside"
    "nav footer footer";
  width: 800px;
  margin: 0 auto;
}

.layout-column:last-child header {
  grid-area: header;
  background: #2196f3;
}

.layout-column:last-child nav {
  grid-area: nav;
  background: #2196f3;
}

.layout-column:last-child main {
  grid-area: main;
  background: #2196f3;
}

.layout-column:last-child .content-block { /* бывшая section */
  grid-area: content-block;
  background: #2196f3;
}

.layout-column:last-child aside {
  grid-area: aside;
  background: #2196f3;
}

.layout-column:last-child footer {
  grid-area: footer;
  background: #2196f3;
}

/* Общие стили для всех элементов внутри контейнера */
.content-container > * {
  color: white;
  font-size: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 8px;
}