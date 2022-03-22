---
title: Скрипт для обработки пустых директорий
desc: Скрипт выполняет команды для каждой найденной пустой директории.
---
# Цикл для пустых директорий

Скрипт **Цикл для пустых директорий** ищет пустые директории и выполняет вложенные команды для каждой найденной пустой директории.

%html.foreach-empty-dir%

**Путь**  
Укажите директорию, в которой нужно искать пустые директории.

**Маска или регулярное выражение**  
**Исключать по маске или рег.выраж.**  
Эти параметры описаны в команде [Цикл для каждого файла](/ru/scripts/foreach-file.html).

**Имя переменной**  
Укажите имя переменной, которой будет присвоен полный путь найденной пустой директории. Вы можете использовать эту переменную во вложенных командах.