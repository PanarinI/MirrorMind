##Верхний уровень:
name: Название чата (например, "Группа поддержки сами знаете кого").
type: Тип чата (например, "private_supergroup").
id: Уникальный идентификатор чата.
messages: Список сообщений, где каждое сообщение представлено как объект JSON.

##Элементы каждого сообщения в messages:
1. **Общие поля:**
id: Уникальный идентификатор сообщения.
type: Тип сообщения (message, service и т. д.).
date: Дата отправки сообщения.
date_unixtime: Временная метка в формате Unix.
from: Имя отправителя.
from_id: Уникальный идентификатор отправителя.

2. **Содержимое сообщения:**
text: Текст сообщения (может быть пустым или содержать другие форматы, например ссылки).[sample.json](../../data/sample.json)
text_entities: Список структурированных элементов текста (например, ссылки, эмодзи).

3. **Ответы и реакции:**

reply_to_message_id: Указывает, на какое сообщение идет ответ (если есть).
reactions: Реакции на сообщение, содержащие:
type: Тип реакции (например, "emoji").
count: Количество реакций.
emoji: Конкретное эмодзи.
recent: Подробности о недавних реакциях (кто и когда поставил).

4. **Дополнительно:**
edited и edited_unixtime: Дата и временная метка редактирования сообщения.
photo, file, media_type: Медиа, прикрепленное к сообщению (если есть).
5. **Сервисные сообщения** (type: "service"):

actor: Действующее лицо (кто выполнял действие).
action: Тип действия (например, создание группы, изменение названия).
members: Участники, вовлеченные в действие (например, при создании группы).