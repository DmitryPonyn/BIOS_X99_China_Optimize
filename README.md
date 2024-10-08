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
Заходим по первой [ссылке](https://github.com/Koshak1013/HuananzhiX99_BIOS_mods/tree/master) на гитхаб кошака и ищем свою материнскую плату. Если твоей платы там нет, то можно перейти в ТГ который указан в гитхабе кошака и попросить разлочить в нём настройки таймингов(если таковых не имеется в стоковом биосе). 

Можно столкнуться с тем что у платы несколько ревизий и биос от одной может не подойти к другой. Как в этом примере:
![](https://github.com/DmitryPonyn/BIOS_X99_China_Optimize/blob/main/images/BIOS_rev.png)

В таком случае нужно осмотреть материнскую плату на наличее надписи Ver и исходя из неё выбрать нужную версию биоса. Если надписи такой нет, то нужно зайти на [xeon-e5450.ru](xeon-e5450.ru) и в выпадающем списке вверху "2011-3" выбрать свою материнскую плату и там будет как различить разные ревизии.
