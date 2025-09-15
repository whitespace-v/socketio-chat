
# Socket.IO Chat

A simple chat demo for Socket.IO

## How to use

```
$ npm i
$ npm start
```

And point your browser to `http://localhost:3000`. Optionally, specify
a port by supplying the `PORT` env variable.

## Features

- Multiple users can join a chat room by each entering a unique username
on website load.
- Users can type chat messages to the chat room.
- A notification is sent to all users when a user joins or leaves
the chatroom.

# Документация

#1. "add user"

Направление: Клиент → Сервер
Назначение: Регистрация нового пользователя в системе
Данные: Имя пользователя (строка)

#2. "login"

Направление: Сервер → Клиент
Назначение: Подтверждение успешной авторизации пользователя
Данные: Объект с количеством пользователей онлайн

#3. "typing"

· Направление: Клиент → Сервер
· Назначение: Уведомление о начале набора сообщения
· Данные: Отсутствуют

#4. "new message"

Направление: Двустороннее (клиент-сервер-клиенты)
Назначение: Отправка и распространение текстовых сообщений
Данные: Текст сообщения (строка)

#5. "stop typing"

Направление: Клиент → Сервер
Назначение: Уведомление о прекращении набора текста
Данные: Отсутствуют

#6. "user joined"

Направление: Сервер → Клиенты
Назначение: Уведомление о подключении нового пользователя
Данные: Объект с именем пользователя и обновлённым количеством участников
