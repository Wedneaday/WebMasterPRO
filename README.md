<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WebMaster PRO — с нуля до фриланса за 1 месяц</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, Roboto, sans-serif;
            background: #0b0c10;
            color: #e5e5e5;
            line-height: 1.5;
            scroll-behavior: smooth;
            transition: background 0.3s, color 0.3s;
        }
        body.theme-light {
            background: #ffffff;
            color: #1a1a2e;
        }
        body.theme-light .card,
        body.theme-light .program-week,
        body.theme-light .quote,
        body.theme-light .project-example {
            background: #f5f5fa;
            border-color: #e0e0e0;
            color: #1a1a2e;
        }
        body.theme-light .card:hover,
        body.theme-light .program-week:hover,
        body.theme-light .project-example:hover {
            border-color: #7c3aed;
        }
        body.theme-light .btn {
            background: #7c3aed;
            color: white;
        }
        body.theme-light .btn:hover {
            background: #6d28d4;
        }
        body.theme-light .tag {
            background: #e9e9f0;
            color: #2d2d44;
        }
        body.theme-light .contact-block {
            background: #f0f0f8;
            border-color: #ddd;
        }
        body.theme-light footer {
            border-top-color: #e0e0e0;
            color: #666;
        }
        body.theme-light .discount-badge {
            background: #ede9fe;
            border-color: #7c3aed;
            color: #5b21b6;
        }
        body.theme-light .hero h1 {
            background: linear-gradient(135deg, #1a1a2e, #7c3aed);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }
        body.theme-light .price-info,
        body.theme-light .old-price {
            color: #555;
        }
        body.theme-light .new-price {
            color: #7c3aed;
        }
        .theme-switcher {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1000;
            background: rgba(0,0,0,0.6);
            backdrop-filter: blur(8px);
            border-radius: 40px;
            padding: 8px;
            cursor: pointer;
            border: 1px solid rgba(255,255,255,0.2);
            transition: 0.2s;
        }
        body.theme-light .theme-switcher {
            background: rgba(200,200,220,0.8);
            border-color: #ccc;
        }
        .theme-switcher:hover {
            transform: scale(1.05);
        }
        .theme-icon {
            font-size: 1.5rem;
            display: block;
            line-height: 1;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }
        .hero {
            padding: 80px 0 60px;
            text-align: center;
        }
        .hero h1 {
            font-size: clamp(2.5rem, 6vw, 4rem);
            font-weight: 800;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #fff, #a855f7);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 32px;
            color: #bbb;
        }
        body.theme-light .hero p {
            color: #3a3a55;
        }
        .btn {
            display: inline-block;
            background: #7c3aed;
            color: white;
            font-weight: 600;
            padding: 14px 40px;
            border-radius: 60px;
            text-decoration: none;
            transition: 0.2s;
        }
        .btn:hover {
            background: #6d28d4;
            transform: translateY(-2px);
            box-shadow: 0 10px 20px -5px rgba(124,58,237,0.5);
        }
        .price-block {
            margin: 40px 0 20px;
        }
        .old-price {
            font-size: 1.5rem;
            text-decoration: line-through;
            color: #888;
            margin-right: 15px;
        }
        .new-price {
            font-size: 2.7rem;
            font-weight: 800;
            color: #c084fc;
        }
        .price-info {
            font-size: 0.9rem;
            color: #aaa;
            margin-top: 10px;
        }
        .section {
            padding: 70px 0;
            border-top: 1px solid #1e1e2a;
        }
        body.theme-light .section {
            border-top-color: #e0e0e0;
        }
        .section h2 {
            font-size: 2rem;
            margin-bottom: 40px;
            text-align: center;
        }
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }
        .card {
            background: #111216;
            border-radius: 24px;
            padding: 28px;
            border: 1px solid #2a2d3a;
            transition: 0.2s;
            display: flex;
            flex-direction: column;
            height: 100%;
        }
        .card:hover {
            border-color: #7c3aed;
            transform: translateY(-4px);
        }
        .card h3 {
            font-size: 1.5rem;
            margin-bottom: 12px;
            color: #c084fc;
        }
        body.theme-light .card h3 {
            color: #7c3aed;
        }
        .program-week {
            margin-bottom: 30px;
            background: #0f1117;
            border-radius: 32px;
            padding: 24px;
        }
        .program-week h3 {
            color: #c084fc;
            margin-bottom: 15px;
            font-size: 1.4rem;
        }
        .tag {
            display: inline-block;
            background: #1f2230;
            padding: 6px 14px;
            border-radius: 40px;
            font-size: 0.8rem;
            margin-right: 10px;
            margin-bottom: 10px;
        }
        .project-example {
            background: #0a0c12;
            border-radius: 20px;
            padding: 20px;
            font-weight: 500;
            text-align: center;
            border: 1px solid #2a2d3a;
            transition: 0.2s;
        }
        .project-example:hover {
            border-color: #7c3aed;
            transform: translateY(-2px);
        }
        .quote {
            font-style: italic;
            background: #111216;
            padding: 30px;
            border-radius: 30px;
            border-left: 5px solid #7c3aed;
        }
        .contact-block {
            text-align: center;
            background: linear-gradient(145deg, #131520, #0a0c10);
            border-radius: 50px;
            padding: 50px 30px;
            margin: 40px 0;
            border: 1px solid #2a2d3a;
        }
        .discount-badge {
            background: #7c3aed20;
            border: 1px solid #7c3aed;
            border-radius: 60px;
            padding: 8px 20px;
            display: inline-block;
            margin-bottom: 20px;
        }
        footer {
            padding: 40px 0;
            text-align: center;
            border-top: 1px solid #1e1e2a;
            color: #777;
            font-size: 0.85rem;
        }
        @media (max-width: 800px) {
            .hero {
                padding: 50px 0;
            }
            .section {
                padding: 50px 0;
            }
            .new-price {
                font-size: 2rem;
            }
            .theme-switcher {
                top: 12px;
                right: 12px;
            }
        }
    </style>
</head>
<body>
    <div class="theme-switcher" id="themeSwitcher">
        <span class="theme-icon" id="themeIcon">🌙</span>
    </div>
    <div class="container">
        <div class="hero">
            <h1>WebMaster PRO <br>с нуля до фриланса за 1 месяц</h1>
            <p>Научись создавать веб-приложения, мини-сервисы и зарабатывать на заказах. Интенсив с реальными проектами и поддержкой.</p>
            <div class="price-block">
                <span class="old-price">70 000 ₽</span>
                <span class="new-price">50 000 ₽</span>
                <div class="price-info">* для выпускников марафона — 40 000 ₽</div>
            </div>
            <a href="https://t.me/KaMillaDasi" target="_blank" class="btn">📩 Записаться на курс</a>
        </div>
        <div class="section">
            <h2>🚀 Что вы получите</h2>
            <div class="grid-3">
                <div class="card">
                    <h3>💻 5 проектов в портфолио</h3>
                    <p>Менеджер задач, панель блогера, трекер расходов, чат, конструктор лендингов.</p>
                </div>
                <div class="card">
                    <h3>🧠 Навыки для фриланса</h3>
                    <p>Вёрстка, JavaScript, React, Node.js, MongoDB, работа с API, авторизация.</p>
                </div>
                <div class="card">
                    <h3>👥 Закрытый клуб</h3>
                    <p>Общение с куратором и участниками, ревью кода, помощь в поиске заказов.</p>
                </div>
            </div>
        </div>
        <div class="section">
            <h2>📅 Программа курса (4 недели, с самой базы)</h2>
            <div class="program-week">
                <h3>Неделя 1: Основы HTML и CSS (с нуля)</h3>
                <p>Теги, атрибуты, заголовки, списки, ссылки, картинки, формы, блочная модель, Flexbox, первая страница-визитка.</p>
                <div><span class="tag">HTML</span><span class="tag">CSS</span><span class="tag">Flexbox</span></div>
            </div>
            <div class="program-week">
                <h3>Неделя 2: Продвинутая вёрстка + адаптив</h3>
                <p>Grid, медиазапросы, анимации, препроцессоры, Pixel Perfect, деплой на GitHub Pages.</p>
                <div><span class="tag">Адаптивный лендинг</span></div>
            </div>
            <div class="program-week">
                <h3>Неделя 3: JavaScript — полный курс</h3>
                <p>Переменные, функции, DOM, события, fetch, async/await, API, localStorage.</p>
                <div><span class="tag">To-Do приложение</span><span class="tag">галерея с фильтрами</span></div>
            </div>
            <div class="program-week">
                <h3>Неделя 4: React + JavaScript (продвинутый уровень) + бэкенд (Node.js, MongoDB) + фриланс</h3>
                <p>Компоненты, хуки, роутинг, управление состоянием (Redux Toolkit), работа с API, создание REST API на Node.js, авторизация (JWT), базы данных, деплой, поиск заказов. Всё на чистом JavaScript (ES6+).</p>
                <div><span class="tag">менеджер задач на React</span><span class="tag">трекер расходов</span><span class="tag">чат с WebSocket</span><span class="tag">JavaScript (ES6+)</span></div>
            </div>
            <p style="margin-top: 20px; text-align: center;">🎯 Итог — полноценное приложение с авторизацией, базой данных и готовое портфолио из 5 проектов.</p>
        </div>
        <div class="section">
            <h2>🌟 Примеры мини-приложений, которые вы создадите</h2>
            <div class="grid-3">
                <div class="project-example">✅ Менеджер задач (To-Do) с авторизацией</div>
                <div class="project-example">📊 Панель управления блогера (статистика+посты)</div>
                <div class="project-example">💰 Трекер расходов с графиками</div>
                <div class="project-example">💬 Чат на WebSocket (обмен сообщениями)</div>
                <div class="project-example">📝 Конструктор простых лендингов</div>
                <div class="project-example">🔎 Поисковик по фильмам/книгам</div>
            </div>
        </div>
        <div class="section">
            <h2>💬 Отзывы учеников</h2>
            <div class="grid-3" style="grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));">
                <div class="quote">«После курса сделал трекер расходов и нашёл первого заказчика на фрилансе. Очень крутая поддержка!»<br>— Александр, студент</div>
                <div class="quote">«Материал структурирован, проекты реально короткие и понятные. Уже работаю веб-разработчиком.»<br>— Екатерина, frontend-стажёр</div>
            </div>
        </div>
        <div class="section">
            <h2>🎁 Бонусы для первых 10 учеников</h2>
            <div class="grid-3">
                <div class="card">
                    <h3>📘 Гайд по фрилансу</h3>
                    <p>Как найти первых клиентов, составить портфолио и провести переговоры.</p>
                </div>
                <div class="card">
                    <h3>🎨 Шаблоны КП</h3>
                    <p>Готовые коммерческие предложения и примеры портфолио для заказчиков.</p>
                </div>
                <div class="card">
                    <h3>⚡ Личная консультация</h3>
                    <p>30 минут со мной: разбор карьеры, ответы на вопросы.</p>
                </div>
            </div>
        </div>
        <div class="contact-block">
            <div class="discount-badge">🔥 Для участников марафона — 40 000 ₽</div>
            <h2 style="margin: 20px 0 10px;">Начни карьеру в IT сегодня</h2>
            <p>Осталось 5 мест на потоке. Пиши в Telegram, отвечу на вопросы, помогу с выбором.</p>
            <a href="https://t.me/KaMillaDasi" target="_blank" class="btn" style="margin-top: 30px;">✍️ Написать в Telegram</a>
            <p style="margin-top: 20px; font-size: 0.8rem;">Рассрочка без процентов — пишите, обсудим</p>
        </div>
        <footer>
            <p>© WebMaster PRO — обучение с нуля до фриланса за 1 месяц</p>
            <p style="margin-top: 8px;">Связь: <a href="https://t.me/KaMillaDasi" style="color:#c084fc;">t.me/KaMillaDasi</a></p>
        </footer>
    </div>
    <script>
        (function() {
            const THEME_KEY = 'webmaster_theme';
            const TIMESTAMP_KEY = 'webmaster_theme_ts';
            const EXPIRY_MS = 3 * 60 * 1000;

            function setTheme(theme, saveTime = true) {
                if (theme === 'light') {
                    document.body.classList.add('theme-light');
                    document.getElementById('themeIcon').textContent = '☀️';
                } else {
                    document.body.classList.remove('theme-light');
                    document.getElementById('themeIcon').textContent = '🌙';
                }
                if (saveTime) {
                    localStorage.setItem(THEME_KEY, theme);
                    localStorage.setItem(TIMESTAMP_KEY, Date.now().toString());
                }
            }

            function getStoredTheme() {
                const theme = localStorage.getItem(THEME_KEY);
                const timestamp = localStorage.getItem(TIMESTAMP_KEY);
                if (theme && timestamp) {
                    const now = Date.now();
                    const elapsed = now - parseInt(timestamp, 10);
                    if (elapsed < EXPIRY_MS) {
                        return theme;
                    } else {
                        localStorage.removeItem(THEME_KEY);
                        localStorage.removeItem(TIMESTAMP_KEY);
                    }
                }
                return null;
            }

            const storedTheme = getStoredTheme();
            if (storedTheme === 'light') {
                setTheme('light', false);
            } else {
                setTheme('dark', false);
            }

            const switcher = document.getElementById('themeSwitcher');
            switcher.addEventListener('click', () => {
                const isLight = document.body.classList.contains('theme-light');
                if (isLight) {
                    setTheme('dark');
                } else {
                    setTheme('light');
                }
            });
        })();
    </script>
</body>
</html>
