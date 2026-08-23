# Источники
- [Whitelist-JetonTech](https://github.com/xwillam437-cloud/Domain-IP-Whitelist-Address-JetonTech/tree/main)
- [GIST-iamwildtuna](https://gist.github.com/iamwildtuna/7772b7c84a11bf6e1385f23096a73a15)

# Сканирование сети
> Для подключения через SSH нужно разрешить это в настройках роутера. Для JetonTech настройка находится по пути **HomeGurd -> ACL**.<br>
После настройки рекомендуется отключить доступ по SSH, постоянно держать его включенным не безопасно.

### Авторизация в роутере
```cmd
ssh admin@192.168.131.1
```
### Отображение трафика вне белого списка
```cmd
tcpdump -i br-lan -n dst port 443 or dst port 80
```
### Отображение трафика вне белого списка с фильтрацией по конкретному устройству
```cmd
tcpdump -i br-lan -n host {IP устройства} and dst port 443 or dst port 80
```
