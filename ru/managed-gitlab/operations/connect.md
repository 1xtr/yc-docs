# Подключение к инстансу {{ mgl-name }}

## Настройка групп безопасности {#configuring-security-groups}

{% include [security-groups-note-services](../../_includes/vpc/security-groups-note-services.md) %}

В {{ mgl-name }} используется [группа безопасности по умолчанию](../../vpc/concepts/security-groups.md#default-security-group) для выбранной [сети](../../vpc/concepts/network.md#network). Выбрать другую при создании инстанса нельзя.

Настройте группу безопасности по умолчанию для выбранной сети так, чтобы она разрешала входящий трафик с любых IP-адресов на порты 22, 2222, 80, 443, 5050. Для этого [создайте правила](../../vpc/operations/security-group-add-rule.md) для входящего трафика.

Для работы с Git-репозиторием по протоколу [SSH](../../glossary/ssh-keygen.md):
* Протокол — `TCP`.
* Диапазон портов — `22`.
* Тип источника — `CIDR`.
* Источник — `0.0.0.0/0`.

Для работы с Git-репозиторием по протоколу SSH:
* Протокол — `TCP`.
* Диапазон портов — `2222`.
* Тип источника — `CIDR`.
* Источник — `0.0.0.0/0`.

Для получения HTTP-трафика:
* Протокол — `TCP`.
* Диапазон портов — `80`.
* Тип источника — `CIDR`.
* Источник — `0.0.0.0/0`.

Для получения HTTPS-трафика:
* Протокол — `TCP`.
* Диапазон портов — `443`.
* Тип источника — `CIDR`.
* Источник — `0.0.0.0/0`.

Для подключения к [{{ container-registry-full-name }}](../../container-registry/):
* Протокол — `TCP`.
* Диапазон портов — `5050`.
* Тип источника — `CIDR`.
* Источник — `0.0.0.0/0`.

## Подключение к инстансу {#connect}

1. Задайте пароль администратора. Для этого перейдите по ссылке из письма, присланного на электронную почту администратора, указанную при регистрации инстанса.
1. Откройте в браузере ссылку на веб-интерфейс инстанса. Она указана в письме, отправленном на электронную почту администратора, и в [детальной информации об инстансе](instance/instance-list.md#get).
1. Авторизуйтесь с помощью логина и пароля администратора.