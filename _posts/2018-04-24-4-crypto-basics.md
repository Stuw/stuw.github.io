---
number: 4
title: "Основы криптографии"
subtitle: "Шифрование и хеширование"
date: "2018-04-24 22:00:00"
keywords: "crypto, криптография, симметричное шифрование, асимметричное шифрование, хеш"
mp3file: "Безопасность для всех - 4 - 2018.04.24.mp3"
mp3size: "7170024"
mp3duration: "10:27"
---
Обнаружены очередные поддельные расширения для браузера Google Chrome, часть пользователей установили эти расширения. Власти Канадской провинции Новая Шотландия выложили конфиденциальные данные в открытый доступ. Google закрывает возможность обхода блокировок через свои домены, а Volkswagen Group исправила уязвимости в автомобилях.

<!--more-->
## Предисловие
Мир реальный и мир виртуальный отличаются очень сильно. Например, в виртуальном мире не стоит практически никаких усилий создать копию чего-либо. Некоторые сущности не имеют прямых аналогов в реальном мире. Приведенные мною аналогии реального мира для объяснения сущностей мира виртуального можно применять только с оговорками. Но они помогают понять суть вещей. Помните об этом, когда будете слушать этот и последующие выпуски.

## Картинка недели
![Безопасность xkcd](/assets/images/4_xkcd_538_v1.png)

[https://xkcd.ru/538/](https://xkcd.ru/538/)

## Вспомогательные темы
Принцип Керкгоффса - правило разработки криптографических систем, согласно которому криптосистема должна оставаться безопасной даже в том случае, когда злоумышленнику известно всё, кроме применяемых ключей. Другими словами, при разработке криптосистемы не следует полагаться на то, что злоумышленнику не будут известны все детали применяемого алгоритма.

Сущность принципа заключается в том, что чем меньше секретов содержит система, тем выше её безопасность.
Секретность алгоритмов иногда допустима, например в случае алгоритмов военного или государственного применения. В этой ситуации секретность является дополнительным рубежом обороны.

Большинство распространенных криптографических систем использует открытые алгоритмы, которые сами не являются секретом.

## Новости
### Более 20 млн пользователей Chrome установили поддельное расширение AdBlock
Расширения-блокировщики рекламы защищают пользователей от всплывающих окон и назойливой рекламы на сайтах. Для Google Chrome есть достаточно большое количество разнообразных расширений. Но среди полезных попадаются поддельные расширения, и особенно много поддельных блокировщиков рекламы. Как сообщают исследователи из Adguard Software Limited, они нашли очередную порцию таких расширений. На данный момент Google уже удалил их, но более 20 млн пользователей успели их поставить.

Из открытых блокировщиков можно посоветовать uBlock Origin от разработчика по имени Реймонд Хилл. Если будете искать его, то ищите именно полное название - uBlock Origin, т.к. существуют ответвления и поддельные расширения.

[https://www.hackread.com/20-million-chrome-users-have-installed-fake-malicious-ad-blockers/](https://www.hackread.com/20-million-chrome-users-have-installed-fake-malicious-ad-blockers/)

### Власти Новой Шотландии выложили в публичный доступ приватные данные жителей
19-летний молодой человек из провинции Канады искал информацию в публичном архиве, в который местные власти помещают некоторые документы, в соответствии с законодательством. Он подметил, что адрес документа на сайте содержит числовой идентификатор. При изменении этого идентификатора в адресной строке браузера можно получить доступ к другому документу. Т.к. существующее решения для поиска по документам его не устроило, он написал однострочный скрипт и скачал весь архив.

Как оказалось, местные власти неблагоразумно выложили в публичный доступ конфиденциальную информацию и теперь инкриминируют юноше незаконный доступ.

Данный пример демонстрирует одну из распространенных проблем/уязвимостей в информационных системах - небезопасный прямой доступ. Broken Access Control в терминологии OWASP Top 10 за 2017 год. В данном случае факт “эксплуатации” уязвимости неоднозначен, т.к. информация была расположена на сайте, предполагающем свободный доступ к информации. Однако полиция возбудила уголовное дело. Пока не ясно, чем закончится эта история.

[https://boingboing.net/2018/04/16/scapegoating-children.html](https://boingboing.net/2018/04/16/scapegoating-children.html)

### Google закрывает domain-fronting
До недавнего времени разработчики приложений могли использовать домены Google в качестве прокси, для перенаправления трафика к своим серверам. Это можно было использовать для обхода блокировок. Как заявляет Google, данная возможность никогда официально не поддерживалась. Теперь же, после изменений в сетевой инфраструктуре гиганта, данный подход работать не будет.

[https://www.theverge.com/2018/4/18/17253784/google-domain-fronting-discontinued-signal-tor-vpn](https://www.theverge.com/2018/4/18/17253784/google-domain-fronting-discontinued-signal-tor-vpn)

### Некоторые модели концерна Volkswagen Group можно взломать
В ходе исследовательской работы специалисты компании Computest обнаружили уязвимость в некоторых моделях концерна Volkswagen Group. Уязвимость позволяет получить удаленный доступ к системам автомобиля. В некоторых случаях можно получить доступ к мультимедиа, адресной книге, истории разговоров. Также есть вероятность получить доступ к навигационной системе. Т.к. названные компоненты имеют косвенный доступ к системе управления ускорением и торможением автомобиля, исследование решено было прекратить.

Специалисты уведомили о проблемах VW Group, которая уже устранила проблемы. Как вы можете видеть, иногда обновлять необходимо даже автомобили.

[https://www.computest.nl/en/pressrelease-en/volkswagen-group-models-vulnerable-to-hackers/](https://www.computest.nl/en/pressrelease-en/volkswagen-group-models-vulnerable-to-hackers/)

## Основы криптографии
Я не буду сегодня оперировать формулами. Во-первых, потому, что это может быть скучно или непонятно, как минимум для некоторых слушателей. Во-вторых, потому, что голосом объяснять формулы достаточно сложно.

Многие пугаются слов криптография, шифрование, ключи шифрования, и т.д. На самом деле в основе большинства протоколов и алгоритмов лежит три простых концепции, для объяснения которых мне не понадобятся математические формулы. Поэтому этой темы совершенно не стоит бояться.

Математическая точность нужна при реализации и проектировании криптоалгоритмов. Для использования нужно знать некоторые тонкости. Но для понимания общих схем и принципа действия достаточно базовых знаний.

### Симметричное шифрование
Первый примитив, который используется - это симметричное шифрование. Симметричное оно потому, что для шифрования и расшифровывания нужен один и тот же ключ. Это должно быть интуитивно понятно. Схему симметричного шифрования можно сравнить с сейфом, который закрывается на ключ. Чтобы спрятать от посторонних глаз какие-то данные мы закрываем сейф нашим ключем. Чтобы получить доступ к закрытым в сейфе данным, мы берем тот же ключ, или точную его копию, и открываем сейф.

### Асимметричное шифрование (с открытым ключем)
Следующий примитив - асимметричное шифрование или шифрование с публичным ключем. В этом случае, в отличие от симметричного шифрования используются два разных ключа. Один используется для шифрования, второй - для расшифровывания.
Один из ключей называется открытый или публичный, второй закрытый или приватный.

Давайте попытаемся понять, какой из ключей используется для шифрования, а какой для расшифровывания… Как ясно из названия публичный ключ известен всем. Приватный же должен быть известен только одному субъекту или группе. Никто кроме них не должен уметь получать исходное сообщение из зашифрованного. Значит для расшифровывания должен использоваться приватный ключ.

Соответственно, публичный будет использоваться для шифрования. При таком подходе любой, кто знает публичный ключ, может зашифровать сообщение для владельца приватного ключа. И только владелец приватного ключа сможет это сообщение прочитать.

Асимметричное шифрование с небольшой натяжкой можно сравнить с банковским переводом - для того, чтобы отправить деньги нужно знать, ФИО и номер счета, которые будут выступать в качестве публичного ключа. Чтобы деньги забрать, нужен будет паспорт, который является аналогом ключа приватного.

### Хеширование
Третий примитив - это хеширование, т.е. преобразование входных данных произвольной длины к значению определенного размера. Алгоритмы хеширования различаются свойствами. Для нас пока важным будет криптографическая стойкость.

Что это такое? Это свойство означает, что алгоритм, или функция, хеширования должна, во-первых, не позволять найти исходные данные зная лишь значение хеша. Во-вторых должна быть стойкой к коллизиям.
Первый вариант коллизий: если имеется какое-то входное значение и его хеш, нельзя найти другое входное значение, у которого результат хеш функции будет совпадать с исходным.
Второй, более строгий вариант: нельзя найти два набора входных данных, у которых значение хеша будет одинаковым.

Под словом “нельзя” понимается, что это невозможно сделать за разумное время. Для разных систем разумными могут быть разные временные промежутки.

### Особенности
Асимметричное шифрование оперирует числами. Поэтому большие объемы данных, например файл в несколько гигабайт, зашифровать таким алгоритмом проблематично. Симметричное шифрование в своей основе имеет более быстрые операции. Но симметричные алгоритмы чаще всего оперируют блоками определенной длины. Поэтому для шифрования больших объемов, данные разбивают на небольшие куски и шифруют отдельно.

Если мы знаем публичный ключ и нам нужно будет передать большой объем данных владельцу приватного ключа, нам придется использовать и асимметричное, и симметричное шифрование. Мы должны будем сгенерировать ключ для симметричного шифрования, этим ключем зашифровать данные, используя, естественно, симметричный алгоритм. А уже сам ключ зашифровать публичным ключем.

При получении нужно будет действовать в обратном порядке. Сначала, используя свой приватный ключ, расшифровать ключ симметричного шифрования. И уже используя симметричный алгоритм расшифровать данные.



На сегодня у меня все. Многие важные вещи мы оставили за пределами обсуждения, но к ним мы еще обязательно вернемся.

Свободного всем интернета, до следующей недели.
