# BIOS_X99_China_Optimize
***[DISCORD](https://discord.com/invite/EJRjXXtjMV)***
## Предупреждение
ВАЖНО ПОНИМАТЬ ЧТО ЛЮБЫЕ МАХИНАЦИИ С ПРОШИВКОЙ БИОСА ПРИ ИЗМЕНЁННЫХ НАСТРОЙКАХ(ОСОБЕННО ТЕХ ЧТО НАХОДЯТСЯ В ТЕСТЕ) ДЕЛАЮТСЯ НА СВОЙ СТРАХ И РИСК. ГАЙД НЕ МОЖЕТ ЯВЛЯТЬСЯ 100% РЕШЕНИЕМ ИБО БИОСЫ У ВСЕХ РАЗНОЙ СТЕПЕНИ ГОВЁНОСТИ И ЧТО МОЖЕТ НОРМАЛЬНО РАБОТАТЬ НА ОДНОЙ ПЛАТЕ МОЖЕТ СПОКОЙНО НЕ РАБОТАТЬ НА ДРУГОЙ. На большинстве Huananzhi и Machinist всё должно работать, но кто знает что может выстрелить.

Для отката биоса в случае проблем нужен программатор CH341A.

Гайд основан на:
1. [Биосы кошака/там же и некоторые гайды](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/tree/master)
2. [Xeon-e5450.ru faq](https://xeon-e5450.ru/socket-2011-3/faq/)
3. [Драйвера для x99](https://xeon-e5450.ru/socket-2011-3/drivers-x99/)
4. [Хак турбобуста](https://xeon-e5450.ru/socket-2011-3/e5-2600-v3/dobavlyaem-anlok-v-bios-raz-i-navsegda-cherez-s3turbotool/)
5. [GENERAL Overclock.Net BIOS](https://www.overclock.net/threads/gaming-and-mouse-response-bios-optimization-guide-for-modern-pc-hardware.1433882)
6. [INTEL BIOS SETTINGS EXPLANATION](https://docs.google.com/document/d/1s43_3YGJIy3zs0ZIksoOmxgrDKnu4ZNhhnXW_NiJZ0I/edit)
7. [Hidden bios settings list - Des1de & CatGamerOP](https://docs.google.com/document/d/1KIW7D9tCcv5sBBCh9qR6S-jZSsvTKQFwtOfBhkaBD4E/edit)
8. [Intel Hidden Bios Setting Guide Scewin By Ancel](https://docs.google.com/document/d/1ztCWHU2vCG9hnD_94VhlnsLJq1-0Mq7OwhjF79JsYgA/edit)
9. Свои методы реализации некоторых моментов при настройке.
10. [S3TurboTool](https://4pda.to/forum/index.php?showtopic=1015953)
11. [Overclockers 2011-3](https://forums.overclockers.ru/viewtopic.php?f=1&t=602922&start=520)
12. [Разгон ОЗУ x99 Overclockers](https://forums.overclockers.ru/viewtopic.php?f=4&t=622568)

## 1. Подбор биоса для своей материнской платы
Заходим по первой [ссылке](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/tree/master) на гитхаб кошака и ищем свою материнскую плату. Если твоей платы там нет, то можно перейти в ТГ который указан в там же, предоставить дамп оригинадьного биоса и попросить разлочить в нём настройки таймингов(если таковых не имеется в стоковом биосе). 

Можно столкнуться с тем что у платы несколько ревизий и биос от одной может не подойти к другой. Как в этом примере:
![](https://github.com/DmitryPonyn/BIOS_X99_China_Optimize/blob/main/images/BIOS_rev.png)

В таком случае нужно осмотреть материнскую плату на наличее надписей Ver/Rev и исходя из неё выбрать нужную версию биоса. Если надписи такой нет, то нужно зайти на [xeon-e5450.ru](xeon-e5450.ru) и в выпадающем списке вверху "2011-3" выбрать свою материнскую плату и там будет как различить разные ревизии.

После нахождения нужной папки скачиваем zip архив в названии которого есть приписка kot и разорхивируем в корень диска C в папку BIOS.

Для того чтобы удостовериться что мы скачали верный биос скачиваем S3TurboTool по 10 [ссылке](https://4pda.to/forum/index.php?showtopic=1015953) и распаковываем архив в папку в которую распаковали наш биос. Запускаем S3TurboTool из папки в которую мы его распаковали, соглашаемся с соглашением и делаем бекап нынешнего биоса в папку с программой в формате .bin. Далее в том же окне S3TurboTool открываем два окна AMIBCP в которых открываем бекап нынешнего биоса и который мы скачали с гитхаба. В обоих окнах выбераем вверху вкладку DMI Tables и там пункт "Base Board (or Module) Information (Type 2)" и сравниваем информацию в строках которые выдаст программа.
![](https://github.com/DmitryPonyn/BIOS_X99_China_Optimize/blob/main/images/BIOS_check.png)

Если всё сошлось то прекрасно, значит мы скачали то что нужно.

## 2. Разгон/анлок турбобуста(если процессор v4 пропускай) 

<details>
<summary>Разгон 16xx v3<summary/>
ДАННЫЙ МЕТОД РАБОТАЕТ ТОЛЬКО ЕСЛИ В ТВОЕЙ МАТЕРИНСКОЙ ПЛАТЕ СТОИТ СЕРВЕРНЫЙ ЧИПСЕТ, ЕСЛИ У ТЕБЯ ДЕСКТОПНЫЙ, ТО ТВОЙ ЕДИНСТВЕННЫЙ ВАРИАНТ ЭТО АНЛОК ТУРБОБУСТА. 
</details>
