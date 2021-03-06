# Введение

Буквально пару лет назад не было легионов специалистов по глубокому обучению
разрабатывающих интеллектуальные системы и сервисы в больших компаниях и стартапах.
Когда самый молодый из авторов попал в эту сферу, машинное обучение
не показывалось в заголовках ежедневных газет.
Наши родители не имели представление что такое машинное обучение,
не говоря уже о том почему мы предпочли его медицине или закону.
Машинное обучение было перспективной академической дисциплиной с 
большим количеством применений в реальной жизни.
И эти применения, такие как распознавание речи или компьютерное зрение 
требовали так много знаний в предметной области, что рассматривались отдельно, 
будто машинное обучение это просто маленькая часть этого.
Затем нейронные сети, предпосылки моделей глубого обучения.
То на чём мы остановимся в книге считалось устаревшим инструментом


В последние 5 лет глубокое обучение застало мир врасплох, стремительный прогресс в таких разнообразных 
областях, как компьютерное зрение, обработка естественного языка, автоматическое распознавание речи, 
обучение с подкреплением и статистическое моделирование. С этими достижениями в руках теперь мы 
можем делать машины с автопилотом с таким количеством автоматизации котороый не было никогда.
(и меньшее количество автоматизации в которое некоторые компании могут заставить вас поверить)
интеллектуальные системы ответов, которые автоматически составляют самые обыденные электронные письма,
помогающие людям разгребять угнетающе большие почтовые аккануты,
и программные агенты которые перегоняют людей в таких сферах как Го, Шахматы. Что считалось невероятным пару
десятков лет назад. Уже эти инструменты оказывают все большее влияние на производство и общество, меняя то как
создаются фильмы, и диагнозируются заболевания. Так же тяжело отрицать их растущую роль в фундаментальных науках
от астрофизики до биологии.


## Об этой книге

Эта книга представляет нашу попытку сделать глубокое обучение доступным,
обучая вас *концептам*, *контексту* и *программированию*.

### Единое место объединяющее код, математику и Html

Чтобы любая вычислительная технология достигла своего полного эффекта,
она должена быть хорошо понятена, хорошо документирована и поддерживаться
умелыми специалистами с хорошо поддерживаемыми инструментами
Ключевые идеи должны быть четко сформулированы,
тем самы сводя к минимуму времени на адаптацию, необходимого для того, чтобы ввести новых практикующих в курс дела.
Фреймворки и серьёзные библиотеки должны автоматизировать стандартные задачи,
и примеры кода должны упростить задачу для новичков, чтобы они могли без особого труда
изменять, применять и расширять распространенные приложения в соответствии с потребностями.
Возьмем в качестве примера динамические веб-приложения.
Несмотря на большое количество компаний, таких как Amazon,
разрабатывающих успешные веб-приложений основывающихся на базах данных в 1990-е годы,
потенциал этой технологии за последние десять лет был раскрыт большей степени,
отчасти благодаря разработке мощных, хорошо документированных фреймворков.


Приложение потенциала глубокого обучения представляет собой уникальное
испытание, ибо любое приложение соединяет различные дисциплны.
Приложение глубокого обучения требует одновременного понимания
(i) постановку задачи определённым образом;
(ii) математическую основу конкретного подхода;
(iii) оптимизационные алгоритмы для обучения модели;
и (iv) технические навыки для эффективного обучения,
понимание численных методов и полчение максимума из доступного железа.
Навыки критического мышления, необходимы для формулирования проблем,
математика для их решения, программные инструменты для реализации этих
решений. Воссоединение всего этого представляет собой серьёзное испытание.
Цель этой книги представить общий ресурс для того чтобы ввести будущих практиков
в курс дела.

В то время когда мы начинали этот проект не было ресурсов
которые бы:
(i) являлись актуальными; (ii) охватывали весь спектр
современного машинного обучения с достаточной технической глубиной;
и (iii) чередовала бы теорию с практическими реализациями.
Мы нашли множество примеров кода на тех или иных
фреймворках глубокого обучения
(например, как сделать базовые вычисления с матрицами в TensorFlow)
или для реализации конкретных методов
(например, фрагменты кода для LeNet, AlexNet, ResNets и т. Д)
разбросанные по различным постам в блогах и репозиториям GitHub.
Однако эти примеры обычно основаны на том как реализовать
тот или иной механизм, но они не иллюстрируют то зачем определённые
алгоритмические решения были сделаны.
В то время как некоторые интерактивные ресурсы появлялись от случая к случаю, 
чтобы описать к определенную тему, например, привлекательные сообщения в блогах, 
опубликованным на веб-сайте Distill, или личные блоги, охватывают только отдельные темы в глубоком обучении
и часто не имели связи друг с другом.
опубликовано на вебсайте [Distill](http://distill.pub), или личных блогах,
они касались только отдельных тем в глубоком обучении,
и часто не имело программных реализаций.
С другой стороны, появилось несколько учебников,
самый заметний из которых :cite:`Goodfellow.Bengio.Courville.2016`,
который предлагает всесторонний обзор концепций, лежащих в основе глубокого обучения,
эти ресурсы не имеют подходящего описания
для реализации материала в коде,
иногда оставляя читателей в неведении относительно того, как их реализовать.
Более того крайне большое количество ресурсов имеют продавцы курсов.

Мы задались целью создать ресурс, который мог бы
(i) быть свободно доступным для всех;
(ii) предложить достаточную техническую глубину, чтобы обеспечить отправную точку на пути к тому,
чтобы действительно стать прикладным специалистом по машинному обучению;
(iii) включать запускаемый код, показывающий читателям способы решать проблемы на практике;
(iv) быть доступным для быстрого изменения как нами так и сообществом в целом.
и (v) дополнятся [форумом](http://discuss.d2l.ai)
для обсуждения технических деталей и ответов на вопросы.

Эти цели часто противоречили друг другу.
Уравнения, теоремы и цитаты лучше всего оформлялись при помощи LaTeX.
Код лучше всего описывался питоном.
А сайт на чистом HTML и JavaScript.
Кроме того, мы хотим, чтобы контент был
доступен как в виде исполняемого кода, так и в виде физической книги
как загружаемый пдф файл и доступный веб версия.
В настоящее время не существует инструментов идеально подходящих 
для этих требований, поэтому нам пришлось создать свои собственные.
Мы подробно описываем наш подход в :numref:`sec_how_to_contribute`.
Мы создали проект на GitHub, чтобы поделиться исходным кодом и разрешить правки,
Jupyter файлы для смешывания кода, уравнений и текста,
Sphinx как движок рендеринга для генерации.
и Discourse для форума.
Пока наша система не идеально,
эти решения являются хорошим компромисом между конкурирующими проблемами.
Мы считаем, что это может быть первая книга, опубликованная с использованием такого
рабочего процесса.



### Обучение на практике

Многие учебники преподают ряд тем, каждая из которых исчерпывающе детализирована.
Например, отличный учебник Криса Бишопа :cite:`Bishop.2006`,
обучает каждой теме настолько тщательно, что для того чтобы добраться до главы
с линейной регрессией требуется немалое количестов работы.
Пока эксперты любят эту книгу за её доскональность, для новичков
это свойство ограничивает возможности этой книги как вводный материал.

В этой книге мы будем изучать большинство концептов прямо тогда
когда они понадобятся для практических целей.
В то же время для самого начала в любом случае придётся уяснить некоторые
базовые понятия такие как: Линейная алгебра и теория вероятности.
Мы хотим чтобы вы почувствовали вкус удовольствия от обучения вашей первой
модели прежде чем беспокоиться о более сложных распределениях вероятностей.

Помимо нескольких предварительных частей, которые обеспечивают ускоренный курс
в основную математическую базу каждая последующая глава вводит
как разумное количество новых концепций, так и предоставляет отдельные 
практические примеры с использованием реальных наборов данных.
Некоторые модели можно логически сгруппировать в одной части.
А некоторые идеи лучше всего показывать подряд.
С другой стороны, есть большое преимущество в том, чтобы придерживаться
политики *один рабочий пример, одна записная книжка*:
Это позволяет вам максимально легко начать свои собственные исследовательские проекты, используя наш код.
Просто скопируйте код и начните его изменять.

Мы будем чередовать код с текстовым материалом по мере необходимости.
В общем, мы часто ошибаемся, используя инструменты, 
прежде чем объяснить их полностью.
Например, мы могли бы использовать *стохастический градиентный спуск*
, прежде чем полностью объяснить, почему он полезен или почему он работает.
Это помогает дать практикующим необходимую
амуницию для быстрого решения проблем,
за счет того, что читатель может положится на нас в использовании решений.

Эта книга обучит концепциям глубокого обучения с нулля.
Иногда мы хотим углубится в в детали скрытые от пользователя
высокоуровневыми абстракциями реализованными в фреймворке.
Это особенно актуально в базовых частях книги,
где мы хотим, чтобы вы все поняли
что именно происходит в данном слое или оптимизаторе.
В этих случаях мы представялем две версии: одна написанная с нуля, 
а вторая с использованием высокоуровневого апи фреймворка.
После того, как мы объяснили вам, как работает какой-либо компонент, 
далее мы можем просто использовать высокоуровневые API.


### Контент и структура

Книга может быть грубо разделена на три части,
которые представлены различными цветами в :numref:`fig_book_org`:

![Структура книги](../img/book-org.svg)
:label:`fig_book_org`


* Первая часть покрывать основы и необходимую для понимания 
информацию.:numref:`chap_introduction` 
предлагает введение в глубокое обучение.
Затем в :numref:`chap_preliminaries`,
мы быстро расскажем о необходимой информации для практики глубокого
обучения. Например о том как хранить и управлять данными и как
прилагать различные операции основываюсь на концепициях из
линейной алгебры, математического анализи и теории вероятности.
:numref:`chap_linear` и :numref:`chap_perceptrons`
покрывает самые основные техники и идеи из машинного обучения,
такие как линейная регрессия, многослойный перцептрон и регуляризация.

* Следующие пять глав рассказывают о современных идеях в машинном обучении.
:numref:`chap_computation` описывает различные ключевые вещи в глубоком обучении
обучение расчётам и основы позволят нам в будущем 
реализовывать более сложные модели.
Далее в :numref:`chap_cnn` и :numref:`chap_modern_cnn`,
мы приступим к свёрточным нейронным сетям (CNNs), мощным инструментам
которые формируют хребет современных систем компьютерного зрения.
Потом в:numref:`chap_rnn` и :numref:`chap_modern_rnn`, 
мы доходим до рекурентных нейронных сетей(RNNs), модели, использующие
временную или последовательную структуру данных, и зачастую используемые в 
прогнозировании временных рядов и работе в обработке языка.
В :numref:`chap_attention`, мы демонстрируем новый класс моделей
которые полагаются на технику называемую механизмом внимания,
они только недавно начали замещать рекурентные нейронные сети в обработке языка.
Эти разделы помогут вам быстро освоить основные инструменты, 
лежащие в основе большинства современных приложений глубокого обучения.


* В части три берётся во внимание масштабирование, эффективность, и приложения.
Во Первых, в :numref:`chap_optimization`,
мы обсуждаем различные оптимизационные алгоритмы позволяющие обучать модели.
В следующей части, :numref:`chap_performance` исследуется несколько ключевых факторов
, влияющих на производительность вашего кода.
В :numref:`chap_cv`,
проиллюстрируем основные области применения
глубокого обучения в компьютерном зрении.
В :numref:`chap_nlp_pretrain` и :numref:`chap_nlp_app`,
мы покажем, как предварительно обучить языковые модели представления и применить
их к задачам обработки естественного языка.


### Код
:label:`sec_code`

Большинство секций этой книги представляют запускаемый код из-за нашей веры
в важность получения практических навыков в глубоком обучении.
В настоящее время часть понятий может быть усвоена только путем проб и ошибок.
Немного изменяя код и наблюдая за результатами. В лучшем случае элегантная математическая теория
может сказать нам точно как нужно изменить код для получения желамых результатов.
К сожалению, в настоящее время такие изящные теории ускользают от нас.
Несмотря на наши лучшие попытки, формальные объяснения некоторых техник ещё отсутсвую
по причине сложнейшей математической базы лежащей за этими моделями, а так же 
по причине их новизны. Мы надеемся что по ходу развития глубокого обучения
будущие издания этой книги будут способны предложить объяснения там, где 
сейчас их нет.
Временами во избежание излешнего повторения мы создаем часто
используемые классы, функции и тд в d2l пакет.
Любой объект который будет сохранен в наш пакет будет отмечен соответсвующим образом
`#@save`. Мы предлагаем подробный обзор этих функций и классов в :numref:`sec_d2l`.
`d2l` пакет легковесный и требует только следующие зависимости:

```{.python .input}
#@tab all
#@save
import collections
from collections import defaultdict
from IPython import display
import math
from matplotlib import pyplot as plt
import os
import pandas as pd
import random
import re
import shutil
import sys
import tarfile
import time
import requests
import zipfile
import hashlib
d2l = sys.modules[__name__]
```

:begin_tab:`mxnet`
Большая часть кода в этой версии написана на Apache MXNet.
MXNet это открытый фреймворк для глубокого обучения
этот фреймворк используется в AWS (Amazon Web Services),
и также большим количеством компаний и сотрудников.
Весь этот код проходит тесты на последней версии MXNet.
Но из-за скоростного развития глубокого обучения и фреймворков в частности
*код в печатной версии* может работать не совсем корректно в последних версиях MXNet.
Но мы всё равно планируем держать веб версию в актуальном состоянии.
В случае если вы встретите какую-то проблему,
пожалуйста донесите :ref:`chap_installation`
чтобы обновить код и виртуальное окружение.

Вот как мы импортируем модули для MXNet.
:end_tab:

:begin_tab:`pytorch`
Большая часть кода в этой версии написана на pytorch.
MXNet это открытый фреймворк для глубокого обучения
этот фреймворк безумно популярен среди исследователей,
и также используется большим количеством компаний и сотрудников.
Весь этот код проходит тесты на последней версии pytorch.
Но из-за скоростного развития глубокого обучения и фреймворков в частности
*код в печатной версии* может работать не совсем корректно в последних версиях pytorch.
Но мы всё равно планируем держать веб версию в актуальном состоянии.
В случае если вы встретите какую-то проблему,
пожалуйста донесите :ref:`chap_installation`
чтобы обновить код и виртуальное окружение.

Вот как мы импортируем модули для pytorch.
:end_tab:

:begin_tab:`tensorflow`
Большая часть кода в этой версии написана на tensorflow.
MXNet это открытый фреймворк для глубокого обучения
этот фреймворк безумно популярен среди исследователей и бизнеса,
и также используется большим количеством компаний и сотрудников.
Весь этот код проходит тесты на последней версии tensorflow.
Но из-за скоростного развития глубокого обучения и фреймворков в частности
*код в печатной версии* может работать не совсем корректно в последних версиях tensorflow.
Но мы всё равно планируем держать веб версию в актуальном состоянии.
В случае если вы встретите какую-то проблему,
пожалуйста донесите :ref:`chap_installation`
чтобы обновить код и виртуальное окружение.

Вот как мы импортируем модули для tensorflow.
:end_tab:

```{.python .input}
#@save
from mxnet import autograd, context, gluon, image, init, np, npx
from mxnet.gluon import nn, rnn
```

```{.python .input}
#@tab pytorch
#@save
import numpy as np
import torch
import torchvision
from torch import nn
from torch.nn import functional as F
from torch.utils import data
from torchvision import transforms
from PIL import Image
```

```{.python .input}
#@tab tensorflow
#@save
import numpy as np
import tensorflow as tf
```

### Целевая аудитория

Эта книга для студентов (закончивших или ещё получающих высшее образование),
инженеров, и исследователей, ищущих хороший ресурс для обучения
практическим техникам глубокого обучения.
Именно поэтому мы объсняем каждый пример с нуля,
никакого опыта в машинном обучении не требуется.
Полное понимание методов машинного обучения требует определённые знания
по математике и программированию,
но мы просто предполагаем, что вы уже обладаете этими навыками,
включая (самые основы) линейная алгебра, математический анализ, теория веорятности,
и программирование на языке питон.
Кроме того, в Приложении мы предлагаем освежить
большую часть математики, используемой в этой книге.
Большую часть времени мы будем отдавать предпочтение интуиции и идеям, 
а не математической строгости.
Есть много потрясающих книг позволяющих углубиться в интересующую тематику.
Например, Linear Analysis by Bela Bollobas :cite:`Bollobas.1999`
охватывает линейную алгебру и функциональный анализ.
All of Statistics :cite:`Wasserman.2013` это потрясный гайд по статистике.
И если вы никогда не использовали питон раньше,вы
можете использовать этот ресурс[Python tutorial]( http://learnpython.org/).


### Форум

В связи с этой книгой мы запустили тематический форум
[discuss.d2l.ai](https://discuss.d2l.ai/).
Когда у вас возникнут вопросы по любой части этой книги
вы сможете найти ссылку на соответсвующую страницу в конце
каждого эпизда.


## Благодарности

Мы в долгу перед сотниями вкладчиков для английской и китайской версии.
Они помогли улучшить контент и предложить ценные замечания.
В частности, мы благодарим каждого автора английской версии за то что сделали
её лучше для всех.
Их GitHub IDs или имена (в случайном порядке):
alxnorden, avinashingit, bowen0701, brettkoonce, Chaitanya Prakash Bapat,
cryptonaut, Davide Fiocco, edgarroman, gkutiel, John Mitro, Liang Pu,
Rahul Agarwal, Mohamed Ali Jamaoui, Michael (Stu) Stewart, Mike Müller,
NRauschmayr, Prakhar Srivastav, sad-, sfermigier, Sheng Zha, sundeepteki,
topecongiro, tpdi, vermicelli, Vishaal Kapoor, Vishwesh Ravi Shrimali, YaYaB, Yuhong Chen,
Evgeniy Smirnov, lgov, Simon Corston-Oliver, Igor Dzreyev, Ha Nguyen, pmuens,
Andrei Lukovenko, senorcinco, vfdev-5, dsweet, Mohammad Mahdi Rahimi, Abhishek Gupta,
uwsd, DomKM, Lisa Oakley, Bowen Li, Aarush Ahuja, Prasanth Buddareddygari, brianhendee,
mani2106, mtn, lkevinzc, caojilin, Lakshya, Fiete Lüer, Surbhi Vijayvargeeya,
Muhyun Kim, dennismalmgren, adursun, Anirudh Dagar, liqingnz, Pedro Larroy,
lgov, ati-ozgur, Jun Wu, Matthias Blume, Lin Yuan, geogunow, Josh Gardner,
Maximilian Böther, Rakib Islam, Leonard Lausen, Abhinav Upadhyay, rongruosong,
Steve Sedlmeyer, Ruslan Baratov, Rafael Schlatter, liusy182, Giannis Pappas,
ati-ozgur, qbaza, dchoi77, Adam Gerson, Phuc Le, Mark Atwood, christabella, vn09,
Haibin Lin, jjangga0214, RichyChen, noelo, hansent, Giel Dops, dvincent1337, WhiteD3vil,
Peter Kulits, codypenta, joseppinilla, ahmaurya, karolszk, heytitle, Peter Goetz, rigtorp,
Tiep Vu, sfilip, mlxd, Kale-ab Tessera, Sanjar Adilov, MatteoFerrara, hsneto,
Katarzyna Biesialska, Gregory Bruss, Duy–Thanh Doan, paulaurel, graytowne, Duc Pham,
sl7423, Jaedong Hwang, Yida Wang, cys4, clhm, Jean Kaddour, austinmw, trebeljahr, tbaums,
Cuong V. Nguyen, pavelkomarov, vzlamal, NotAnotherSystem, J-Arun-Mani, jancio, eldarkurtic,
the-great-shazbot, doctorcolossus, gducharme, cclauss, Daniel-Mietchen, hoonose, biagiom,
abhinavsp0730, jonathanhrandall, ysraell, Nodar Okroshiashvili, UgurKap, Jiyang Kang,
StevenJokes, Tomer Kaftan, liweiwp, netyster, ypandya, NishantTharani, heiligerl, SportsTHU,
Hoa Nguyen, manuel-arno-korfmann-webentwicklung, aterzis-personal, nxby, Xiaoting He, Josiah Yoder,
mathresearch, mzz2017, jroberayalas, iluu, ghejc, BSharmi, vkramdev, simonwardjones, LakshKD,
TalNeoran, djliden, Nikhil95, Oren Barkan, guoweis, haozhu233, pratikhack, 315930399, tayfununal,
steinsag, charleybeller, Andrew Lumsdaine, Jiekui Zhang, Deepak Pathak, Florian Donhauser, Tim Gates,
Adriaan Tijsseling, Ron Medina, Gaurav Saha, Murat Semerci, Lei Mao, Levi McClenny, Joshua Broyde,
jake221, jonbally, zyhazwraith, Brian Pulfer, Nick Tomasino.

Мы благодарим Amazon Web Services, especially Swami Sivasubramanian,
Raju Gulabani, Charlie Bell, и Andrew Jassy за их щедрую помощь в написании этой книги. Без времени, ресурсов 
и постоянного поощрения эта книга не вышла бы


## Итог

* Глубокое обучение произвело революцию в распознавании образов, внедрив технологию, которая теперь поддерживает широкий спектр областей, включая компьютерное зрение, обработку естественного языка, автоматическое распознавание речи.
* Чтобы успешно применять глубокое обучение, вы должны понимать, как сформулировать задачу, математику моделей, алгоритмы обучения ваших моделей на данным и технические методы для реализации всего этого.
* Эта книга представляет собой исчерпывающий ресурс, включающий в себя идеи, иллюстрации, математику и код, все в одном месте
* Чтобы получить ответы на вопросы можете посетить наш форум https://discuss.d2l.ai/.
* Все материалы доступны на GitHub.


## Упражнения

1. Зарегистрируйте аккаунт на сайте дискуссий этой книги [discuss.d2l.ai](https://discuss.d2l.ai/).
1. Установите питон на ваш компьютер.
1. Проследйте по ссылкам ниже на форум, где вы сможете найти помощь и обсудить книгу, и найти ответы на ваши вопросы вовлекая широкое сообщество и авторов.

:begin_tab:`mxnet`
[Discussions](https://discuss.d2l.ai/t/18)
:end_tab:

:begin_tab:`pytorch`
[Discussions](https://discuss.d2l.ai/t/20)
:end_tab:

:begin_tab:`tensorflow`
[Discussions](https://discuss.d2l.ai/t/186)
:end_tab:
