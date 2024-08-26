<div align="center">

# Мемная лента Телеграм | Парсер новых мемов из групп

Бот, который с помощью vk-api ~~ворует~~ копирует мемы вам в чат, ЛС или супергруппу!  
Мой Телеграм канал - [Клик](https://t.me/CreateTrigger)

<img src="https://github.com/user-attachments/assets/b3e68df3-a872-43aa-a93a-cc8e28ace541" width=70% height=80%>
</div>

## 📖 Описание

Для функционирования вам потребуется аккаунт во ВКонтакте, бот с помощью методов vk-api получает информацию о новом посте.  
В свою очередь новые посты проверяются специльным скриптом [checker](bot/checker.py).  
  
Можно заставить бота скидывать мемы в группу, канал, супергруппу или в линые сообщения.  

Все данные храняться в SQLite, мемы в хранилище, поэтому вам потребуется место на диске

## 📦 Команды

В личных сообщениях бот полностью работает на callback кнопках (кроме добавления новых групп)

### Команды для групп и супергрупп:

* `add {url}` - Подписывает чат на новые мемы группы ВК.
* `list` - Выводит список всех групп, на которые подписан чат.

<div align="center">
<img src="https://github.com/user-attachments/assets/5cab8e86-2803-4e71-a18f-7c0865f74c75" width=70% height=80%>
</div>

### У супергрупп есть топики, или же обсуждения, и если не указать в какой из топиков отправлять мемы, вылезет оишбка...

* `мем сюда` - Можно писать несколько раз, дает понять боту в какой топик скидывать мемы.
* `meme here` - Альтернатива `мем сюда`.

<div align="center">
<img src="https://github.com/user-attachments/assets/d5552996-8a86-4d0c-9ce0-bde5d71b44e9" width=70% height=80%>
</div>

Если нажать на callback с названием группы, после ввода команды `list` - покажется панель усправления.  
Здесь можно отписаться от новых мемов группы.

<div align="center">
Здесь можно отписаться от новых мемов группы.
<img src="https://github.com/user-attachments/assets/c2a7bd71-6c3a-46ae-b934-0ce0b4f07c8c" width=70% height=80%>
</div>

## 🤖 Запуск бота

Для функционирования бота вам потребуется аккаунт ВКонакте и место на диске.

### 1. Для начала вам потребутеся склонировать репозиторий к себе на компьютер через Git Bash.

```git
git clone https://github.com/droptrigger/VK-to-TG-parser-memes-news-feed.git
```

### 2. Установим все неободимые библиотки:

```console
pip install aiogram
pip install vk-api
pip install aiosqlite
```

### 3. Переходим по ссылке **https://vkhost.github.io**, выбираем "Настройки", включаем ВСЕ права, тип токена - пользователь. Разрешаем и копируем ссылку.
<div align="center">
<img src="https://github.com/user-attachments/assets/f8ba0c58-431c-446a-addc-6fa70af80035" width=80% height=80%>
</div>

### 4. Из ссылки копируем все с `access_token=` по `&expires_in...`. И записываем это куда-нибудь.
### 5. Переходим в https://t.me/BotFather и создаем бота, отключаем ему режим `Privacy mode`. Это нужно для того, чтобы бот реагировал н сообщения.
<div align="center">
<img src="https://github.com/user-attachments/assets/0e0a9373-2e2f-4986-8230-d1c011a05f4c" width=60% height=80%>
</div>

### 6. В том же BotFather берем и копируем API ключ

<div align="center">
<img src="https://github.com/user-attachments/assets/16d2b471-2818-49c9-a248-4a8e77b37685" width=60% height=80%>
</div>

### 7. Переходим в файл [config](bot/data/config.py) и вместо пропусков вписываем наши токены.
* P.S: (если начнет ругаться vk-api при запуске, вы не правильно вставили токен, либо он вовсе не правильный)

## ✅ Well done! Теперь все должно работать

<div align="center">
![image](https://github.com/user-attachments/assets/cbec2ec9-189e-43b3-a2f9-85444ebb04b7)
</div>
