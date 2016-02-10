---
layout: post
title: Установка и настройка локального веб-сервера wamp и среды разработки под него.
tags: [apache, mysql, php, postgresql, wamp]
---

Это пост-инструкция для того, чтобы каждый раз не вспоминать, что, где и как настраивается, откуда берётся и куда устанавливается.

##WAMP дистрибутивы

Куда устанавливать? Для удобства использую две директории в корне диска:
в **documents** хранятся все файлы проектов, в **usr** устанавливаю весь серверный и вспомогательный софт.

Apache пока подойдёт версии 2.2 (для php 5.5 нужна версия 2.4, об этом напишу отдельно), берём [здесь](http://httpd.apache.org/download.cgi#apache22), в binaries/win32 последняя версия с openssl — чтобы можно было локально запускать сайты по https.

PHP качаем [отсюда](http://windows.php.net/download/) архивом. Дополнительно можно взять и установщик, если лень вручную указывать переменные окружения. В таком случае следует обязательно после установки поверх скопировать файлы из архива.

Следом забираем с официальных серверов дистрибутивы [MySQL](http://dev.mysql.com/downloads/mysql/) и [PostgreSQL](http://www.postgresql.org/download/windows/). В качестве альтернативы MySQL можно использовать [MariaDB](https://mariadb.org/) — форк MySQL, выделившийся в отдельный проект после покупки Sun компанией Oracle.

##Настройка

Поскольку в основном я пишу на Eaze Framework, то при настройке локального веб-сервера придерживаюсь его [документации](http://wiki.eaze.ru/start/%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%BD%D1%8B%D0%B5_%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B8).

##Инструменты разработки

1.IDE — [PhpStorm](http://www.jetbrains.com/phpstorm/) (к слову, [EAP-версией](http://confluence.jetbrains.com/display/PhpStorm/PhpStorm+Early+Access+Program) можно пользоваться бесплатно совершенно легально);
2.Контроль версий — SVN ([TortoiseSVN](http://tortoisesvn.net/downloads.html));
3.Total Commander — помогает быстро перемещаться по директориям, также является неплохим FTP-клиентом;
4.[Babun](http://babun.github.io/) — эмулятор линуксового шелла с поддержкой zsh, пакетным менеджером pact и другими вкусностями; надстройка над [Cygwin](https://www.cygwin.com/);
5.[Sublime Text](https://antyblin.wordpress.com/2014/09/12/%d1%83%d1%81%d1%82%d0%b0%d0%bd%d0%be%d0%b2%d0%ba%d0%b0-%d0%b8-%d0%bd%d0%b0%d1%81%d1%82%d1%80%d0%be%d0%b9%d0%ba%d0%b0-%d0%bb%d0%be%d0%ba%d0%b0%d0%bb%d1%8c%d0%bd%d0%be%d0%b3%d0%be-%d0%b2%d0%b5%d0%b1/www.sublimetext.com/3) — лучший текстовый редактор из тех, что я встречал, быстрый, удобный, лёгкий;
6.EMS MySQL Manager и PostgreSQL Manager значительно упрощают работу с БД;
7.Toad Data Modeller — для построения схем БД с возможностью экспорта в SQL-файл;
8.[Fiddler](http://www.telerik.com/download/fiddler) — прокси, позволяющий работать с трафиком между локальным компьютером и удалённым сервером.