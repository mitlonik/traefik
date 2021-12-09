Intro to Traefik: https://habr.com/ru/post/508636/ . Has been used this manual.

---
Traefik. Оно идеально подходит для проксирования запросов в различные docker контейнеры на одном хосте.

Принцип работы там следующий. Запускаете на хосте контейнер с traefik и подключаете ему хостовый сокет докера, чтобы он мог следить за запущенными контейнерами. Traefik из коробки имеет web интерфейс, через который можно всем управлять. Далее вы запускаете новые контейнеры с веб сайтами, передавая им некоторые метки через конфиг docker-compose. Сайты автоматически регистрируются в панели traefik, вы ими управляете. Ничего со стороны брать не надо, traefik все умеет сам.

Чтобы быстро запустить и понять, как traefik работает, подойдет Quick Start из его руководства - https://doc.traefik.io/traefik/getting-started/quick-start/ У него в целом хорошая инструкция с крутыми картинками.

Для более приближенной к реальной эксплуатации схеме можно воспользоваться инструкцией с DO, где показано, как проксировать запросы на несколько разных сайтов - https://www.digitalocean.com/community/tutorials/how-to-use-traefik-as-a-reverse-proxy-for-docker-containers-on-ubuntu-18-04-ru



Ссылки на источники:
1. https://habr.com/ru/post/508636/
2. https://habr.com/ru/post/551792/
3. https://gist.github.com/designervoid/424f6e1c14a982d210d39422e966f23c
4. https://doc.traefik.io/traefik/getting-started/quick-start/
5. https://www.digitalocean.com/community/tutorials/how-to-use-traefik-as-a-reverse-proxy-for-docker-containers-on-ubuntu-18-04-ru
6. https://techsch.com/tutorials/multiple-websites-jwilder-nginx-proxy-letsencrypt + traefik
7. полезное чтиво https://habr.com/ru/post/526440/