# Изучить материал
    + https://cli.vuejs.org/ru/guide/installation.html
    + https://ru.vuejs.org/v2/guide/single-file-components.html
    + https://ru.vuejs.org/v2/guide/components-slots.html
    + https://ru.vuejs.org/v2/guide/mixins.html
    + https://ru.vuejs.org/v2/guide/computed.html

    + https://ru.vuejs.org/v2/guide/components-props.html
    + https://ru.vuejs.org/v2/guide/components-custom-events.html
# Практика
    
1) Создать компоненту FormGenerator. Которая будет выдавать шаблон для ввода значений.
Пример использования: <FormGenerator :form="['input[type=text]', 'input[type=email]', 'input[type=button]', 'input[type=text]']">

2) Добавляем props с названием model <FormGenerator :model="inputData">. В model свойство будет сохранятся результат введенных значений во все поля, которые генерируются.
# Лекция

1) Создать список из имен блоков. Внутри компоненты ContactContainer есть input type="text", если введеное значение равно одному из имен блоков - блок подсвечивается.
