# Разработка системы распознавания голоса с использованием глубоких нейронных сетей для улучшения точности распознавания
[COLAB](https://colab.research.google.com/drive/1roXCUIT8J9LsLAAVYxytE3HSI4BOaMoI?authuser=2#scrollTo=cmBgvAe1wxyV)
[TG](https://t.me/alkashGPT3_bot)
## Описание проекта

Данный проект представляет собой Telegram-бота, который принимает голосовые сообщения от пользователей и преобразует их в текст с использованием модели распознавания речи Whisper от OpenAI. Бот написан на языке программирования Python и использует GPU для повышения скорости обработки данных.

## Технологии

- Язык программирования: Python
- Основные библиотеки:
  - [PyTelegramBotAPI](https://github.com/eternnoir/pyTelegramBotAPI) — для взаимодействия с Telegram API
  - [Whisper](https://github.com/openai/whisper) — для распознавания речи
  - [PyTorch](https://pytorch.org/) — для работы с моделью Whisper на GPU
  - [pydub](https://github.com/jiaaro/pydub) — для конвертации аудиофайлов

## Требования

1. Python версии 3.8 или выше.
2. Установленный PyTorch с поддержкой GPU (CUDA).
3. Токен Telegram-бота, полученный через BotFather.

## Установка

1. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/LastPeek1/Lab-3.git
   ```
2. Перейдите в директорию проекта:
   ```bash
   cd Lab-3
   ```
3. Установите необходимые зависимости:
   ```bash
   pip install -r requirements.txt
   ```
   

## Запуск

1. Вставьте токен вашего бота в переменную `API_TOKEN` в файле `bot.py`.
2. Запустите бота:
   ```bash
   python bot.py
   ```

## Принцип работы

1. Пользователь отправляет голосовое сообщение боту в Telegram.
2. Бот загружает голосовое сообщение и сохраняет его в формате OGG.
3. Бот конвертирует аудиофайл из OGG в WAV с помощью библиотеки `pydub`.
4. Модель Whisper обрабатывает WAV-файл и преобразует его в текст.
5. Бот отправляет распознанный текст в ответ пользователю.

## Возможные ошибки

- **Ошибка конвертации аудиофайла:** Убедитесь, что установлены необходимые кодеки для работы с аудиоформатами.
- **Ошибка распознавания:** Проверьте корректность пути к аудиофайлу и доступность GPU.

## Примеры использования

1. Отправьте боту голосовое сообщение в Telegram.
2. Получите текстовую расшифровку сообщения в ответ.

## Заключение

Проект представляет собой простое, но мощное решение для преобразования голосовых сообщений в текст с использованием современной модели распознавания речи Whisper. Использование GPU значительно ускоряет обработку данных, что делает бота идеальным для работы в реальном времени.
