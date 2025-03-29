# **Morse Code Converter**

**Проект выполнен в рамках обучения в [Yandex Practicum](https://practicum.yandex.ru/)**

## **Описание проекта**

Проект представляет собой HTTP-сервер, который умеет автоматически определять, является ли ввод текстом или кодом Морзе, и преобразовывать его в противоположный формат:

- **Текст → Код Морзе** (например, `"SOS"` → `"... --- ..."`)
- **Код Морзе → Текст** (например, `".- --."` → `"AG"`)

Сервер принимает POST-запросы с входными данными и возвращает результат в текстовом виде.

---

## **Функциональность**

### **1. Определение типа ввода**

Сервер автоматически распознаёт, является ли ввод:

- **Текстом** (содержит буквы, цифры, знаки препинания)
- **Кодом Морзе** (состоит только из `.`, `-` и пробелов)

### **2. Преобразование**

- Если ввод — текст, он кодируется в Morse.
- Если ввод — Morse, он декодируется в текст.

### **3. HTTP API**

- **Метод:** `POST /convert`
- **Тело запроса:** Произвольный текст или Morse-код
- **Ответ:** Преобразованный результат

---

## **Как запустить проект**

### **Требования**

- Go 1.20+

### **Установка и запуск**

1. Клонируйте репозиторий:

   ```sh
   git clone https://github.com/Vova4o/sprin6
   cd sprint6
   ```

2. Запустите сервер:

   ```sh
   go run ./cmd/main.go
   ```

3. Сервер будет доступен по адресу:
   ```
   http://localhost:8080
   ```

---

## **Примеры запросов**

### **1. Кодирование текста в Morse**

**Запрос:**  
На странице вы модете закачать файл с текстом.

**Ответ:**

В ответ получите строку морзе, и файл в основной директории с данным кодом.

### **2. Декодирование Morse в текст**

**Запрос:**

Также можно передать файл с морзе.

**Ответ:**

В ответ вы получите текст, и сохраненый файл в домашнее дирктории проекта.

## **Тестирование**

Для проверки корректности работы можно использовать:

- **Ручные запросы** (Postman)
- **Веб интерфейс**

---

Выполнено в рамках курса **"Go-разработчик с нуля"** в [Yandex Practicum](https://practicum.yandex.ru/).

---
