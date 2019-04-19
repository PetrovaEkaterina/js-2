# Homework #2 OOP, prototype inheritance
## Deadline 06.05.2019
### Create menu
Вы хозяин небольшого кафе быстрого питания. Ваше меню состоит из следующих позиций:
#### 1) Гамбургер
    
    - маленький (+50 тугриков, +20 калорий)
    - большой (+100 тугриков, +40 калорий)
    
    Гамбургер может быть с одним из нескольких видов начинок (обязательно):
    
    - сыром (+10 тугриков, +20 калорий)
    - салатом (+20 тугриков, +5 калорий)
    - картофелем (+15 тугриков, +10 калорий)

#### 2) Салат (цена и калории указаны за 100г)

    - Цезарь (+100 тугриков, +20 калорий)
    - Оливье (+50 тугриков, +80 калорий)
    
#### 3) Напиток
    
    - Кола (+50 тугриков, +40 калорий)
    - Кофе (+80 тугриков, +20 калорий)
    
Необходимо написать программу, для расчета стоимости и/или каллорийности заказа посетителя.
В заказе могут быть как одна, так и несколько позиций разных видов. (Например заказ может состоять из 2х гамбургеров(один большой, другой маленький), салата Оливье(150г) и кофе). В заказ можно как добавлять позиции, так и удалять из него лишнее (при условии, что оно там есть). После оплаты заказа он должен стать не редактируемым - ничего добавить или удалить из него больше нельзя.

**Комментарии**  
Задачу необходимо решить используя ООП и ES5. Крайне желательно использование наследования и композиции. Типы начинок, размеры надо сделать константами. Никаких [магических строк](https://ru.wikipedia.org/wiki/%D0%9C%D0%B0%D0%B3%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%BE%D0%B5_%D1%87%D0%B8%D1%81%D0%BB%D0%BE_(%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5)#.D0.9F.D0.BB.D0.BE.D1.85.D0.B0.D1.8F_.D0.BF.D1.80.D0.B0.D0.BA.D1.82.D0.B8.D0.BA.D0.B0_.D0.BF.D1.80.D0.BE.D0.B3.D1.80.D0.B0.D0.BC.D0.BC.D0.B8.D1.80.D0.BE.D0.B2.D0.B0.D0.BD.D0.B8.D1.8F) не должно быть. 

**Реализация**  
Выполнить задание необходимо с UI частью, используя DOM события. Выбор стилей, инструментов на личное усмотрение каждого, верстка оцениваться в рамках данной задачи не будет. 

#### Примерный вид класса гамбургер  

    /**
    * Класс, объекты которого описывают параметры гамбургера. 
    * 
    * @constructor
    * @param size        Размер
    * @param stuffing    Начинка
    */
    function Hamburger(size, stuffing) { ... } 

    /* Размеры, виды начинок и добавок */
    Hamburger.SIZE_SMALL = ...
    Hamburger.SIZE_LARGE = ...
    Hamburger.STUFFING_CHEESE = ...
    Hamburger.STUFFING_SALAD = ...
    Hamburger.STUFFING_POTATO = ...

    /**
     * Узнать размер гамбургера
     */
    Hamburger.prototype.getSize = function () ...

    /**
     * Узнать начинку гамбургера
     */
    Hamburger.prototype.getStuffing = function () ...

    /**
     * Узнать цену гамбургера
     * @return {Number} Цена в тугриках
     */
    Hamburger.prototype.calculatePrice = function () ...

    /**
     * Узнать калорийность
     * @return {Number} Калорийность в калориях
     */
    Hamburger.prototype.calculateCalories = function () ...

