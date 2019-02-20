# Изучить материал

* https://learn.javascript.ru/prototype
* https://learn.javascript.ru/new-prototype
* https://learn.javascript.ru/native-prototypes
* https://learn.javascript.ru/classes
* https://ru.wikipedia.org/wiki/%D0%9E%D0%B1%D1%8A%D0%B5%D0%BA%D1%82%D0%BD%D0%BE-%D0%BE%D1%80%D0%B8%D0%B5%D0%BD%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D0%BE%D0%B5_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5

# Практика

1) Создать класс SuperMath. Добавить к экземпляру метод - check(obj), параметр obj которого имеет свойства X, Y, znak. Метод должен подтвердить у пользователя хочет ли он произвести действие znak c Х и У. Если - да, сделать математическое действие znak(которое описано в прототипе), иначе - запросить ввод новых данных через метод input() класса SuperMath.
Пример обекта: `obj = { X:12, Y:3, znak: “/”}`, возможные варианты znak=>  `+ - / * %`.
При вводе znak нужно сделать проверку корректности ввода на возможные математические действия

        p = new SuperMath();
        p.check(obj); // --> no p.input() -> 3 prompt -> считает
        