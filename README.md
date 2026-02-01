<!DOCTYPE html><html lang="uk">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Wedding of Vladyslav & Alina</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Montserrat:wght@300;400;500&display=swap" rel="stylesheet">
  <style>
    :root {
      --burgundy: #6b1f2b;
      --cherry: #8b2c3a;
      --milk: #f7f3ef;
      --champagne: #e6d3b1;
      --text-dark: #2b2b2b;
    }* { box-sizing: border-box; margin:0; padding:0; }
body { font-family: 'Montserrat', sans-serif; background: var(--milk); color: var(--text-dark); line-height:1.6; }
header { min-height:100vh; display:flex; align-items:center; justify-content:center; text-align:center; padding:40px 20px; background: radial-gradient(circle at top, #ffffff, var(--milk)); }
.hero { max-width:720px; }
.hero h1 { font-family:'Playfair Display', serif; font-size:42px; color:var(--burgundy); margin-bottom:16px; }
.hero p { font-size:16px; margin-bottom:32px; }
section { padding:80px 20px; text-align:center; }
section h2 { font-family:'Playfair Display', serif; font-size:32px; color:var(--cherry); margin-bottom:24px; }
.details p { font-size:17px; margin-bottom:10px; }
.dresscode { background: linear-gradient(180deg, #ffffff, var(--milk)); }
.colors { display:flex; justify-content:center; gap:12px; margin-top:24px; flex-wrap:wrap; }
.color { width:50px; height:50px; border-radius:50%; border:1px solid #ddd; }
.timer { font-size:24px; font-weight:500; color:var(--burgundy); margin-top:16px; }
.rsvp { background:var(--milk); }
form { max-width:400px; margin:0 auto; display:flex; flex-direction:column; gap:14px; }
select, button { padding:12px 14px; font-size:15px; border-radius:6px; border:1px solid #ccc; font-family:inherit; }
button { background:var(--burgundy); color:#fff; border:none; cursor:pointer; transition:0.3s; }
button:hover { background:var(--cherry); }
footer { padding:40px 20px; text-align:center; font-size:14px; color:#777; }

  </style>
</head>
<body>  <header>
    <div class="hero">
      <h1>Wedding of Vladyslav & Alina</h1>
      <p>З великою радістю запрошуємо вас розділити з нами один із найважливіших днів у нашому житті — день нашого весілля.</p>
    </div>
  </header>  <section class="details">
    <h2>Дата та місце</h2>
    <p><strong>13 червня 2026 року</strong></p>
    <p>Ресторан «Jozefina 2»</p>
  </section>  <section>
    <h2>Зворотний відлік</h2>
    <div id="timer" class="timer"></div>
  </section>  <section class="dresscode">
    <h2>Дрес-код</h2>
    <p>Ми будемо вдячні, якщо ви підтримаєте стиль нашого свята.<br>Елегантна класика та ніжні відтінки вітаються.</p>
    <div class="colors">
      <div class="color" style="background:#6b1f2b"></div>
      <div class="color" style="background:#8b2c3a"></div>
      <div class="color" style="background:#f7f3ef"></div>
      <div class="color" style="background:#ffffff"></div>
      <div class="color" style="background:#e6d3b1"></div>
    </div>
  </section>  <section class="rsvp">
    <h2>Підтвердження присутності</h2>
    <form>
      <select required>
        <option value="">Ви будете присутні?</option>
        <option>Так</option>
        <option>Ні</option>
      </select>
      <button type="submit">Підтвердити</button>
    </form>
  </section>  <footer>
    З любовʼю, Vladyslav & Alina
  </footer>  <script>
    const weddingDate = new Date('2026-06-13T00:00:00').getTime();
    const timerEl = document.getElementById('timer');

    setInterval(() => {
      const now = new Date().getTime();
      const diff = weddingDate - now;
      if(diff <= 0){ timerEl.textContent = 'Сьогодні наш особливий день!'; return; }
      const days = Math.floor(diff / (1000*60*60*24));
      const hours = Math.floor((diff / (1000*60*60)) % 24);
      const minutes = Math.floor((diff / (1000*60)) % 60);
      timerEl.textContent = `${days} днів ${hours} год ${minutes} хв`;
    },1000);
  </script></body>
</html>
