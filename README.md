# Практическая работа 1 (выполнила Огольцова Н.Д. ББМО-01-22)

## Ход работы
1. Установим две ВМ Debian12 и проверим, что между ними есть сетевой обмен

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20113642.png)

2. Установим rsyslog на обе ВМ
   2.1. Установка на первую ВМ

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20114416.png)

   2.2. Установка на вторую ВМ
   
![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20114352.png)

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20114400.png)

3. Проверим, что утилита работает командой systemctl status rsyslog

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20114611.png)

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20114618.png)

4. Изменим кофигурационный файл на первой ВМ, чтобы получать логи со второй

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20115806.png)

5. Проверяем, что логи отправляются, и смотрим какие именно

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20121225.png)

6. Скачиваем Loki на первую ВМ

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20122849.png)

7. Скачиваем конфигурационный файл и запускаем с ним Loki

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20123314.png)

8. Проверяем, что Loki работает корректно, открыв адрес: localhost:3100/metrics

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20123350.png)

9. Скачиваем Promtail на второй ВМ

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20124336.png)

10. Скачиваем кофигурационный файл и вносим в него изменения, изменив адрес на первую ВМ

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20124544.png)

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20124726.png)

11. Проверяем работу Promtail, перейдя по адресу localhost:9080/targets

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20124952.png)

12. Скачиваем SigNoz

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20125447.png)

13. Вводим свою почту и, перейдя по адресу localhost:3301/signup, по ней же регистрируемся

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20125732.png)

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20125852.png)

14. Проверяем, что сбор логов активен

![Изображение](https://github.com/NataliaOgoltsova/System-syslog_2023/blob/main/Снимок%20экрана%202023-09-25%20130103.png)
