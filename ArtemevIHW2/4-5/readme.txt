1) Работу выполнил студент группы 227 Артемьев Александр Вячеславович
2) Вариант 1
Задача о парикмахере. В тихом городке есть парикмахерская. Салон парикмахерской мал, работать в нем нем может
только один парикмахер, обслуживающий одного посетителя. Есть несколько стульев для ожидания в очереди.
Парикмахер всю жизнь обслуживает посетителей. Когда в салоне никого нет, он спит в кресле. Когда посетитель приходит
и видит спящего парикмахера, он будет его, садится в кресло, и сидит в нем, пока парикмахер обслуживает его.
Если посетитель приходит, а парикмахер занят, то он встает в очередь, садится на свободный стул и «засыпает».
После стриж- ки парикмахер сам провожает посетителя. Если есть ожидающие посетители, то парикмахер будит одного
из них, ждет пока тот сядет в кресло парикмахера и начинает стрижку. Если никого нет, он снова садится в свое
кресло и засыпает до прихода посетителя. Количество стульев для ожидания в очереди ограничено числом N.
Если стульев не хватает, то пришедший посетитель уходит.
Создать многопроцессное приложение, моделирующее рабочий день парикмахерской.
Парикмахера и каждого из посетителей моделировать в виде отдельных процессов. Последние могут независимо порождаться в
произвольное время и завершать работу после их обслуживания.
3) SharedData реализует разделяемую память, с которой взаимодействуют процессы, каждый посетитель - customer и парикмахер
- barber представляют отдельный процесс. В main программа получает от пользователя количество мест в салоне и количество
посителей. Затем создается процесс барбера, который работает, пока не обработает всех посетителей. Посетители создаются
в виде процессов и занимают свое место в очереди ожидая( с помощью семафора) барбера, а  барбер обрабатывает
последовательно всех покупателей. В начале метода customera рандомное время он спит, реализуя порождение посетителя в
 рандомное время. А если очередь заполнена, то посетитель уходит, например в тесте 3.
4) Задача решалась используя
Множество процессов взаимодействуют с использованием неиме- нованных POSIX семафоров расположенных в разделяемой па- мяти.
Обмен данными также ведется через разделяемую па- мять в стандарте POSIX.
5) Программа останавливает свою работу при завершении всех процессов, либо при нажатии ctrl+c
6) Тесты приведены в этой же папке 4 - 5
    1) Для 5 человек и 5 мест
    2) остановка ctrl c
    3) Для 5 человек и 2 мест
    4) Для 2 человек и 5 мест

