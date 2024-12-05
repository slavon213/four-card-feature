# four-card-feature

## Мій варіант рішення домашнього завдання

### Створено за допомогою:

-   Semantic HTML5 markup
-   CSS custom properties
-   Flexbox

---

### В цьому домашньому завдання я використав:

-   глобальні змінні для кольорів
-   вставку картинки через background-image
-   **Flexbox** для розміщення елементів
-   linear-gradient для фону в верхньому бордері

### Що було найважче?

-   Найважчим завданням для мене було створити верхній кольоровий бордер
    Знайшов таке рішення:

```html
<article class="supervisor">
    <div class="stick"></div>
    <h3>Supervisor</h3>
    <p>Monitors activity to identifyproject roadblocks</p>
    <div class="image"></div>
</article>
```
Тут `<div class="stick"></div>`  відповідає за верхній бордер.

```css
div.stick {
    width: 100%;
    height: 8px;
    border-radius: 8px 8px 0 0;
    background: linear-gradient(to bottom, var(--top-stick) 50%, #fff 50%);
    position: absolute;
    left: 0;
    top: 0;
}
```

Тут верхній `div` має колірний градієнт. Кольори поділені по висоті наполовину і нижній колір завжди має колір фону `article`. Верхній колір `var(--top-stick)` змніюється відповідно до макету.

В макеті `border-radius` articl-а має `8px`, тоді верхній колір матиме висоту `4px` (половина від висоти скруглення).
