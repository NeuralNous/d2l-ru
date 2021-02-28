# Установка
:label:`chap_installation`

Для того чтобы дать вам возможность практиковаться,
нам нужно настроить ваше окружение,
Jupyter, необходимые библиотеки,
и код необходимый для запуска сам по себе.

## Установка miniconda
Простейший способ установки
[Miniconda](https://conda.io/en/latest/miniconda.html). Необходим Питон 3.x версии. 
Вы можете пропустить эти шаги, если conda уже установлена.
Скачайте соответствующий miniconda sh файл с нашего сайта
и запустите установки из командной строки
используя `sh <FILENAME> -b`. Для пользователей MacOs:

```bash
# The file name is subject to changes
sh Miniconda3-latest-MacOSX-x86_64.sh -b
```


Для пользователей Linux:

```bash
# The file name is subject to changes
sh Miniconda3-latest-Linux-x86_64.sh -b
```


Далее инициализируйте Shell чтобы запускать `conda` напрямую.

```bash
~/miniconda3/bin/conda init
```


Перезапустите Shell. Вы сможете создать новое окружение при помощи
этой команды:

```bash
conda create --name d2l python=3.8 -y
```


## Скачайте d2l ноутбук

Далее нам надо скачать весь код этой книги. Это можно сделать нажав на вкладку "All
Notebooks" на верху каждой HTML страницы, после чего распаковать архив.
В ином случае если у вас есть `unzip` (в ином случае запустите `sudo apt install unzip`):

```bash
mkdir d2l-en && cd d2l-en
curl https://d2l.ai/d2l-en.zip -o d2l-en.zip
unzip d2l-en.zip && rm d2l-en.zip
```


Теперь нам нужно активировать окружение `d2l`.

```bash
conda activate d2l
```


## Устанавливаем пакет `d2l`

Перед установкой фреймворка для глубокого обучения, пожалуйста проверьте
имеется ли у вас подходящая видеокарта
(Интегрированная видеокарта не подойдет для наших целей).
Если у вас всё таки есть Гп, то проследуйте,
на :ref:`subsec_gpu` за интструкциями по установке версии
для видоекарт.

В ином случае вы можете установить версию для процессора.
Этих мощностей будет более чем достаточно для начала, но
лучше вам получить доступ как графическому процессору для
запуска больших моделей.


:begin_tab:`mxnet`

```bash
pip install mxnet==1.7.0.post1
```


:end_tab:


:begin_tab:`pytorch`

```bash
pip install torch torchvision -f https://download.pytorch.org/whl/torch_stable.html
```


:end_tab:

:begin_tab:`tensorflow`
Обе версии как для гп так и для цп устанавливаются этой командой:

```bash
pip install tensorflow tensorflow-probability
```


:end_tab:


Так же мы установим пакет `d2l` который реализует часто используемые функции
в книге .

```bash
# -U: Upgrade all packages to the newest available version
pip install -U d2l
```


Как только всё установлено мы запускаем Jupyter notebook при помощи:

```bash
jupyter notebook
```


С этого моменты вы можете открыть http://localhost:8888 (обычно открывается автоматически) в вашем браузере. Тогда мы сможем запускать код из каждой секции книги.
Всегда запускайте `conda activate d2l` чтобы включить виртуальное окружение
перед запуском кода книги или обновления вашего фреймворка глубокого обучения или `d2l` пакета.
Для выхода из окружения запустите `conda deactivate`.


## Поддержка ГП
:label:`subsec_gpu`

:begin_tab:`mxnet`
По стандарту, MXNet устанавливается без поддержки ГП
для того чтобы быть уверенными в том, что он будет работать на любом компьюетре (включая большинство ноутбуков).
Часть этой книги рекомендуется делать на ГП.
Если в вашем компьютере установлена видеокарта NVIDIA [CUDA](https://developer.nvidia.com/cuda-downloads),
Тогда вы можете установить GPU версию.
Если вы установили CPU версию, то вы можете её удалить используя:

```bash
pip uninstall mxnet
```


Теперь нам нужно найти вашу версию CUDA.
Её можно проверить при помощи `nvcc --version` или `cat /usr/local/cuda/version.txt`.
Предположим у вас CUDA 10.1,
тогда для установки используйте следующую команду:

```bash
# For Windows users
pip install mxnet-cu101==1.7.0 -f https://dist.mxnet.io/python

# For Linux and macOS users
pip install mxnet-cu101==1.7.0
```


Вы можете изменить последние цифры в соответствии с вашей версией куда, например `cu100` для
CUDA 10.0 и `cu90` для CUDA 9.0.
:end_tab:


:begin_tab:`pytorch,tensorflow`
По стандарту, MXNet устанавливается с поддержкой ГП.
IЕсли в вашем компьютере установлена видеокарта NVIDIA [CUDA](https://developer.nvidia.com/cuda-downloads),
тогда у вас всё готово.
:end_tab:

## Упражнения

1. Скачайте код книги и установите окружение.

:begin_tab:`mxnet`
[Discussions](https://discuss.d2l.ai/t/23)
:end_tab:

:begin_tab:`pytorch`
[Discussions](https://discuss.d2l.ai/t/24)
:end_tab:

:begin_tab:`tensorflow`
[Discussions](https://discuss.d2l.ai/t/436)
:end_tab:
