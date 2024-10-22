# TinyMCE Custom Plugins

<details>
  <summary><strong>Shortcodes</strong></summary>
  
  #### Опис

  > Плагін <strong>shortcodes</strong> для TinyMCE дозволяє користувачам легко вставляти шорткоди в редактор тексту через зручний інтерфейс. Він підтримує як статичні, так і динамічні шорткоди. 

  #### Основні функції

  > - **Меню шорткодів**: Дозволяє користувачам вибирати шорткоди з контекстного меню.
  > - **Копіювання в буфер обміну**: Шорткоди автоматично копіюються у буфер обміну при виборі, що спрощує їх використання.
  > - **Сповіщення**: Інформує користувачів про успішне копіювання шорткоду або про помилки.

  #### Встановлення

  > 1. Завантажити файл `shortcodes.min.js` та перейменувати його на `plugin.min.js`.
  > 2. В директорії TinyMCE знайти папку `plugins` та створити в ній папку `shortcodes`, перемістити туди файл, який був завантажений та перейменований.
  > 3. У файлі, де ініціалізується TinyMCE, додати `shortcodes` до параметрів `plugins` та `toolbar`:
  ```javascript
     tinymce.init({
         plugins: 'anchor code shortcodes',
         toolbar: 'fullscreen | shortcodes',
     });
  ```
  
  Готово!

  #### Приклади використання

  > 1. **Статичні шорткоди**:
   ```html
      <textarea class="f-tinymce" data-shortcodes='@json([["key" => "[user:email]", "name" => "Email користувача"]])'></textarea>
   ```
   ```html
      <textarea class="f-tinymce" data-shortcodes='{{ json_encode([["key" => "[user:firstname]", "name" => "Ім'я користувача"], ["key" => "[user:lastname]", "name" => "Прізвище користувача"]]) }}'></textarea>
   ```

  > 2. **Динамічні шорткоди**:
   ```html
     <textarea class="f-tinymce" data-shortcodes-url="http://site.test/api/shortcodes"></textarea>
   ```
</details>
