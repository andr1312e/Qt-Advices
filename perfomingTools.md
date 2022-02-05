ВИНДА:
Вертикальные линии обозначают столбцы.

* Very Sleepy — это бесплатный профилировщик процессов C/C++ для систем Windows. - Скачать http://www.codersnotes.com/sleepy/.

![image](https://user-images.githubusercontent.com/22058642/152636162-16a5b448-ffc7-487c-a33c-d9d678d2e2be.png)

Как юзать: http://supercomputingblog.com/windows/how-to-profile-c-code-in-visual-studio-for-free/
 
* MD CodeXL. еще один профилировщик от АМД с открытым исходным кодом. У него гораздо более богатый пользовательский интерфейс, чем у Very Sleepy. Он поддерживает отладку GPU, анализ кадров, GPU профилирование, анализ шейдеров и профилирование мощности и еще всяко разное кощунство. Есть на хабре статьи https://habr.com/ru/search/?q=%5Bcodexl%5D&target_type=posts. Собирать не надо, качаем с релизов гитхаба. Есть в аддонах вижлы.

 https://github.com/GPUOpen-Archive/CodeXL/releases/tag/v2.6
 
https://developer.amd.com/wordpress/media/2012/10/CodeXL_Quick_Start_Guide.pdf - стартовый гайд

* Люк Стэкуокер (http://lukestackwalker.sourceforge.net/) гораздо лучший пользовательский интерфейс, чем Very Sleepy, и доступен для Windows, но
к сожалению, он поддерживает только отладочную информацию компилятора Microsoft. Уступает проге выше. Кому то может и пригнянется

![image](https://user-images.githubusercontent.com/22058642/152636444-9e6e46fe-b969-46a0-bd0d-55d0eb451f25.png)

* По пямяти. Здесь, я должен признать, у нас нет хорошего инструмента профилирования памяти с открытым исходным кодом сравнимо с Valgrind's Massif в Linux, который может показать использование памяти трассировать и атрибутировать части используемой памяти.
Мы можем получить общий обзор используемой памяти через Sysinternal, но чтобы увидеть, что потребляет память, нам пришлось бы использовать программу инструмент, как GammaRay. Еще инструменты для Windows - heob, который даже интегрирован с Qt Creator или Dr. Memory.

* RAMMap — бесплатная утилита, разработанная Марком Руссиновичем и Брайсом Когсвеллом из компании Sysinternals. Качаем:
https://docs.microsoft.com/en-us/sysinternals/downloads/rammap. Там же и как юзать.

![image](https://user-images.githubusercontent.com/22058642/152636632-777aa55f-f811-402e-a385-dcf4453d3640.png)

* Гамма рей статья о том как и что https://habr.com/ru/company/infopulse/blog/258411/. Бинарников под Windows нет. Исходники здесь: https://github.com/KDAB/GammaRay. Для сборки под Windows мне понадобилось поправить файл CMakeLists.txt.


