---
number: 23
title: "Мы пойдем другим путем!"
subtitle: "Атаки по сторонним каналам"
date: "2018-09-06 23:00:00"
keywords: "side channel"
mp3file: "Безопасность для всех - 23 - 2018.09.06.mp3"
mp3size: "7528388"
mp3duration: "11:35"
---

Утечка данных пользователей Air Canada; в Twitter опубликована неисправленная уязвимость в Windows; из Google Play удалено 127 вредоносных приложений; кража данных платежных карт на зараженных сайтах.

Основная тема - атаки по сторонним каналам (Side Channel Attacks).

<!--more-->

## Картинка недели

![Родина слышит](/assets/images/23-motherland-listens.jpg)

[http://vasya-lozhkin.ru/pictures/rodina-slyshit/](http://vasya-lozhkin.ru/pictures/rodina-slyshit/)

## Вспомогательные темы

Сетевой червь - разновидность вредоносной программы, которая самостоятельно распространяется через Интернет и локальные сети.

CERT - computer emergency response team. Название групп экспертов, занимающихся исследованием инцидентов информационной безопасности, их классификацией и нейтрализацией. Первый такой центр был создан в институте Карнеги-Меллон по заказу правительства США для борьбы с червем Морриса, который в 1988 году парализовал работу интернета. Оригинальная команда (CERT/CC) все также базируется в институте Карнеги-Меллон и является координационным центром для других команд CERT.

## Новости

### Утечка данных пользователей Air Canada

Компания Air Canada подтвердила утечку данных. По предварительным подсчетам могли быть скомпрометированы данные 20 000 пользователей. Компания сообщила, что заметила подозрительные входы в мобильное приложение в период с 22 по 24 августа. В этот период персональные данные могли быть доступны злоумышленникам.

Пока нет ясности, был ли это взлом систем авиакомпании или же злоумышленники воспользовались повторно используемыми паролями и виноваты в утечке сами пользователи. В любом случае компания заблокировала все аккаунты во избежание других утечек и порекомендовала пользователям сменить пароли.

[https://thehackernews.com/2018/08/air-canada-data-breach.html](https://thehackernews.com/2018/08/air-canada-data-breach.html)

### В Twitter опубликована неисправленная уязвимость в Windows

Неожиданным способом открылась информация о новой уязвимости в Windows. Пользовательница под ником SandboxEscaper опубликовала в Twitter ссылку на свой github репозиторий, в котором размещены примеры эксплуатации. Проблема относится к типу локального повышения привилегий и позволяет локальному пользователю поднять свои права до System.

Проблемным компонентом является планировщик процессов, проблема связана с неправильной обработкой вызовов расширенных локальных процедур (Advanced Local Procedure Call, ALPC). Через некоторое время после публикации твита аналитик координационного центра CERT Уилл Дорманн (Will Dormann) подтвердил, что проблема воспроизводится на последней версии Windows 10 со всеми установленными апдейтами.

Ждем фикс в очередном вторнике патчей, который намечен на 11 сентября.

[https://thehackernews.com/2018/08/windows-zero-day-exploit.html](https://thehackernews.com/2018/08/windows-zero-day-exploit.html)

### Из Google Play удалено 127 вредоносных приложений

Специалисты компании Dr.Web обнаружили в Google Play приложения, которые подписывают пользователей на платные услуги.

Одно из приложений предоставляло функциональность поиска по каталогу Эльдорадо. Но помимо этого приложение показывало рекламу, а также открывало страницы с платными услугами и, автоматически нажимая кнопку, подписывало на них пользователя. Приложение проникало в каталог в двух вариациях, обе удалены.

Вторая группа приложений также подписывала пользователей на платные услуги. Маскировались эти приложения под онлайн магазины, такие как Aliexpress, доску объявлений Юла, голосового помощника Алиса от Яндекс и другие легитимные приложения. Услуги подключали с помощью фишинга: приложение открывало сайт, на котором предлагалось скачать приложение или сообщалось о выигрыше. Далее у пользователя спрашивали номер телефона и код подтверждения из смс. Код, как Вы понимаете, использовался для подтверждения подписки.

Были также обнаружены и другие разновидности вредоносных приложений. Некоторые маскировались под приложения от букмекерских контор.

По большому счету подобные приложения могут маскироваться под любое другое. В том числе и под мессенджер. Наличие рекламы, а тем более большого ее количества, в приложении известной компании должно насторожить - многие компании прибыль обычно получают за счет продажи товаров или услуг, а не за счет рекламы в мобильных приложениях. Поэтому при установке софта обращайте внимание на издателя. Абсолютной защиты это не даст, но часть мошенников точно отсеет.

[https://xakep.ru/2018/08/31/more-android-click/](https://xakep.ru/2018/08/31/more-android-click/)

### Кража данных платежных карт на зараженных сайтах

Независимый исследователь Виллем де Грот (Willem de Groot) обнаружил более 7 тысяч зараженных сайтов, с которых злоумышленники получали данные о банковских картах пользователей. Все зараженные сайты объединяет то, что они работают на платформе Magento.

Заражение происходит следующим образом. Сначала злоумышленники получают доступ к панели управления интернет магазина. Обычно просто подбирая пароль, на что в некоторых случаях могут уйти месяцы.

Далее в шаблон сайта внедряется вредоносный скрипт с домена magentocore.net, а также добавляется запускаемый периодически скрипт, который нужен для восстановления доступа, на случай, если основной скрипт будет удален с сайта. Также злоумышленники добавляют пользователя с фиксированным паролем.

Для удаления вредоноса нужно сначала найти путь, которым он проник, затем вычистить все его следы. Чтобы предотвратить подобное, владельцы должны периодически обновлять платформу, использовать сложные неповторяющиеся пароли. По возможности использова 2fa (двухфакторную аутентификацию), тем более magento это позволяет.

[https://xakep.ru/2018/08/31/magentocore/](https://xakep.ru/2018/08/31/magentocore/)

## Атаки по сторонним каналам

А теперь об атаках и утечках данных по сторонним каналам. Я не буду пытаться рассказать про все возможные типы и способы, а постараюсь рассказать про наиболее простые и интересные. Начну с довольно старой вещи, которую, думаю, многие знают и помнят. Речь про Денди. Да, про ту самую игровую приставку, клон Nintendo Famicom.

### Денди

Как она относится к нашей теме? Да самым прямым способом. Возможно кто-то с этим даже сталкивался сам. Однажды я пытался найти на телевизоре какой-то канал и запустил автоматический поиск. Я пропустил несколько раз уже известные мне каналы и ждал следующий, который найдет телевизор. Каково же было мое удивление, когда телевизор остановил поиск, а среди кучи помех я увидел силуэты из знакомой игры.

Что же я увидел и откуда оно взялось в моем телевизоре? Разгадка проста, это был сигнал с приставки соседа. Дело в том, что приставку можно было подключить к телевизору через антенное гнездо, обычным коаксиальным кабелем. При этом, как оказалось, сигнал достаточно сильно излучается, что позволяет поймать его на обычную комнатную антенну в соседней квартире или доме.

### ПЭМИН

Это явление имеет свое определение - Побочные ЭлектроМагнитные Излучения и Наводки (ПЭМИН). С такими паразитными излучениями стараются бороться, например, экранированием. Если брать жизненные примеры из менее далекого прошлого, то можно найти проект под названием Tampest SDR. Что такое Software Defined Radio, я рассказывал в 14-м выпуске подкасата. А TEMPEST в названии появилось от названия американского стандарта на электромагнитные излучения ( Transient Electromagnetic Pulse Emanation Standard).

Проект Tampest SDR позволяет исследовались излучаемые сигналы для восстановления изображения выводимого на монитор. Причем как оказалось, большие утечки сигнала идут не от монитора, а от видеокарты.

[https://github.com/martinmarinov/TempestSDR](https://github.com/martinmarinov/TempestSDR)

[https://www.youtube.com/watch?v=PV_v1HgjN3Q](https://www.youtube.com/watch?v=PV_v1HgjN3Q)

### Колебания

Еще один тип побочного излучения - механические колебания и звуковые волны. Самыми очевидными объектами исследований стали матричные принтеры, которые, как оказалось, все еще достаточно часто используются в некоторых сферах, и клавиатуры. Получать данные из звуков клавиатуры оказалось сложнее, из-за человеческого фактора. А вот информацию с принтеров, как показали исследования можно восстановить более чем в 70% случаев. А если знать контекст, то процент ближе к 95.

Но исследователи пошли в изучении звуков работающих устройств еще дальше. Наверняка все замечали, что при включении устройств, у которых нет вентиляторов и других движущихся частей, все-равно возникает некоторый писк. Он связан с электрическим током. Совсем недавно, в августе, были опубликованы результаты работы по изучению звуков работающего монитора для восстановления изображения. Это возможно, потому что для вывода изображения на разные участки, тратится разное количество энергии. Как следствие меняется энергопотребление и звук. Четкое изображение получить не удастся, но некоторую информацию восстановить можно.

[http://www.opennet.ru/opennews/art.shtml?num=49185](http://www.opennet.ru/opennews/art.shtml?num=49185)

### Потребление энергии

Изменение уровня потребления энергии может быть использовано при анализе криптографической защиты устройств. Если на разных стадиях работы криптоалгоритма устройством тратится разное количество энергии, то это может дать представление, например, о том, какой ключ шифрования используется.

### Время

Еще один фактор, который достаточно часто используют в атаках, это время. Допустим алгоритм проверяет пароль. Сначала проверяется первый символ, затем второй и так далее. Если результат будет возвращаться сразу же, как встретится первый неправильный символ, то в зависимости от того, в какой позиции находится этот символ, время проверки будет различаться. Как следствие, анализируя затраченное время, можно будет сказать, в какой позиции находится неправильный символ. Это даст возможность подбирать символы отдельно - сначала первый, потом второй и так далее. Это существенно сократит количество перебираемых комбинаций.

Фактор времени используется и в нашумевших атаках Spectre и Meltdown. В них атакующий формирует код таким образом, что процессор загружает к себе в кеш значение одной из ячеек массива. Какой именно ячейки, зависит от значения в памяти, которое нужно прочитать атакующему. У атакующего нет возможности прочитать это значение напрямую. Далее атакующий читает все элементы массива по порядку и замеряет время доступа. Тот элемент, доступ к которому был получен быстрее всего и был закеширован. По этому признаку атакующий и узнает содержимое ячейки памяти, к которой у него нет прямого доступа. Ведь именно это значение влияло на то, какой элемент массива кэшировался ранее.

### Передача данных с изолированного компьютера

Напоследок еще один интересный случай. Допусти есть компьютер, на котором нет никаких сетевых подключений - ни wi-fi, ни блютус, ни проводных. Вообще никаких, просто изолированный компьютер. Туда попало наше ПО, например, на USB флешке. Как получить с этого компьютера данные? Казалось бы, что это невозможно. Но есть несколько способов. Один из них - кодировать данные с помощью звука работы жесткого диска. Пример можной найти на YouTube вбив в поиске DiskFiltration.

[https://www.youtube.com/watch?v=H7lQXmSLiP8](https://www.youtube.com/watch?v=H7lQXmSLiP8)

---

На сегодня все. Дерзайте и придумывайте новое. До следующей недели.

