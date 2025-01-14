---
description: Что такое SWAP, и зачем мы его используем
---

# 🤔 Почему хостинг использует SWAP?

### 🤔 Что такое SWAP?

SWAP - это раздел на физической памяти диска для временного хранения неактивных элементов ОЗУ.

### 👨‍🔬 Как работает SWAP?

<table data-header-hidden><thead><tr><th width="227"></th><th></th></tr></thead><tbody><tr><td>Запуск сервера</td><td>ОЗУ начинает заполняться</td></tr><tr><td>Активная игра</td><td>ОЗУ активно записывает данные чанков, игроков, и т.д. </td></tr><tr><td>Игрок вышел или GC отработал</td><td>Неактивные элементы переносятся в SWAP, освобождая ОЗУ</td></tr></tbody></table>

{% hint style="warning" %}
💡 Важно:

SWAP никогда не используется в качестве основной ОЗУ на наших нодах. Его смысл прост - освобождать драгоценную ОЗУ, перенося в него неактивные элементы.
{% endhint %}



### ❓ Почему другие хостинги не используют SWAP, если он так идеален?

1. Почти 100% хостингов используют дешевые серверы с I9 9900K, который подходит под 128 ГБ ОЗУ. Он быстро нагружается, и 128 ГБ ОЗУ - его предел.
2. Использование SWAP на этом процессоре не имеет смысла из-за ограничений ядер/потоков. Это позволяет создать идеальное соотношение цены и использования ресурсов.
3. Некоторые хостинги, использующие эти серверы, выставляют цены даже выше наших, до 140% разницы.
4. **Утверждения о 5 GHz в I9 9900K вводят в заблуждение. В этом процессоре чаще всего только одно-два ядра на короткий срок могут разогнаться до 5ГГц.**

{% hint style="success" %}
💡 Неиспользование SWAP на чудо-хостингах объясняется их стратегией и техническими характеристиками. Наши же решения обеспечивают лучшее соотношение цены и качества, используя SWAP оптимальным образом.
{% endhint %}

### 😕 Почему мой сервер может лагать?

#### Не связанные с хостингом причины

* В скачанной сборке могут содержаться вирусы, майнеры, и другие вредоносные программы.
* Нехватка ресурсов в тарифе: Иногда пользователи не понимают, что выбранный тариф не соответствует их потребностям. Поэтому мы советуем проконсультироваться с поддержкой Discord перед покупкой тарифа.

#### ❗ Связанные с хостингом причины:

Иногда человек может не заметить, и вовремя не закрыть ноду, из-за чего на ней станет больше потребителей чем ресурсов, и у всех будет лагать.

#### 🔧 Как мы решаем проблемы:

* Если нода перегружена, мы информируем об этом и переносим пострадавшие серверы на другой узел.
* Мы предоставляем компенсацию, в размере оплаченного сервера на определенный период или рубли на счет хостинга.
