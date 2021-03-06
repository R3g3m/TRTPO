
# Требования к проекту 
___
## Содержание
1. [Введение](#1)
1. [Требования пользователя](#2)  
    2.1. [Программные интерфейсы](#2.1)  
    2.2. [Интерфейс пользователя](#2.2)  
    2.3. [Характеристики пользователей](#2.3)
1. [Системные требования](#3)  
    3.1. [Функциональные требования](#3.1)  
    3.2. [Нефункциональные требования](#3.2)  
        3.2.1. [Атрибуты качества](#3.2.1)  
            3.2.1.1. [Требования к удобству использования](#3.2.1.1)   
            3.3.1.2. [Требования к безопасности](#3.2.1.2)  
        3.2.2. [Ограничения](#3.2.2)  
 1. [Аналоги](#4)
--- 
## 1. Введение <a name="1"></a>
***MusicLand*** - это веб-приложение, которое построено в формате интернет-магазина и предназначено для продажи музыкальных инструментов, звукозаписывающего оборудования и аксессуаров.

## 2. Требования <a name="2"></a>
### 2.1. Программные интерфейсы <a name="2.1"></a>
Серверная часть проекта построена на ***Java***, а также использует базу данных ***MySQL***. Клиентская часть использует ***Angular.js*** и ***Bootstrap***.

### 2.2. Интерфейс пользователя <a name="2.2"></a>
[Главная страница](https://github.com/R3g3m/TRTPO/blob/master/Mockups/main.png) включает меню в верхней части страницы, позволяющей обеспечить быстрый доступ к основным элементам приложения (корзина, окно авторизации).   
[Страница каталога](https://github.com/R3g3m/TRTPO/blob/master/Mockups/catalog.png) отображает информацию о товарах, найденных с помощью поисковой строки и с использованием фильтров. На странице имеется информация о стоимости товаров. Основной функцией данной страницы является кнопка добавления товара в корзину.  
[Страница товара](https://github.com/R3g3m/TRTPO/blob/master/Mockups/item.png) включает детальную информацию о товаре: стоимость, описание, параметры, фото. Страница также включает кнопку добавления в корзину.
### 2.3. Характеристики пользователей <a name="2.3"></a>
Приложение предназначено для профессиональных музыкантов а также людей, которые решили приобрести музыкальный инструмент. Приложение также позволяет менеджеру интернет-магазина добавлять и удалять новые товары в каталог, редактировать их описание и цену.
| Класс пользователей | Описание |
|---|---|
| **Administrator** | Пользователь, являющийся управляющим всего приложения. Имеет доступ к полному функционалу. Имеет возможность создания/удаления пользователей с меньшим уровнем доступа. Имеет возможность управления базой данных|
| **Manager** | Пользователь, который имеет доступ к расширенному, но ограниченному функционалу. Может изменять, добавлять и удалять в продукты в каталог, определять ключевые слова для поиска, менять статус наличия продукта. Имеет доступ к списку сформированных заказов. |
| **User** | Пользователь, который имеет доступ к ограниченному функционалу. Может изменять, добавлять и удалять в продукты в проделах своей корзины, отправлять заказ на обработку. |
| **Unregistered User** | Пользователь, который имеет доступ к максимально ограниченному функционалу. Может только просматривать каталог, перед покупкой товара ему будет предложено пройти регистрацию в системе.  |

## 3. Системные требования <a name="3"></a>
Работа приложения осуществляется на любых устройствах, поддерживающих веб-браузеры ***Chrome***, ***Opera***, ***Safari*** и ***Firefox*** последних версий.

### 3.1. Функциональные требования <a name="3.1"></a>
Пользователю предоставлены возможности:
1. Предоставление интерфейса к БД продаваемых товаров (в виде каталога, прайс-листа);
2. Регистрация покупателей(администратор);
3. Работа с электронной корзиной покупателя(менеджер, user);
4. Оформление заказов с выбором метода оплаты, даты и типа доставки(user);
5. Автоматический обмен информацией с серверами в офисе компании и системами банковских рассчётов.

### 3.2 Нефункциональные требования <a name="3.2"></a>

#### 3.2.1 Атрибуты качества <a name="3.2.1"></a>

#### 3.2.1.1 Требования к удобству использования <a name="3.2.1.1"></a>
1. Предусмотрено навигационное меню в верхней части экрана, позволяющее быстро перейти к любой странице приложения.
2. Наличие формы авторизации для предоставления пользователям возможности авторизироваться либо сменить текущий аккаунт.
3. Наличие иконкок корзины и профиля пользователя.
4. Отображение количества товаров, находящихся в корзине, рядом с иконкой корзины.
5. Отображение стоимости товаров, находящихся в корзине, рядом с иконкой корзины.

#### 3.2.1.2 Требования к безопасности <a name="3.2.1.2"></a>
1. Защищенное соединение посредством TLS-шифрования.
1. Отсутствие XSS-уязвимостей посредством правильно настроенных Content-Security-Policy.
1. Отсутствие External Information Leak уязвимостей, предоставляющих данные о системе, посредством обработки исключений и логгирования.
1. Отсутствие Cross-Site Scripting уязвимостей, посредством валидации входных и выходных данных.

### 3.2.2 Ограничения <a name="3.2.2"></a>
1. Бразуеры, помимо ***Chrome***, ***Opera***, ***Safari*** и ***Firefox***, не имеют гарантированной поддержки
2. Последние версии вышеперечисленных бразуеров.

### 4. Аналоги <a name="4"></a>
1. http://guitarland.by/
2. http://musicmarket.by/
3. http://crazysound.by/
