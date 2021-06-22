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

## Конкурентность в Go

### Параллельное программирование в Go
https://proglib.io/p/parallelnoe-programmirovanie-v-go-2021-05-23 - по большей части обзорная статья с простыми примерами использования горутин, каналов, мьютексов и.т.д. Полезно для тех, кто очень редко сталкивался с многопоточностью и не знает, как правильно пользоваться перечисленными фичами.

### Understanding Golang and Goroutines
https://medium.com/technofunnel/understanding-golang-and-goroutines-72ac3c9a014d - статья на тему конкурентности и параллельности выполнения. Помогает понять разницу между этими понятиями а так же объясняет, почему работа с разными горутинами не гарантирует параллельность выполнения.

### Go concurrency patterns
https://blog.golang.org/pipelines - статья на тему паттернов конкуретности. Показаны простые примеры, благодаря которым можно понять как правильно пользоваться каналами и горутинами на примере конвейеров.

## Прочее

### Go Traps
https://go-traps.appspot.com/#watchman - типичные ошибки и грабли гоферов

### 50 Shades of Go: Traps, Gotchas, and Common Mistakes for New Golang Devs
http://devs.cloudimmunity.com/gotchas-and-common-mistakes-in-go-golang/index.html - типичные ошибки и грабли гоферов

