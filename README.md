<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lova Shop UA - Магазин жіночого одягу</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5e6ff 0%, #ffe6f2 100%);
            color: #6a4a7a;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
        
        /* Шапка сайта */
        .header {
            text-align: center;
            margin-bottom: 25px;
            width: 100%;
            max-width: 500px;
        }
        
        .shop-title {
            font-size: 32px;
            font-weight: 800;
            margin-bottom: 8px;
            background: linear-gradient(45deg, #8a63a2, #f472b6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: 1px;
        }
        
        .shop-subtitle {
            font-size: 20px;
            color: #b38fd9;
            font-weight: 500;
        }
        
        /* Визитная карточка */
        .visiting-card {
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 30px;
            box-shadow: 0 15px 35px rgba(183, 148, 224, 0.25);
            width: 100%;
            max-width: 500px;
            padding: 40px 30px;
            text-align: center;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        
        /* ЛОГОТИП ВМЕСТО ФОТО ПРОФИЛЯ */
        .logo-container {
            width: 180px;
            height: 180px;
            margin: 0 auto 25px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .logo-svg {
            width: 100%;
            height: 100%;
            filter: drop-shadow(0 8px 20px rgba(183, 148, 224, 0.3));
            transition: transform 0.5s ease;
        }
        
        .logo-svg:hover {
            transform: rotate(5deg) scale(1.05);
        }
        
        /* Контактная информация */
        .contact-info {
            background: linear-gradient(to right, #e6d4ff, #ffd6f0);
            border-radius: 20px;
            padding: 22px;
            margin: 25px 0;
            font-size: 24px;
            font-weight: 700;
            color: #7e57a0;
            box-shadow: 0 5px 15px rgba(183, 148, 224, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .phone-icon {
            color: #7360f2;
            margin-right: 15px;
            font-size: 28px;
        }
        
        /* Facebook ссылка */
        .facebook-link {
            display: block;
            margin: 20px 0 30px;
            padding: 18px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 18px;
            text-decoration: none;
            color: #6a4a7a;
            font-size: 18px;
            border: 2px dashed #d8b4fe;
            transition: all 0.3s ease;
            word-break: break-all;
        }
        
        .facebook-link:hover {
            background: white;
            border-color: #8a63a2;
            border-style: solid;
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(183, 148, 224, 0.2);
        }
        
        .facebook-icon {
            color: #1877F2;
            margin-right: 10px;
            font-size: 22px;
        }
        
        /* Кнопки соцсетей */
        .buttons-container {
            display: flex;
            flex-direction: column;
            gap: 16px;
            margin-top: 30px;
        }
        
        .btn {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 19px 25px;
            border-radius: 20px;
            text-decoration: none;
            font-size: 19px;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 6px 16px rgba(0, 0, 0, 0.1);
        }
        
        .btn i {
            margin-right: 15px;
            font-size: 24px;
        }
        
        .instagram {
            background: linear-gradient(45deg, #f9c6e3, #d8b4fe);
            color: #7a4988;
        }
        
        .telegram {
            background: linear-gradient(45deg, #b5c6ff, #d0b5ff);
            color: #4a5fa8;
        }
        
        .viber-btn {
            background: linear-gradient(45deg, #c6b5ff, #e6b5ff);
            color: #5e4a9e;
        }
        
        .wholesale {
            background: linear-gradient(45deg, #a78bfa, #f472b6);
            color: white;
            font-size: 20px;
            margin-top: 8px;
        }
        
        .btn:hover {
            transform: translateY(-7px);
            box-shadow: 0 12px 25px rgba(183, 148, 224, 0.35);
        }
        
        .footer {
            margin-top: 40px;
            font-size: 15px;
            color: #b39bc8;
            padding-top: 25px;
            border-top: 1px solid #f0e6ff;
            text-align: center;
        }
        
        .contact-note {
            margin-top: 20px;
            font-size: 17px;
            color: #9f7fbf;
            font-style: italic;
        }
        
        /* Адаптивность */
        @media (max-width: 600px) {
            .header {
                margin-bottom: 20px;
            }
            
            .shop-title {
                font-size: 28px;
            }
            
            .shop-subtitle {
                font-size: 18px;
            }
            
            .visiting-card {
                padding: 30px 20px;
                border-radius: 25px;
            }
            
            .logo-container {
                width: 160px;
                height: 160px;
            }
            
            .contact-info {
                font-size: 20px;
                padding: 18px;
            }
            
            .phone-icon {
                font-size: 24px;
            }
            
            .facebook-link {
                font-size: 16px;
                padding: 15px;
            }
            
            .btn {
                padding: 17px 20px;
                font-size: 17px;
            }
        }
        
        /* Анимации */
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .floating {
            animation: float 5s ease-in-out infinite;
        }
    </style>
</head>
<body>

    <!-- ВИЗИТНАЯ КАРТОЧКА -->
    <main class="visiting-card">
        <!-- ЛОГОТИП В ЦЕНТРЕ (вместо фото профиля) -->
        <div class="logo-container">
            <svg class="logo-svg floating" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 200">
                <defs>
                    <linearGradient id="grad4" x1="0%" y1="0%" x2="100%" y2="100%">
                        <stop offset="0%" style="stop-color:#c9a8e6;stop-opacity:1" />
                        <stop offset="50%" style="stop-color:#f0b6e6;stop-opacity:1" />
                        <stop offset="100%" style="stop-color:#e6cfff;stop-opacity:1" />
                    </linearGradient>
                </defs>
                
                <circle cx="100" cy="100" r="90" fill="url(#grad4)"/>
                <circle cx="100" cy="100" r="80" fill="white"/>
                
                <text x="100" y="100" text-anchor="middle" fill="#8a63a2" font-family="Arial, sans-serif" font-size="24" font-weight="bold">
                    <tspan x="100" dy="-10">lova</tspan>
                    <tspan x="100" dy="25">shop</tspan>
                </text>
                
                <circle cx="100" cy="160" r="4" fill="#b38fd9"/>
                <circle cx="115" cy="160" r="4" fill="#d8b4fe"/>
                <circle cx="85" cy="160" r="4" fill="#f9c6e3"/>
            </svg>
        </div>

        <!-- ШАПКА С НАЗВАНИЕМ МАГАЗИНА -->
    <header class="header">
        <h1 class="shop-title">Lova_shop_ua</h1>
        <p class="shop-subtitle">Магазин жіночого одягу</p>
    </header>

        <!-- КОНТАКТНЫЙ НОМЕР -->
        <div class="contact-info" id="phone-number">
            <i class="fab fa-viber viber-icon"></i>
            +38 (097) 55-66-953
        </div>
        
        
        <p class="contact-note">Зв'яжіться зі мною зручним способом</p>
        
        <!-- КНОПКИ СОЦСЕТЕЙ -->
        <div class="buttons-container">
            <a href="https://www.instagram.com/lova_shop_ua?igsh=ZDJ1ZDdsNm1iZHRt" target="_blank" class="btn instagram">
                <i class="fab fa-instagram"></i> Instagram
            </a>
            
            <a href="https://t.me/lova_shop_ua_ukraine" target="_blank" class="btn telegram">
                <i class="fab fa-telegram"></i> Telegram
            </a>
            
            <a href="https://invite.viber.com/?g2=AQB3Wh8oWXzoflI%2BUgsoQC1cC%2BuSO0aRZP15UGO4K4JhZi2uWbX5XJ1iuu%2FLY5QB" class="btn viber-btn">
                <i class="fab fa-viber"></i>  Viber
            </a>
            
            <a href="https://invite.viber.com/?g2=AQA3na9Hc7rAplVUo2JJSiDC%2BiWLDvLZQ2zHVkHLFunjaGz1pfAG2TF0V941MPBu" class="btn wholesale">
                <i class="fas fa-boxes"></i> Для оптових покупців
            </a>
        </div>
        
        <!-- ФУТЕР -->
        <div class="footer">
            <p>© <span id="current-year">2024</span> Lova Shop UA. Всі права захищені.</p>
            <p style="margin-top: 8px; font-size: 14px; color: #c9a8e6;">Доставка по всій Україні та за кордон • Безкоштовна консультація</p>
        </div>
    </main>

    <script>
        // Анимация при загрузке
        document.addEventListener('DOMContentLoaded', function() {
            const card = document.querySelector('.visiting-card');
            const logo = document.querySelector('.logo-svg');
            
            // Начальное состояние
            card.style.opacity = '0';
            card.style.transform = 'scale(0.95) translateY(20px)';
            logo.style.opacity = '0';
            logo.style.transform = 'scale(0.5)';
            
            // Анимация появления
            setTimeout(() => {
                card.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
                card.style.opacity = '1';
                card.style.transform = 'scale(1) translateY(0)';
                
                logo.style.transition = 'opacity 1s ease, transform 1s ease';
                logo.style.opacity = '1';
                logo.style.transform = 'scale(1)';
            }, 300);
            
            // Обновление года
            document.getElementById('current-year').textContent = new Date().getFullYear();
            
            // Копирование номера телефона
            const phoneNumber = document.getElementById('phone-number');
            phoneNumber.style.cursor = 'pointer';
            
            phoneNumber.addEventListener('click', function() {
                const phone = '+380975566953';
                navigator.clipboard.writeText(phone).then(() => {
                    const originalHTML = this.innerHTML;
                    const originalBg = this.style.background;
                    
                    this.innerHTML = '<i class="fas fa-check"></i> Номер скопійовано!';
                    this.style.background = 'linear-gradient(to right, #a8ff78, #78ffd6)';
                    this.style.color = '#2d5a27';
                    
                    setTimeout(() => {
                        this.innerHTML = originalHTML;
                        this.style.background = originalBg;
                        this.style.color = '#7e57a0';
                    }, 2000);
                });
            });
            
            // Анимация логотипа при наведении
            logo.addEventListener('mouseenter', function() {
                this.style.animation = 'none';
                setTimeout(() => {
                    this.style.animation = 'float 5s ease-in-out infinite';
                }, 10);
            });
        });
    </script>
</body>
</html>
