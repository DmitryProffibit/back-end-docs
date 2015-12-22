# Dictionary API

## GET public/dictionary/:dictTypeId

### PARAMS   
  * dictTypeId - идентификатор словаря. Существующие словарей можно узнать выполнив `GET dicttype` 

### RESPONCE
```js
  {
    key, // идентификатор записи в справочнике
    value, // значение для отображения пользователю
    sort, // поле для сортировки
    // остальные возвращаемые поля являются временным побочным эфектом
  }
```
### Note