#Домашнее задание к лекции 9.«Работа с библиотекой requests, http-запросы»
##Задача №1

Кто самый умный супергерой? Есть [API](https://superheroapi.com/?ref=apilist.fun#appearance) по информации о супергероях. Нужно определить кто самый умный(intelligence) из трех супергероев- Hulk, Captain America, Thanos. Для определения id нужно использовать метод /search/name

Токен, который нужно использовать для доступа к API: 2619421814940190.
Таким образом, все адреса для доступа к API должны начинаться с https://superheroapi.com/api/2619421814940190/.

-> ⚠️ Недавно сервис SuperHero API переехал на заблокированный Роскомнадзором IP-адрес, из-за чего некоторые интернет-провайдеры заблокировали к нему доступ, он может быть недоступен. В таком случае решайте это задание на REPL.it — оттуда всё должно быть доступно.

##Задача №2

У Яндекс.Диска есть очень удобное и простое API. Для описания всех его методов существует [Полигон](https://yandex.ru/dev/disk/poligon/). Нужно написать программу, которая принимает на вход путь до файла на компьютере и сохраняет на Яндекс.Диск с таким же именем.

1. Все ответы приходят в формате json;
2. Загрузка файла по ссылке происходит с помощью метода put и передачи туда данных;
3. Токен можно получить кликнув на полигоне на кнопку "Получить OAuth-токен".

HOST: https://cloud-api.yandex.net:443

Важно: Токен публиковать в github не нужно, переменную для токена нужно оставить пустой!

Шаблон для программы

``` class YaUploader:
    def __init__(self, token: str):
        self.token = token

    def upload(self, file_path: str):
        """Метод загружает файлы по списку file_list на яндекс диск"""
        # Тут ваша логика
        # Функция может ничего не возвращать


if __name__ == '__main__':
    # Получить путь к загружаемому файлу и токен от пользователя
    path_to_file = ...
    token = ...
    uploader = YaUploader(token)
    result = uploader.upload(path_to_file)
    
   ```

##*Задача №3(необязательная)

Самый важный сайт для программистов это stackoverflow. И у него тоже есть [API](https://api.stackexchange.com/docs) Нужно написать программу, которая выводит все вопросы за последние два дня и содержит тэг 'Python'. Для этого задания токен не требуется.
