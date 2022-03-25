---
title: Одинаковые файлы
desc: Скрипт находит одинаковые файлы и сохраняет их в файл.
---
# Одинаковые файлы

Скрипт **Одинаковые файлы** ищет одинаковые файлы в указанной директории и всех поддиректориях. Файлы считаются одинаковыми, если у них равен размер и **MD5** хэш. Команда сохраняет информацию о найденных файлах в текстовый файл формата YAML, JSON, CSV или HTML. 

%html.duplicate-file-finder%

**Путь**  
Укажите директорию, в которой нужно искать одинаковые файлы. Одинаковые файлы будут искаться во всех поддиректориях.

**Маска или регулярное выражение**  
**Исключать по маске или рег.выраж.**  
Эти параметры описаны в команде [Цикл для каждого файла](/ru/scripts/foreach-file.html).

**Файл вывода**  
Укажите имя файла, в который будет сохраняться информация о найденных файлах. Если расширение файла равно *yaml*, *json*, *html*, то список файлов будет сохранён в соответствующем формате. Например, фрагмент YAML файла:

```yaml
- size: 1890
  md5: "ae9d4728d7113094397b29c5001384ae",
  list":
     - "/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.66.2/testdata/full.ini"
     - "/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.62.0/testdata/full.ini"
     - "/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.64.0/testdata/full.ini"
- size: 8943
  md5: "17faebcd8a80fc6ffff1fad0b3bc2473",
  list":
     - "/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.62.0/testdata/multiline.ini"
     - "/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.64.0/testdata/multiline.ini"
```

Если файл имеет другое расширение или расширение отсутствует, то информация будет сохранена в CSV формате. Например:

```txt
1890,ae9d4728d7113094397b29c5001384ae,/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.66.2/testdata/full.ini
1890,ae9d4728d7113094397b29c5001384ae,/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.62.0/testdata/full.ini
1890,ae9d4728d7113094397b29c5001384ae,/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.64.0/testdata/full.ini
8943,17faebcd8a80fc6ffff1fad0b3bc2473,/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.62.0/testdata/multiline.ini
8943,17faebcd8a80fc6ffff1fad0b3bc2473,/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.64.0/testdata/multiline.ini
```

Если **Файл вывода** не указан, то будет создан и показан отчет о найденных одинаковых файлах.

%html.duplicate-file-report%
