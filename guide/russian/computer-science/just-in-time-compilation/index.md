---
title: Just in Time Compilation
localeTitle: Только во время компиляции
---
## Только во время компиляции

Компиляция «точно вовремя» - это метод повышения производительности интерпретируемых программ. Во время выполнения программа может быть скомпилирована в собственный код, чтобы повысить ее производительность. Он также известен как динамическая компиляция.

Динамическая компиляция имеет некоторые преимущества перед статической компиляцией. При запуске приложений Java или C # среда выполнения может профилировать приложение во время его запуска. Это позволяет создавать более оптимизированный код. Если поведение приложения изменяется во время его запуска, среда выполнения может перекомпилировать код.

Некоторые из недостатков включают задержки запуска и накладные расходы компиляции во время выполнения. Чтобы ограничить накладные расходы, многие компиляторы JIT компилируют часто используемые коды кода.

### обзор

Традиционно существует два метода преобразования исходного кода в форму, которая может быть запущена на платформе. Статическая компиляция преобразует код в язык для конкретной платформы. Интерпретатор напрямую выполняет исходный код.

Компиляция JIT пытается использовать преимущества обоих. Пока интерпретируемая программа запускается, компилятор JIT определяет наиболее часто используемый код и компилирует его в машинный код. В зависимости от компилятора это можно сделать по методу или в меньшем разделе кода.

Динамическая компиляция была впервые описана в статье Дж. Маккарти на LISP в 1960 году.

Just In Time Compilation, JIT или Dynamic Translation - это компиляция, выполняемая во время выполнения программы. Значение во время выполнения, в отличие от предшествующего выполнения. Что происходит, это перевод на машинный код. Преимущества JIT связаны с тем, что, поскольку компиляция имеет место во время выполнения, компилятор JIT имеет доступ к динамической информации о времени выполнения, что позволяет ему улучшать оптимизацию (например, встроенные функции).

Что важно понимать в компиляции JIT, заключается в том, что он будет компилировать байт-код в инструкции машинного кода работающей машины. Смысл в том, что полученный машинный код оптимизирован для архитектуры процессора работающего компьютера.

Два примера JIT-компиляторов: JVM (Java Virtual Machine) в Java и CLR (Common Language Runtime), на C #.

## JIT означает Just-in-Time, что означает, что код скомпилируется, когда это необходимо, а не во время выполнения.

Вначале компилятор отвечал за превращение языка высокого уровня (более высокого уровня, чем ассемблер) в объектный код (машинные инструкции), который затем был бы связан (компоновщиком) с исполняемым файлом.

В какой-то момент эволюции языков компиляторы будут компилировать язык высокого уровня в псевдокод, который затем будет интерпретироваться (интерпретатором) для запуска вашей программы. Это устранило объектный код и исполняемые файлы и позволило переносить эти языки на несколько операционных систем и аппаратных платформ. Паскаль (который скомпилирован в P-Code) был одним из первых; Java и C # являются более свежими примерами. В конце концов термин P-Code был заменен байт-кодом, так как большинство псевдо-операций являются байтами длинных.

Компилятор Just-In-Time (JIT) - это функция интерпретатора времени выполнения, который вместо интерпретации байт-кода при каждом вызове метода скомпилирует байт-код в инструкции машинного кода работающей машины и затем вызывает это вместо этого. В идеале эффективность запуска кода объекта будет преодолевать неэффективность перекомпиляции программы каждый раз, когда она запускается.

Компилятор JIT запускается после запуска программы и компиляции кода (обычно байт-кода или каких-либо инструкций VM) «на лету» (или точно в срок, как его называют), в форму, которая обычно быстрее, обычно родной процессор основного процессора набор инструкций. JIT имеет доступ к динамической информации о времени выполнения, тогда как стандартный компилятор не делает и может улучшить оптимизацию, например, часто используемые функции наложения.

Это противоречит традиционному компилятору, который компилирует весь код для машинного языка до того, как программа будет запущена в первый раз.

Чтобы перефразировать, обычные компиляторы строят всю программу как EXE-файл ПЕРЕД первым при ее запуске. Для более новых программ стиля сборка создается с псевдокодом (p-код). Только ПОСЛЕ того, как вы выполняете программу в ОС (например, дважды щелкнув по ее значку), компилятор (JIT) запустит и сгенерирует машинный код (m-код), который процессор Intel или что-то поймет.

## Типичный сценарий:

Исходный код полностью преобразуется в машинный код

## Сценарий JIT:

Исходный код будет преобразован в язык ассемблера, такой как структура \[для ex IL (промежуточный язык) для C #, ByteCode для java\].

Промежуточный код преобразуется в машинный язык только тогда, когда требуется приложение, требуемые коды преобразуются только в машинный код.

## Сравнение JIT и Non-JIT:

В JIT не весь код сначала преобразуется в машинный код, часть необходимого кода будет преобразована в машинный код, а если вызванный метод или функциональность не находится в машине, то это будет превращено в машинный код ... это уменьшает нагрузку на CPU. Поскольку машинный код будет генерироваться во время выполнения .... JIT-компилятор будет генерировать машинный код, оптимизированный для работы архитектуры процессора. Примеры JIT:

В Java JIT находится в JVM (виртуальная машина Java) В C # он находится в CLR (Common Language Runtime) В Android он находится в DVM (Dalvik Virtual Machine) или ART (Android RunTime) в новых версиях.

Java Virtual Machine (JVM) (JVM исполняет байт-код) поддерживает подсчет количества времени выполнения функции. Если этот счет превышает предопределенный предел, JIT компилирует код в машинный язык, который может быть непосредственно выполнен процессором (в отличие от обычного случая, когда javac компилирует код в байт-код, а затем java - интерпретатор интерпретирует этот байт-код по строкам, преобразует его в машинный код и выполняется).

Также в следующий раз, когда эта функция вычисляется, тот же скомпилированный код выполняется снова, в отличие от обычной интерпретации, в которой код интерпретируется снова по строкам. Это ускоряет выполнение.

#### Больше информации

*   [Компиляция JIT (Википедия)](https://en.wikipedia.org/wiki/Just-in-time_compilation)
*   [Введение в JIT](https://eli.thegreenplace.net/2013/11/05/how-to-jit-an-introduction/)