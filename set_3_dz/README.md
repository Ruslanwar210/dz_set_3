## Задание

Реализуйте структуру телефонной книги с помощью HashMap.
Программа также должна учитывать, что в во входной структуре будут повторяющиеся имена с разными телефонами, их необходимо считать, как одного человека с разными телефонами. Вывод должен быть отсортирован по убыванию числа телефонов.

## Решение

Решил создать отдельный класс `PhoneBook` в виде коллекции, основанной на `HashMap`. В качесве ключа выступает имя контакта (тип данных: `String`), значение - список номеров (тип данных`ArrayList<String>`).

#В классе `PhoneBook` реализованы такие методы как:
- `size`: возвращает количество контактов в коллекции
- `empty`: возвращает `true` если коллекция пустая
- `put`: добавляет контакт в коллекцию, если при добавлении имя контакта уже существует - то добавляется только номер в значение по данному ключу
- `delContact`: удаляет контакт по ключу (имя)
- `clear`: полностью очищает всю коллекцию
- `getAll`: возвращает коллекцию целиком

Так же переопределен метод `toString` в котором реализована сортировка коллекции по убыванию номеров. Если коллекция пуста, то метод вернет строку: `"The phone book is empty"`
