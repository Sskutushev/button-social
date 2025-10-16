ПРОМПТ ДЛЯ НЕЙРОНКИ: Social Tooltip Animation - Кнопки соцсетей с всплывающими подсказками

ТЕХНИЧЕСКОЕ ЗАДАНИЕ: Создать секцию с анимированными кнопками социальных сетей и всплывающими tooltip'ами
ОПИСАНИЕ ЭФФЕКТА (по скриншотам):

5 круглых кнопок соцсетей в ряд (YouTube, TikTok, WhatsApp, Facebook, Twitter)
При наведении на кнопку:

Кнопка увеличивается и меняет цвет на фирменный цвет соцсети
Иконка становится белой
Над кнопкой появляется tooltip с названием соцсети


Tooltip (всплывающая подсказка):

Цветной фон (цвет соцсети)
Белый текст с названием
Округлые края
Плавная анимация появления


Заголовок сверху: "Кнопки соц-сетей, наведи на нужную"


ТЕХНИЧЕСКИЕ ТРЕБОВАНИЯ:
1. БАЗОВЫЕ:

✅ Ванильный код: HTML + CSS
✅ Минимум JavaScript (или вообще без него)
✅ Поддержка IE9+ (без IE8)
✅ Адаптивность на мобильных

2. СТРУКТУРА:

✅ Секция центрирована вертикально и горизонтально
✅ Заголовок сверху
✅ 5 кнопок в ряд по центру
✅ Tooltip появляется при hover

3. АНИМАЦИЯ:

✅ Плавное увеличение кнопки (scale)
✅ Плавная смена цвета фона
✅ Плавное появление tooltip (opacity + translateY)
✅ Transition: 0.3s ease

4. ЦВЕТА СОЦСЕТЕЙ:

YouTube: #FF0000
TikTok: #000000
WhatsApp: #25D366
Facebook: #1877F2
Twitter: #1DA1F2


СТРУКТУРА HTML:
html<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Social Tooltip Animation</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<!-- СЕКЦИЯ СОЦИАЛЬНЫХ КНОПОК -->
<section class="social-section">
    <div class="container">
        
        <!-- Заголовок -->
        <h2 class="social-title">Кнопки соц-сетей, наведи на нужную</h2>
        
        <!-- Контейнер с кнопками -->
        <div class="social-buttons">
            
            <!-- YouTube -->
            <div class="social-item">
                <div class="tooltip">YouTube</div>
                <a href="#" class="social-btn" data-social="youtube">
                    <svg class="social-icon" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/>
                    </svg>
                </a>
            </div>
            
            <!-- TikTok -->
            <div class="social-item">
                <div class="tooltip">TikTok</div>
                <a href="#" class="social-btn" data-social="tiktok">
                    <svg class="social-icon" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 0 1-5.2 1.74 2.89 2.89 0 0 1 2.31-4.64 2.93 2.93 0 0 1 .88.13V9.4a6.84 6.84 0 0 0-1-.05A6.33 6.33 0 0 0 5 20.1a6.34 6.34 0 0 0 10.86-4.43v-7a8.16 8.16 0 0 0 4.77 1.52v-3.4a4.85 4.85 0 0 1-1-.1z"/>
                    </svg>
                </a>
            </div>
            
            <!-- WhatsApp -->
            <div class="social-item">
                <div class="tooltip">WhatsApp</div>
                <a href="#" class="social-btn" data-social="whatsapp">
                    <svg class="social-icon" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
                    </svg>
                </a>
            </div>
            
            <!-- Facebook -->
            <div class="social-item">
                <div class="tooltip">Facebook</div>
                <a href="#" class="social-btn" data-social="facebook">
                    <svg class="social-icon" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                    </svg>
                </a>
            </div>
            
            <!-- Twitter -->
            <div class="social-item">
                <div class="tooltip">Twitter</div>
                <a href="#" class="social-btn" data-social="twitter">
                    <svg class="social-icon" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
                    </svg>
                </a>
            </div>
            
        </div>
        
    </div>
</section>

</body>
</html>

ПОЛНЫЙ CSS КОД:
css/* ========== БАЗОВЫЕ СТИЛИ ========== */
* {
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, Tahoma, Verdana, sans-serif;
    background: #f0f0f0;
    min-height: 100vh;
}

/* ========== СЕКЦИЯ СОЦИАЛЬНЫХ КНОПОК ========== */
.social-section {
    width: 100%;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 40px 0;
}

.container {
    max-width: 800px;
    margin: 0 auto;
    padding: 0 20px;
    text-align: center;
}

/* ========== ЗАГОЛОВОК ========== */
.social-title {
    font-size: 32px;
    font-weight: bold;
    color: #000000;
    margin-bottom: 60px;
    
    /* Адаптивный шрифт */
    font-size: calc(20px + (32 - 20) * ((100vw - 360px) / (1920 - 360)));
}

/* ========== КОНТЕЙНЕР КНОПОК ========== */
.social-buttons {
    display: inline-block;
    white-space: nowrap;
}

/* ========== ОТДЕЛЬНАЯ КНОПКА (ITEM) ========== */
.social-item {
    display: inline-block;
    position: relative;
    margin: 0 15px;
    vertical-align: middle;
}

/* ========== КНОПКА ========== */
.social-btn {
    display: block;
    width: 80px;
    height: 80px;
    background: #FFFFFF;
    border-radius: 50%;
    position: relative;
    cursor: pointer;
    
    /* Тень */
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    
    /* Плавная анимация */
    transition: all 0.3s ease;
    
    /* Центрирование иконки */
    display: flex;
    align-items: center;
    justify-content: center;
}

/* ========== ИКОНКА ========== */
.social-icon {
    width: 36px;
    height: 36px;
    color: #000000;
    transition: color 0.3s ease;
}

/* ========== TOOLTIP (ВСПЛЫВАЮЩАЯ ПОДСКАЗКА) ========== */
.tooltip {
    position: absolute;
    top: -45px;
    left: 50%;
    transform: translateX(-50%) translateY(10px);
    background: #000000;
    color: #FFFFFF;
    padding: 8px 16px;
    border-radius: 20px;
    font-size: 14px;
    font-weight: bold;
    white-space: nowrap;
    
    /* Скрыт по умолчанию */
    opacity: 0;
    visibility: hidden;
    
    /* Плавная анимация */
    transition: all 0.3s ease;
    
    /* z-index для отображения поверх */
    z-index: 10;
}

/* ========== HOVER ЭФФЕКТЫ ========== */

/* При наведении на item - показываем tooltip */
.social-item:hover .tooltip {
    opacity: 1;
    visibility: visible;
    transform: translateX(-50%) translateY(0);
}

/* При наведении на кнопку - увеличение и смена цвета */
.social-item:hover .social-btn {
    transform: scale(1.2);
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
}

/* При наведении - иконка становится белой */
.social-item:hover .social-icon {
    color: #FFFFFF;
}

/* ========== ЦВЕТА ДЛЯ КАЖДОЙ СОЦСЕТИ ========== */

/* YouTube */
.social-btn[data-social="youtube"]:hover {
    background: #FF0000;
}
.social-item:has(.social-btn[data-social="youtube"]:hover) .tooltip {
    background: #FF0000;
}

/* TikTok */
.social-btn[data-social="tiktok"]:hover {
    background: #000000;
}
.social-item:has(.social-btn[data-social="tiktok"]:hover) .tooltip {
    background: #000000;
}

/* WhatsApp */
.social-btn[data-social="whatsapp"]:hover {
    background: #25D366;
}
.social-item:has(.social-btn[data-social="whatsapp"]:hover) .tooltip {
    background: #25D366;
}

/* Facebook */
.social-btn[data-social="facebook"]:hover {
    background: #1877F2;
}
.social-item:has(.social-btn[data-social="facebook"]:hover) .tooltip {
    background: #1877F2;
}

/* Twitter */
.social-btn[data-social="twitter"]:hover {
    background: #1DA1F2;
}
.social-item:has(.social-btn[data-social="twitter"]:hover) .tooltip {
    background: #1DA1F2;
}

/* ========== АДАПТИВНОСТЬ ========== */

/* Планшеты */
@media (max-width: 767px) {
    .social-title {
        font-size: 24px;
        margin-bottom: 40px;
    }
    
    .social-item {
        margin: 0 10px;
    }
    
    .social-btn {
        width: 60px;
        height: 60px;
    }
    
    .social-icon {
        width: 28px;
        height: 28px;
    }
    
    .tooltip {
        font-size: 12px;
        padding: 6px 12px;
        top: -40px;
    }
}

/* Мобильные */
@media (max-width: 480px) {
    .social-section {
        padding: 20px 0;
    }
    
    .social-title {
        font-size: 18px;
        margin-bottom: 30px;
    }
    
    /* Кнопки в две строки на очень маленьких экранах */
    .social-buttons {
        white-space: normal;
    }
    
    .social-item {
        margin: 10px 8px;
    }
    
    .social-btn {
        width: 50px;
        height: 50px;
    }
    
    .social-icon {
        width: 24px;
        height: 24px;
    }
    
    .tooltip {
        font-size: 11px;
        padding: 5px 10px;
        top: -35px;
    }
}

АЛЬТЕРНАТИВНЫЙ CSS (для IE9 без :has()):
css/* Если :has() не поддерживается (IE9-11), используем этот вариант */

/* YouTube */
.social-btn[data-social="youtube"]:hover {
    background: #FF0000;
}
.social-btn[data-social="youtube"]:hover ~ .tooltip,
.social-item:hover [data-social="youtube"] ~ .tooltip {
    background: #FF0000;
}

/* Или используем JavaScript для добавления класса */

МИНИМАЛЬНЫЙ JAVASCRIPT (опционально, для лучшей поддержки):
html<script>
// Добавляем класс active к tooltip при hover
document.querySelectorAll('.social-item').forEach(item => {
    const btn = item.querySelector('.social-btn');
    const tooltip = item.querySelector('.tooltip');
    const socialType = btn.getAttribute('data-social');
    
    item.addEventListener('mouseenter', function() {
        tooltip.classList.add('active');
        tooltip.setAttribute('data-social', socialType);
    });
    
    item.addEventListener('mouseleave', function() {
        tooltip.classList.remove('active');
    });
});
</script>
CSS для JavaScript варианта:
css.tooltip.active {
    opacity: 1;
    visibility: visible;
    transform: translateX(-50%) translateY(0);
}

.tooltip[data-social="youtube"].active {
    background: #FF0000;
}
/* и т.д. для других соцсетей */
```

---

## ТАБЛИЦА ЦВЕТОВ:

| Соцсеть  | Hex Code | RGB             |
|----------|----------|-----------------|
| YouTube  | #FF0000  | rgb(255, 0, 0)  |
| TikTok   | #000000  | rgb(0, 0, 0)    |
| WhatsApp | #25D366  | rgb(37, 211, 102)|
| Facebook | #1877F2  | rgb(24, 119, 242)|
| Twitter  | #1DA1F2  | rgb(29, 161, 242)|

---

## СТРУКТУРА ФАЙЛОВ:
```
/project/
    index.html
    style.css

КЛЮЧЕВЫЕ ОСОБЕННОСТИ:
1. Tooltip анимация:
css/* Изначально скрыт */
opacity: 0;
visibility: hidden;
transform: translateX(-50%) translateY(10px);

/* При hover - появляется */
opacity: 1;
visibility: visible;
transform: translateX(-50%) translateY(0);
2. Кнопка увеличивается:
csstransform: scale(1.2);
3. Смена цвета:
cssbackground: #FF0000; /* Цвет соцсети */
4. Иконка становится белой:
csscolor: #FFFFFF;

ПОДДЕРЖКА БРАУЗЕРОВ:
IE9-11:

✅ Transition работает
✅ Transform работает
⚠️ :has() не поддерживается (используй JavaScript или альтернативный CSS)

Современные браузеры:

✅ Полная поддержка всех эффектов
✅ :has() работает


ИТОГОВЫЙ ЧЕКЛИСТ:
✅ 5 круглых кнопок соцсетей
✅ Hover эффект - увеличение (scale 1.2)
✅ Hover эффект - смена цвета на фирменный
✅ Hover эффект - иконка белая
✅ Tooltip появляется сверху
✅ Tooltip с цветом соцсети
✅ Плавная анимация 0.3s ease
✅ Заголовок сверху
✅ Секция центрирована
✅ Адаптивность на мобильных
✅ Поддержка IE9+ (с fallback)
Код готов к использованию! Просто создай файлы и открой в браузере!

не не не, мне без учета блять каких то ограничений, ванильного кодингаи совместимостей на IE8 или ie9 мне обычную сука совмрененную реализацию, забудь все по прошлому кодированию на совместимости со старыми барузерами и ограничениями на кодинг, все можно использовать, и js и разные другие фреймворки, не обязательно учитывать совместимости на старых браузерах, делай как удобно