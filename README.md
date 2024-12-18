# goit-rdb-hw-02

## Початкова таблиця

| Номер_замовлення | Назва_товару і кількість | Адреса_клієнта | Дата_замовлення | Клієнт    |
| ---------------- | ------------------------ | -------------- | --------------- | --------- |
| 101              | Лептоп: 3, Мишка: 2      | Хрещатик 1     | 2023-03-15      | Мельник   |
| 102              | Принтер: 1               | Басейна 2      | 2023-03-16      | Шевченко  |
| 103              | Мишка: 4                 | Комп'ютерна 3  | 2023-03-17      | Коваленко |

## 1NF

| Номер_замовлення | Назва_товару | Кількість | Адреса_клієнта | Дата_замовлення | Клієнт    |
| ---------------- | ------------ | --------- | -------------- | --------------- | --------- |
| 101              | Лептоп       | 3         | Хрещатик 1     | 2023-03-15      | Мельник   |
| 101              | Мишка        | 2         | Хрещатик 1     | 2023-03-15      | Мельник   |
| 102              | Принтер      | 1         | Басейна 2      | 2023-03-16      | Шевченко  |
| 103              | Мишка        | 4         | Комп'ютерна 3  | 2023-03-17      | Коваленко |

## 2NF

### Order

| Номер_замовлення | Дата_замовлення | Клієнт    |
| ---------------- | --------------- | --------- |
| 101              | 2023-03-15      | Мельник   |
| 102              | 2023-03-16      | Шевченко  |
| 103              | 2023-03-17      | Коваленко |

### OrderItem

| Номер_замовлення | Назва_товару | Кількість |
| ---------------- | ------------ | --------- |
| 101              | Лептоп       | 3         |
| 101              | Мишка        | 2         |
| 102              | Принтер      | 1         |
| 103              | Мишка        | 4         |

### User

| Клієнт    | Адреса_клієнта |
| --------- | -------------- |
| Мельник   | Хрещатик 1     |
| Шевченко  | Басейна 2      |
| Коваленко | Комп'ютерна 3  |

## 3NF

### Order

| Order_ID | Номер_замовлення | Дата_замовлення | Клієнт_ID |
| -------- | ---------------- | --------------- | --------- |
| 1        | 101              | 2023-03-15      | 1         |
| 2        | 102              | 2023-03-16      | 2         |
| 3        | 103              | 2023-03-17      | 3         |

### OrderItem

| ID  | Замовлення_ID | Товар_ID | Кількість |
| --- | ------------- | -------- | --------- |
| 1   | 1             | 1        | 3         |
| 2   | 1             | 2        | 2         |
| 3   | 2             | 3        | 1         |
| 4   | 3             | 2        | 4         |

### Product

| ID  | Назва_товару |
| --- | ------------ |
| 1   | Лептоп       |
| 2   | Мишка        |
| 3   | Принтер      |

### User

| ID  | Ім'я_клієнта | ID_Адреси |
| --- | ------------ | --------- |
| 1   | Мельник      | 1         |
| 2   | Шевченка     | 2         |
| 3   | Коваленко    | 3         |

### Address

| ID  | Вулиця      | Будинок |
| --- | ----------- | ------- |
| 1   | Хрещатик    | 1       |
| 2   | Басейна     | 2       |
| 3   | Комп'ютерна | 3       |

### ER Diagram

![ER Diagram](./screenshots/p4_erdiagram2.png)

### Database Schema

![Database Schema p1](./screenshots/p5_1.png)
![Database Schema p2](./screenshots/p5_2.png)
