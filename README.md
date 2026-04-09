# Лабораторная работа №20. Работа с DOM и событиями в JavaScript

---

## Основная информация

**ФИО:** Гвоздева В.А, Деушев Т.Т
**Группа:** ИСП-231
**Дата:** 07.04.2026

---

## Краткое описание работы




---

## Структура проекта

- Lab20_DOM_Events_Gvozdeva_Deushev/ 
    - dynamicElements.html
    - dynamicElements.js
    - index.html
    - main.js
    - README.md
    - style.css
    - img/ 
        - gitPushLab20_DOM_Events_Gvozdeva_Deushev.png
        - step2_domStructureLab20_Gvozdeva_Deushev.png
        - step3_domSelectionLab20_Gvozdeva_Deushev.png
        - step4_domManipulationLab20_Gvozdeva_Deushev.png
        - step5_clickEventLab20_Gvozdeva_Deushev.png
        - step6_inputEventLab20_Gvozdeva_Deushev.png
        - step7_miniTaskLab20_Gvozdeva_Deushev.png
        - step8_formInputLab20_Gvozdeva_Deushev.png
        - step9_formValidationLab20_Gvozdeva_Deushev.png
        - step10_dynamicElementsLab20_Gvozdeva_Deushev.png

---

## Сравнение с C# (WinForms/WPF)

|**Концепция**|**C# (WinForms)**|**JavaScript (DOM)**|
|:-------:|:-----------:|:--------------:|
|Найти элемент|Button myButton = this.Controls["myButton"]|const myButton = document.getElementById("myButton")|
|Изменить текст|label1.Text = "Новый текст"|label.textContent = "Новый текст"|
|Добавить обработчик|button1.Click += HandleClick|button.addEventListener("click", handleClick)|
|Создать элемент|Button btn = new Button()|const btn = document.createElement("button")|
|Добавить в контейнер|panel1.Controls.Add(btn)|panel.appendChild(btn)|
|Скрыть элемент|button1.Visible = false|button.style.display = "none"|

---

## Events в JS = События в C#

### C# (WinForms):

```csharp
private void Button1_Click(object sender, EventArgs e) {
    label1.Text = "Нажато!";
}
```

### JavaScript (DOM):

```js
button.addEventListener("click", (e) => {
    label.textContent = "Нажато!";
});
```

---

## Валидация формы

### C# (WinForms):

```csharp
private void SubmitButton_Click(object sender, EventArgs e) {
    if (string.IsNullOrEmpty(nameTextBox.Text)){
        MessageBox.Show("Введите имя!");
        return;
    }
    // ...
}
```

### JavaScript (DOM):

```js
form.addEventListener("sumbit", (e) => {
    e.preventDefault();

    if (!nameInput.value.trim()) {
        alert("Введите имя!");
        return;
    }
    // ...
})
```

---

## Главные отличия:

|**Аспект**|**C# WinForms**|**JavaScript DOM**|
|---------:|:-------------:|:----------------:|
|Компиляция|Да|Нет (интерпретация)|
|Типизация|Строгая|Динамическая|
|Ошибки|Во время компиляции|Во время выполнения|
|UI-дизайнер|Есть (визуальный)|Нет (только код)|
|Платформа|Windows|Любой браузер|

---

## Преимущества DOM перед WinForms:

- Кроссплатформенность (работает везде)
- Не нужна установка приложения
- Легко обновлять (обновил файлы — всё работает)
- Современные UI (CSS, анимации)

---

## Преимущества WinForms перед DOM:

- Визуальный дизайнер (drag & drop)
- Ошибки на этапе компиляции
- Интеграция с Windows API
- Более понятная структура

**Вывод:** DOM и WinForms решают схожие задачи, но разными подходами.
