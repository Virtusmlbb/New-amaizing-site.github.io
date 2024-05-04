<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Virtus</title>
    <style>
        /* Общие стили */
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background-color: #fff;
            color: #000;
            line-height: 1.6;
            font-size: 16px;
        }
        .top-panel {
            background-color: rgba(1, 33, 105, 0.8); /* Прозрачный цвет верхней панели */
            padding: 10px 0;
            text-align: center;
            color: #fff;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            transition: top 0.3s ease; /* Плавное изменение положения */
            display: none; /* По умолчанию скрыта */
        }
        .show-panel .top-panel {
            top: 0; /* Появление панели */
        }
        .main-content {
            padding-top: 60px; /* Увеличена верхняя отступ в основном контейнере */
        }
        header {
            background-color: #012169;
            padding: 20px 0;
            text-align: center;
            color: #fff;
            position: relative; /* Изменено на relative */
            z-index: 1001; /* Выше, чем .top-panel */
        }
        nav ul {
            list-style-type: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin-right: 20px;
        }
        nav ul li a {
            text-decoration: none;
            color: #fff;
            font-weight: bold;
            transition: color 0.3s ease;
        }
        nav ul li a:hover {
            color: #fbdc05;
        }
        main {
            text-align: center;
        }
        section {
            margin-bottom: 80px;
            padding: 40px;
            background-color: #f3f4f6;
            border-radius: 20px;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
            transition: transform 0.3s ease, opacity 0.3s ease;
            opacity: 0;
            transform: translateY(20px);
        }
        section:hover {
            transform: translateY(-10px);
        }
        h1, h2 {
            margin-top: 0;
            margin-bottom: 20px;
            color: #012169;
        }
        p {
            font-size: 18px;
            line-height: 1.8;
            color: #333;
        }
        button {
            background-color: #fbdc05;
            color: #012169;
            border: none;
            padding: 15px 30px;
            font-size: 20px;
            border-radius: 30px; /* Изменено на более круглые кнопки */
            cursor: pointer;
            transition: background-color 0.3s ease, color 0.3s ease, transform 0.3s ease; /* Добавлена анимация для кнопок */
        }
        button:hover {
            background-color: #012169;
            color: #fff;
            transform: scale(1.1); /* Увеличение размера при наведении */
        }
        footer {
            background-color: #012169;
            color: #fff;
            text-align: center;
            padding: 20px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        footer p {
            margin: 0;
        }
    </style>
</head>
<body>

<div class="top-panel"> <!-- Верхняя панель -->
    <nav>
        <ul>
            <li><a href="#home">Main page</a></li>
            <li><a href="#about">About us</a></li>
            <li><a href="#history">History</a></li>
            <li><a href="#prizepool">Prizepool</a></li>
            <li><a href="#products">Products</a></li>
            <li><a href="#contact">Contacts</a></li>
        </ul>
    </nav>
</div>

<header>
    <h1>Virtus</h1>
</header>

<main class="main-content">
    <section id="home">
        <h2>Welcome!</h2>
        <p>Welcome to Virtus, your ultimate destination for exotic experiences. Explore our site to learn more.</p>
        <button onclick="location.href='#history'">Learn More</button>
    </section>

    <section id="about">
        <h2>About Us</h2>
        <p>Learn more about Virtus and our mission to provide unforgettable experiences to our customers.</p>
    </section>

    <section id="history">
        <h2>Our History</h2>
        <p>Discover the fascinating history of Virtus and how we've grown over the years.</p>
    </section>

    <section id="prizepool">
        <h2>Prizepool</h2>
        <p>Learn about the incredible prizes and rewards you can win by participating in Virtus events.</p>
    </section>

    <section id="products">
        <h2>Our Products</h2>
        <p>Explore our wide range of high-quality products, designed to enhance your experiences.</p>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <p>Get in touch with us to learn more about our services or to provide feedback.</p>
        <button onclick="location.href='#home'">Back to Top</button>
    </section>
</main>

<footer>
    <p>&copy; 2024 Virtus. All rights reserved.</p>
</footer>

<script>
    // Показывать или скрывать верхнюю панель при прокрутке
    window.addEventListener('scroll', function() {
        const topPanel = document.querySelector('.top-panel');
        if (window.scrollY > 50) {
            topPanel.classList.add('show-panel');
        } else {
            topPanel.classList.remove('show-panel');
        }
    });
</script>

</body>
</html>
