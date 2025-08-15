<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Grid Layout</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <h2>Вариант 1 — grid-line</h2>
  <div class="container-lines">
    <div class="nav">NAV</div>
    <div class="header">HEADER</div>
    <div class="main">MAIN</div>
    <div class="aside">ASIDE</div>
    <div class="section">SECTION</div>
    <div class="footer">FOOTER</div>
  </div>

  <h2>Вариант 2 — grid-areas</h2>
  <div class="container-areas">
    <div class="nav">NAV</div>
    <div class="header">HEADER</div>
    <div class="main">MAIN</div>
    <div class="aside">ASIDE</div>
    <div class="section">SECTION</div>
    <div class="footer">FOOTER</div>
  </div>

</body>
</html>
body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
  padding: 20px;
}

h2 {
  margin-top: 40px;
}

.container-lines {
  display: grid;
  grid-template-columns: 200px 1fr 1fr;
  grid-template-rows: 100px 150px 150px 100px;
  gap: 10px;
  margin-bottom: 40px;
}

.container-areas {
  display: grid;
  grid-template-columns: 200px 1fr 1fr;
  grid-template-rows: 100px 150px 150px 100px;
  gap: 10px;
  grid-template-areas:
    "nav header header"
    "nav main aside"
    "nav section aside"
    "nav footer footer";
}

/* Элементы для первого контейнера (grid-line) */
.container-lines .nav {
  grid-column: 1 / 2;
  grid-row: 1 / 5;
}

.container-lines .header {
  grid-column: 2 / 4;
  grid-row: 1 / 2;
}

.container-lines .main {
  grid-column: 2 / 3;
  grid-row: 2 / 3;
}

.container-lines .aside {
  grid-column: 3 / 4;
  grid-row: 2 / 3;
}

.container-lines .section {
  grid-column: 2 / 3;
  grid-row: 3 / 4;
}

.container-lines .footer {
  grid-column: 2 / 4;
  grid-row: 4 / 5;
}

/* Элементы для второго контейнера (grid-areas) */
.container-areas .nav { grid-area: nav; }
.container-areas .header { grid-area: header; }
.container-areas .main { grid-area: main; }
.container-areas .aside { grid-area: aside; }
.container-areas .section { grid-area: section; }
.container-areas .footer { grid-area: footer; }

/* Общие стили для всех элементов */
.nav, .header, .main, .aside, .section, .footer {
  background: #3399ff;
  color: white;
  font-weight: bold;
  font-size: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 5px;
}
