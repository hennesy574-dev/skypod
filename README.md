# Sky Pod Shop

## Инструкция по установке и деплою

### 1. Установка зависимостей
```bash
npm install
```

### 2. Настройка переменных окружения
Скопируйте `.env.example` в `.env` и заполните своими данными:
```bash
cp .env.example .env
```

### 3. Настройка Firebase
1. Перейдите на https://console.firebase.google.com
2. Создайте новый проект
3. Включите **Realtime Database** (правила: read/write true для теста)
4. Скопируйте конфигурацию в .env файл

### 4. Деплой на Vercel
1. Загрузите проект на GitHub
2. Зайдите на https://vercel.com
3. Создайте новый проект из репозитория
4. Добавьте переменные окружения из .env файла
5. Нажмите Deploy

### 5. Telegram Bot
1. Создайте бота у @BotFather в Telegram
2. Скопируйте токен в .env или настройте через админ-панель
3. Найдите ID чата (используйте @userinfobot)

### Доступ в админ-панель
URL: ваш_сайт/admin
Логин: admin
Пароль: skypod2025

### Firebase правила (для продакшена)
```json
{
  "rules": {
    ".read": true,
    ".write": "auth != null"
  }
}
```
