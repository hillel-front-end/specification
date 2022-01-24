# Изучить материал
* https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Operators/this
* для вас: https://yandexdataschool.ru/edu-process/courses

# Практика
1) Есть обьект `obj = { }`
Внутри него описываем методы `copy, clear, doFunction`.
Организовать создание методов так, что бы можно было вызывать любые
комбинации:<hr >
    `obj.doFunction(sum, 2, 4).doFunction(mul, 6, 3).clear()`<hr >
`doFunction(func, x, y);` получает параметрами 2 числа и функцию, которую нужно применить к x и y. Результат операции сохранять в `obj.result`<hr >
`clear()` очищает значение `obj.result` в 0<hr >

*
`obj.copy(buffer)` получает параметром название ключа buffer (string) и добавляет его к `obj`
Далее в любом порядке можно вызывать комбинации функций 

*
Создать метод `obj.target(property)`- дальнейшие действия функций doFunction() и clear() будут изменять значение не result, а переданной `property`

Пример:
        obj
        .doFunction(sum, 2, 4)
        .copy('some_name')
        .target('some_name')
        .doFunction(mul, 6, 3)


## <hr />

2) Сделайте функцию inArray, которая определяет, есть в массиве элемент с
заданным текстом или нет. Функция первым параметром должна принимать
текст элемента, а вторым - массив, в котором делается поиск. Функция должна
возвращать true или false.<hr >
` inArray('foo', ['sjhfnaof', 'affooasf', 'dfhdfhdfh'])` должно вернуть `true`, т.к. в `affooasf` есть совпадение.


## Лекция

1) Задан обьект с любым количеством свойств. Одно из свойств является функция `renderObject()`, которая описана в window.
При вызове метода `obj.renderObject()` -> выводит в document всё содержимое объекта, кроме самого метода `renderObject`


        obj => { x:10, y: 20 }
        obj.renderObject() -> x:10, y: 20

2) Реализовать объект с методами m1(), m2(), m3(). Должна быть возможность выполнять подобный код:

        obj.m1().m2().m3();
        obj.m2().m1().m3();
        obj.m2().m1().m3().m1().m1();
        ...

3) в обьекте `data` существует метод `addRecord`, который аргументами получает любой набор объектов. Метод `addRecord` добавляет все свойства переданных объектов в `data`.


        data = {
            addRecord: function(){},
            p: 600,
            str: 'hello',
            y: -50
        }
        data.addRecord({x: 10}, {y: 20}, {z: 30, x: 50});
        data.x // 50
        data.y // 20
        data.z // 30
        data.p // 600
        data.str // 'hello'

4) В метод `addRecord` добавляется последний необязательный аргумент `flag`, который указывает приоритет присвоения свойств с одинаковым названием.
Если `true` - берется свойство из первоначального объекта `this`, если `false` - берется свойство из `arguments`.  По умолчанию `flag = false;`