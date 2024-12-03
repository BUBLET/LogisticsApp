
# LogisticsDApp

LogisticsDApp — это децентрализованное приложение (DApp) для управления логистическими заказами на основе блокчейна. Оно обеспечивает прозрачность, безопасность и надежность данных, позволяя пользователям создавать, отслеживать и подтверждать заказы в распределенной сети.

## Возможности

- **Создание заказов:** Отправители могут создавать новые логистические заказы, указывая получателя, расстояние, тип груза и автоматически рассчитываемую цену.
- **Отслеживание заказов:** Пользователи могут просматривать список своих отправленных и полученных заказов.
- **Оплата заказов:** Отправители могут оплачивать заказы через блокчейн.
- **Подтверждение получения:** Получатели могут подтверждать получение заказа и оставлять отзывы.
- **Статистика:** Просмотр общей статистики по количеству заказов, отзывов и средней оценке.
- **Управление компанией:** Специальные функции для компаний, включая управление заказами.

## Стек

- **Frontend:** React, Material-UI, Web3.js
- **Backend:** Truffle, Solidity
- **Блокчейн:** Ethereum (можно использовать Ganache для локального тестирования)
- **Управление состоянием:** React Hooks

## Установка и Запуск

### Инструменты

Убедитесь, что у вас установлены следующие инструменты:

- [Node.js](https://nodejs.org/) (версия 14.x или выше)
- [npm](https://www.npmjs.com/) (устанавливается вместе с Node.js)
- [Truffle](https://www.trufflesuite.com/truffle) (для работы со смарт-контрактами)
- [Ganache](https://www.trufflesuite.com/ganache) (для локального тестирования блокчейна)

### Шаг 1: Клонирование Репозитория

```bash
git clone https://github.com/BUBLET/logistics-app
cd LogisticsDApp
```

### Шаг 2: Установка Зависимостей Backend

В корневой директории проекта установите зависимости для Truffle:

```bash
npm install
```

### Шаг 3: Компиляция и Развёртывание Смарт-Контрактов

1. **Запустите Ganache:** Откройте Ganache для локального тестирования блокчейна.

2. **Настройте Truffle:** Убедитесь, что `truffle-config.js` настроен на использование сети Ganache. Обычно это сеть с ID `5777`.

3. **Миграция контрактов:**

```bash
npm run migrate
```

Это скомпилирует и развернет смарт-контракт на локальном блокчейне. После успешной миграции в папке `build/contracts/` появится файл `Logistics.json`, содержащий ABI и адрес контракта.

### Шаг 4: Установка Зависимостей Frontend

Перейдите в директорию фронтенда и установите зависимости:

```bash
cd frontend/LogisticsApp
npm install
```

### Шаг 5: Запуск Frontend

После установки зависимостей запустите React-приложение:

```bash
npm start
```

Приложение откроется в вашем браузере по адресу [http://localhost:3000](http://localhost:3000).

## Использование

1. **Подключение MetaMask:**
   - Убедитесь, что у вас установлен [MetaMask](https://metamask.io/) и подключён к локальной сети Ganache.
   - Импортируйте аккаунты из Ganache в MetaMask, используя приватные ключи.

2. **Создание Заказа:**
   - Перейдите во вкладку "Добавить заказ".
   - Заполните форму с данными заказа и отправьте транзакцию.

3. **Отслеживание Заказов:**
   - Вкладка "Список заказов" отображает все ваши отправленные и полученные заказы.
   - Для отправителей доступны кнопки "Оплатить" (если заказ не оплачен).
   - Для получателей доступны кнопки "Подтвердить получение" (если заказ оплачен).

4. **Отзывы и Статистика:**
   - Вкладка "Отзывы" позволяет просматривать отзывы о выполненных заказах.
   - Вкладка "Статистика" показывает общую информацию по заказам и отзывам.

5. **Управление Компанией:**
   - Доступна вкладка "Управление" для специальных функций.


