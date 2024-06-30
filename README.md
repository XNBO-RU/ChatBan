# ChatBan Plugin

ChatBan - это плагин для Minecraft, который автоматически банит игроков за использование запрещённых слов в чате. Запрещённые слова и команды для бана настраиваются через конфигурационный файл.

## Функциональные возможности

- **Проверка сообщений в чате**:
  - Плагин проверяет все сообщения, отправляемые игроками в чат.
  - Если в сообщении содержится слово из списка запрещённых слов, игрок автоматически банится.

- **Конфигурация**:
  - Плагин имеет конфигурационный файл `config.yml`, в котором указываются запрещённые слова и команды для бана.
  - Возможность включения/выключения выполнения дополнительной команды при бане.

- **Автоматический бан**:
  - При обнаружении запрещённого слова в сообщении игрока, плагин автоматически выполняет команду для бана.
  - Команда для бана задаётся в конфигурационном файле и поддерживает использование плейсхолдеров для вставки ника нарушителя (например, `{player}`).

- **Дополнительная команда**:
  - Плагин поддерживает выполнение дополнительной команды вместе с баном.
  - В конфигурационном файле можно включить или выключить выполнение дополнительной команды.
  - Дополнительная команда также поддерживает использование плейсхолдеров для вставки ника нарушителя (например, `{player}`).

## Пример конфигурационного файла

```yaml
# Список запрещённых слов в чате
banned_words:
- word1
- word2
- word3

# Команда для бана нарушителя
ban_command: "ban {player} Нарушение правил: плохие слова в чате"

# Включение/выключение выполнения дополнительной команды
additional_command_enabled: true

# Дополнительная команда (например, для уведомления администрации)
additional_command: "broadcast Игрок {player} был забанен за использование запрещённых слов в чате"
```
## Установка
- Скачайте последнюю версию плагина из раздела Releases.
- Поместите скачанный JAR файл в папку plugins вашего Minecraft сервера.
- Перезапустите сервер для загрузки плагина.
- Настройте конфигурационный файл config.yml в папке plugins/ChatBan.

## Команды
`/chatban reload` - Перезагрузка конфигурационного файла плагина без перезапуска сервера.

## Сборка проекта
Для сборки проекта используйте Maven.
### Клонируйте репозиторий:
```yaml
git clone https://github.com/XNBO-RU/ChatBan/ChatBan.git
```
### Перейдите в директорию проекта:
```yaml
cd ChatBan
```

### Соберите проект:
```yaml
 mvn clean package
```
