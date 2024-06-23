# Домашнее задание к занятию "Базы данных и их типы" - Протасов Владислав


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1. СУБД

Кейс

Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для каждой предметной области. Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему?

1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.

*Для этой задачи лучше всего подходят реляционные СУБД, так как они имеют высокую степень надежности и безопасности.*

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.

*Для этой задачи лучше всего подходят NoSQL СУБД, так как они наиболее гибки и быстры.*

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

*Для этой задачи лучше всего подходят документо-ориентированные СУБД, имеют простую и понятную структуру.*

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.

*Для данной задачи лучше всего подходят графовые СУБД, которые быстро работают со связями.*

Приведите ответ в свободной форме.

---

### Задание 2. Транзакции
2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. Ориентируйтесь на шесть действий.

*Для успешного завершения транзакции пополнения баланса счета телефона необходимо:*

*1. Начало транзакции: пользователь инициирует операцию пополнения баланса счета телефона, что запускает начало транзакции в СУБД.*

*2. Проверка баланса счета: СУБД проверяет текущий баланс счета пользователя, чтобы убедиться, что он может совершить пополнение.*

*3. Списание средств со счета пользователя: СУБД списывает необходимую сумму с баланса счета пользователя.*

*4. Обновление баланса счета телефона: СУБД обновляет баланс счета телефона пользователя, добавляя пополненную сумму.*

*5. Фиксация транзакции: если все предыдущие шаги выполнены успешно, СУБД фиксирует транзакцию, делая изменения постоянными и необратимыми.*

*6. Завершение транзакции: транзакция успешно завершается, и пользователь получает подтверждение о пополнении баланса счета телефона.*

Приведите ответ в свободной форме.

---

### Задание 3. SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL.

*1. Структурированность и целостность данных 2. Большее соответствие принципам ACID 3. Универсальность и масштабируемость 4. Более простой язык запросов 5. Большее количество дополнений.*

3.1.* Какие, на ваш взгляд, преимущества у NewSQL систем перед SQL и NoSQL.

*1. Масштабируемость: NewSQL обеспечивает масштабируемость на уровне NoSQL-систем, но при этом обеспечивает гарантии качества выполнения транзакций, свойственные SQL-системам.*

*2. Устойчивость к разделению: NewSQL системы могут эффективно работать на кластерах, что является одним из основных отличий от реляционных баз данных.*

*3. Сокращение ресурсоемкости: NewSQL не использует ресурсоемкий буферный пул, поскольку база данных целиком находится в основной памяти, что улучшает производительность.*

*4. Упрощение кодирования: NewSQL обеспечивает стандартизацию интерфейсов приложений, что упрощает написание кода и уменьшает сложности, связанные с использованием различных языков запросов у NoSQL-систем.* 

*5. Универсальность: NewSQL системы могут комбинировать лучшие стороны SQL и NoSQL, обеспечивая гибкость и масштабируемость, а также надежность и функциональность, свойственные SQL-системам.*

Приведите ответ в свободной форме.

---

### Задание 4. Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин. На основе какого критерия будете выбирать тип СУБД и какая модель распределённых вычислений здесь справится лучше всего и почему?

Приведите ответ в свободной форме.

*При выборе типа СУБД необходимо учитывать следующие критерии: масштабируемость, производительность, надежность, стабильность, безопасность, устойчивость к разделению, доступность. Для данной задачи можно рассмотреть различные комбинации СУБД и моделей распределенных вычислений, такие как Apache Hadoop с HDFS и MapReduce, Apache Spark, Cassandra, MongoDB, или реляционные базы данных с горизонтальным масштабированием.*

---
