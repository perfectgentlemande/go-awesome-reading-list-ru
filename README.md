# go-awesome-reading-list-ru
Список Must Read статей по Go. 
Для всех golang-разработчиков, которые хотят перестать быть code-monkey и стать синьор помидорами.
Не все и не всем бывает сразу понятно и очевидно, поэтому уровень статей вариьируется от примитивных до не очень.

## Типы данных под капотом

### Как не наступать на грабли в Go
https://habr.com/ru/post/325468/ - хорошее и простое описание того, как устроены под капотом массивы, слайсы, интерфейсы

### Golang slice append gotcha
https://medium.com/@Jarema./golang-slice-append-gotcha-e9020ff37374 - интересный пример граблей аппенда в слайс, важно для понимания работы слайса. Толкового объяснения происходящего конкретно в этой статье нет, но если прочитать предыдущую статью выше, можно понять, что происходит :D

### Хэш таблицы в Go. Детали реализации
https://habr.com/ru/post/457728/ - весьма подробное описание того, как же устроены мапы, что такое бакеты и как в мапе работает поиск

### How the Go runtime implements maps efficiently (without generics)
https://dave.cheney.net/2018/05/29/how-the-go-runtime-implements-maps-efficiently-without-generics - более подробное описание того, как устроены мапы

### Strings In Go's Runtime
https://boakye.yiadom.org/go/strings/ - как реализован тип данных string

### Runes and character encoding
https://yourbasic.org/golang/rune/ - что такое руны

### unsafe.Pointer and system calls
https://blog.gopheracademy.com/advent-2017/unsafe-pointer-and-system-calls/ - кое-что об использовании unsafe.Pointer с примерами применения

## Конкурентность в Go

Важно понимать, что главной характерной особенностью языка Go является работа с конкуретностью.
Конкурентный код писать и отлаживать, как мне кажется, тяжелее, однако ниже приведены статьи, которые я бы порекомендовал прочитать для того, чтобы проще было работать с конкурентностью.

### Параллельное программирование в Go
https://proglib.io/p/parallelnoe-programmirovanie-v-go-2021-05-23 - по большей части обзорная статья с простыми примерами использования горутин, каналов, мьютексов и.т.д. Полезно для тех, кто очень редко сталкивался с многопоточностью и не знает, как правильно пользоваться перечисленными фичами.

### Конкурентность в Golang и WorkerPool
https://proglib.io/p/parallelizm-v-golang-i-workerpool-chast-1-2020-12-24
https://proglib.io/p/parallelizm-v-golang-i-workerpool-chast-2-2020-12-26 - статьи на тему того, как построить пул обработчиков (он же Worker Pool). Я бы не сказал, что конкретно эти пулы - идеальное решение (в первой статье мне не понравилась обработка ошибок в конце), но для ознакомления подойдет. Но я бы не советовал начинать изучение пулов именно с этих статей. Во второй части мне не понравилась остановка пула, это проще сделать через сигнальный канал struct{}, а именно через его закрытие. Примеры такого способа (правда в рамках конвейеров) есть в статье `Go concurrency patterns` выше.

### Анатомия каналов в Go
https://habr.com/ru/post/490336/ - отличная статья для того, чтобы научиться работать с каналами и горутинами. Особенность данной статьи: плавный рост сложности примеров. Маленькие примеры, я считаю, это хорошо, особенно на начальных этапах изучения.

Важные момент: стоит понимать разницу между конкурентностью и параллелизмом. 
Конкурентность в Golang не гарантирует параллелизма выполнения задач под капотом. 
В статье ниже это раскрывается.

### Understanding Golang and Goroutines
https://medium.com/technofunnel/understanding-golang-and-goroutines-72ac3c9a014d - статья на тему конкурентности и параллельности выполнения. Помогает понять разницу между этими понятиями а так же объясняет, почему работа с разными горутинами не гарантирует параллельность выполнения.

### Go concurrency patterns
https://blog.golang.org/pipelines - статья на тему паттернов конкуретности. Показаны простые примеры, благодаря которым можно понять как правильно пользоваться каналами и горутинами на примере конвейеров.


## Выделение памяти (пока не сортировал и не описывал)

### Механизмы выделения памяти в Go
https://m.habr.com/ru/company/ruvds/blog/442648/

### GO SCHEDULER: MS, PS & GS
https://povilasv.me/go-scheduler/

### GO memory ballast
https://medium.com/clean-code-channel/go-memory-ballast-dec0c04830b1

### Go: Должен ли я использовать указатель вместо копии моей структуры?
https://habr.com/ru/post/490570/

### Understanding Allocations in Go
https://medium.com/eureka-engineering/understanding-allocations-in-go-stack-heap-memory-9a2631b5035d

## Прочее

### Go Traps
https://go-traps.appspot.com/#watchman - типичные ошибки и грабли гоферов

### 50 Shades of Go: Traps, Gotchas, and Common Mistakes for New Golang Devs
http://devs.cloudimmunity.com/gotchas-and-common-mistakes-in-go-golang/index.html - типичные ошибки и грабли гоферов

### 7 Code Patterns in Go I Can’t Live Without
https://betterprogramming.pub/7-code-patterns-in-go-i-cant-live-without-f46f72f58c4b - 7 трюков и паттернов гошного кода. Примеры: использование мапы в качестве множества (map[keyType]struct{}), использование сигнального канала (chan struct{}, однако в большинстве случаев на практике лучше использовать context.Done()). Есть и другие полезные примеры.
