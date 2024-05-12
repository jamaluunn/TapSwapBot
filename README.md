[<img src="https://img.shields.io/badge/Telegram-%40Me-orange">](https://t.me/sho6ot)


![img1](.github/images/demo.png)

> 🇪🇳 README in english available [here](README-EN.md)

## Функционал  
| Функционал                                                     | Поддерживается  |
|----------------------------------------------------------------|:---------------:|
| Многопоточность                                                |        ✅        |
| Привязка прокси к сессии                                       |        ✅        |
| Авто-покупка предметов при наличии монет (tap, energy, charge) |        ✅        |
| Рандомное время сна между кликами                              |        ✅        |
| Рандомное количество кликов за запрос                          |        ✅        |
| Поддержка tdata / pyrogram .session / telethon .session        |        ✅        |


## [Настройки](https://github.com/shamhi/TapSwapBot/blob/main/.env-example)
| Настройка                | Описание                                                                                    |
|--------------------------|---------------------------------------------------------------------------------------------|
| **API_ID / API_HASH**    | Данные платформы, с которой запускать сессию Telegram (сток - Android)                      |
| **MIN_AVAILABLE_ENERGY** | Минимальное количество доступной энергии, при достижении которой будет задержка (напр. 100) |
| **SLEEP_BY_MIN_ENERGY**  | Задержка при достижении минимальной энергии в секундах (напр. 200)                          |
| **ADD_TAPS_ON_TURBO**    | Сколько тапов будет добавлено при активации турбо (напр. 2500)                              |
| **AUTO_UPGRADE_TAP**     | Улучшать ли тап (True / False)                                                              |
| **MAX_TAP_LEVEL**        | Максимальный уровень прокачки тапа (до 20)                                                  |
| **AUTO_UPGRADE_ENERGY**  | Улучшать ли энергию (True / False)                                                          |
| **MAX_ENERGY_LEVEL**     | Максимальный уровень прокачки энергии (до 20)                                               |
| **AUTO_UPGRADE_CHARGE**  | Улучшать ли заряд энергии (True / False)                                                    |
| **MAX_CHARGE_LEVEL**     | Максимальный уровень прокачки заряда энергии (до 5)                                         |
| **APPLY_DAILY_ENERGY**   | Использовать ли ежедневный бесплатный буст энергии (True / False)                           |
| **APPLY_DAILY_TURBO**    | Использовать ли ежедневный бесплатный буст турбо (True / False)                             |
| **RANDOM_CLICKS_COUNT**  | Рандомное количество тапов (напр. 50,200)                                                   |
| **SLEEP_BETWEEN_TAP**    | Рандомная задержка между тапами в секундах (напр. 10,25)                                    |
| **USE_PROXY_FROM_FILE**  | Использовать-ли прокси из файла `bot/config/proxies.txt` (True / False)                     |


## Установка
Вы можете скачать [**Репозиторий**](https://github.com/shamhi/TapSwapBot) клонированием на вашу систему и установкой необходимых зависимостей:
```shell
~ >>> git clone https://github.com/shamhi/TapSwapBot.git 
~ >>> cd TapSwapBot

# Если вы используете Telethon сессии, то клонируйте ветку "converter"
~ >>> git clone https://github.com/shamhi/TapSwapBot.git -b converter
~ >>> cd TapSwapBot

# Linux
~/TapSwapBot >>> python3 -m venv
~/TapSwapBot >>> source venv/bin/activate
~/TapSwapBot >>> pip3 install -r requirements.txt
~/TapSwapBot >>> cp .env-example .env
~/TapSwapBot >>> nano .env  # Здесь вы обязательно должны указать ваши API_ID и API_HASH , остальное берется по умолчанию
~/TapSwapBot >>> python3 main.py

# Windows
~/TapSwapBot >>> python -m venv venv
~/TapSwapBot >>> venv\Scripts\activate
~/TapSwapBot >>> pip install -r requirements.txt
~/TapSwapBot >>> copy .env-example .env
~/TapSwapBot >>> # Указываете ваши API_ID и API_HASH, остальное берется по умолчанию
~/TapSwapBot >>> python main.py
```

Также для быстрого запуска вы можете использовать аргументы, например:
```shell
~/TapSwapBot >>> python3 main.py --action (1/2/3)
# Или
~/TapSwapBot >>> python3 main.py -a (1/2/3)

# 1 - Создает сессию
# 2 - Запускает кликер
# 3 - Запуск через Telegram
```
