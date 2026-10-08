# Это курс по компьютерным сетям, где сеть не рисуют на доске — её запускают, ломают и чинят руками.

Ты будешь работать с настоящими Linux-хостами, маршрутизаторами, коммутаторами, DNS и HTTP-серверами. Посмотришь
реальные пакеты, разберёшь Ethernet и IP по байтам, увидишь ARP, ICMP, TCP handshake, DNS-запросы и HTTP прямо в
трафике.

Каждая лабораторная — это небольшая живая сеть внутри notebook: сначала разбираемся, как что работает, потом проверяем
гипотезу на стенде, специально что-нибудь ломаем, диагностируем и восстанавливаем.

К концу курса ты сможешь не просто написать `ping`, а понять, **почему пакет пошёл именно туда, где он потерялся и что
нужно проверить следующим**.

Попробовать среду можно прямо в браузере — начни с Lab 0 в GitHub Codespaces

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/cms-lab-core/lab-computer-network?quickstart=1)

## Запуск среды

Codespaces и локальный Dev Container запускают полный CMS Labs контур через kind и опубликованные OCI charts: API `^1.0.0`, terminal `^2.0.0` и capture `^0.1.0`. Соседние репозитории и локальные копии charts не нужны. Values находятся в `.cms-labs/cms-labs-values.yaml`, каталог курса — в `demo-labs.json`.

Дождись сообщения `CMS Labs environment is ready`, открой порт `18080` и войди как `admin@admin.com` / `admin`. Лабораторную выбирай в каталоге CMS.

Для ручного запуска: `./scripts/demo up`. Проверка конфигурации: `./scripts/validate.sh`.

Если Codespace открылся в recovery mode, обнови файлы из `main` и выполни `Codespaces: Rebuild Container`. Если ошибка повторится, открой `Codespaces: View Creation Log`: там будет причина остановки.
