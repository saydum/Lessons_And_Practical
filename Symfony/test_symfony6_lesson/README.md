# Lesson Symfony 6
[Источник](https://www.youtube.com/playlist?list=PL3D9-9G1ETEpy8DQHrapim_OWjRUoRyOb)

## 1. Видео

1. Собираем приложение
`docker-compose -f ./docker/docker-compose.yml build`

2. Запускаем приложение
`docker-compose -f ./docker/docker-compose.yml up -d`

3. Устонавливаем Symfony (Выполняем команду из контейнера)
```bash
docker exec -it php-fpm bash
composer create-project symfony/skeleton:"6.1.*" app
```
---
Error
```txt
Warning: require(/var/www/vendor): Failed to open stream: No error information in /var/www/vendor/composer/autoload_real.php on line 55

Fatal error: Uncaught Error: Failed opening required '/var/www/vendor/composer/..' 
(include_path='.:/usr/local/lib/php') in /var/www/vendor/composer/autoload_real.php:55 Stack trace: 
#0 /var/www/vendor/composer/autoload_real.php(38): composerRequire1eef8cd664260af08300463e89d9d669('0e6d7bf4a5811bf...', '/var/www/vendor...') 
#1 /var/www/vendor/autoload.php(25): ComposerAutoloaderInit1eef8cd664260af08300463e89d9d669::getLoader() 
#2 /var/www/vendor/autoload_runtime.php(5): require_once('/var/www/vendor...')
#3 /var/www/public/index.php(5): require_once('/var/www/vendor...') 
#4 {main} thrown in /var/www/vendor/composer/autoload_real.php on line 55
```
Удалил и заново установил проект Sumfony
---


## 2. Видео
Установка и настройка XDEBUG

## 3. Видео TDD
1. Установка PHPUnit
`composer require --dev phpunit/phpunit symfony/test-pack`

2. переименовываем  `phpunit.xml.dist` в `phpunit.xml`

## 4 Чистая Архитектура (Onion + Modular Monolith + Hexagonal)

### 4.1 Многослойная архитектура
[Источник](https://habr.com/ru/post/427739/)

### 4.2 Модульная архитектура
[Источник](https://habr.com/ru/post/579976/)

### 4.3 Гексагональная архитектура
[Symfony и Гексагональная архитектура](https://habr.com/ru/post/539084/)