# Ограничения на использование экспортных процедур и функций в модуле команд и форм

Не следует размещать экспортные процедуры и функции в модулях команд и
форм. К этим модулям нет возможности обращаться из внешнего по
отношению к ним кода, поэтому экспортные процедуры и функции в этих
модулях не имеют смысла.

## Неправильно

```bsl
&НаКлиенте
Процедура ОбработкаКоманды(ПараметрКоманды, ПараметрыВыполненияКоманды) Экспорт
КонецПроцедуры
```

## Правильно

```bsl
Процедура ОбработкаКоманды(ПараметрКоманды, ПараметрыВыполненияКоманды)
КонецПроцедуры
```

## См.

- [Ограничения на использование экспортных процедур и функций](https://its.1c.ru/db/v8std#content:544:hdoc)