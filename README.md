# PZ6_Lr3
Выполнил Костомахин Антон Александрович , ББМО-02-23

# C помощью ifconfig узнаем ip-адрес DVL. Cканируем ip-адрес с помощью nmap
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/4446c831-24d4-4705-868d-4e3cc91c8a67)
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/cfcac5a7-0d3c-4b2f-93aa-79bc4043c360)
# Сканируем DVL при помощи Openvas
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/92dbcf6c-09e6-49c8-a122-10a734c4790e)
# XSS
Запускаем burpsuite. Переходим во вкладуку Proxy и включаем перехват.
Переходим на сайт с XSS уязвимостью
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/97cd4073-a70a-4433-9f30-9f5e6b97f5ae)
После ввода данных и нажатия кнопки Add Comment в burpsuite увидим запрос
меняем последнюю строчку на name=Pankov&comment=<script>alert ("Pankov_XSS") </script >
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/3c89ff29-9fdd-4bd7-9078-f73ab4959c0d)
# CSRF
Переходим на сайт с CSRF уязвимостью
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/a8658a36-2517-4841-b4eb-de553723b11d)
После ввода данных и нажатия кнопки Add Comment в burpsuite увидим запрос
Меняем последнюю строчку на item=pen&quantity=1234567890
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/ccbfa53f-3c76-4927-b97c-833d5e2a5cec)
Устанавливаем и запускаем OWASP ZAP. Запускаем автоматическое сканирование и исследуем результат SQL injection
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/a2a66dbb-1bed-4067-852b-1d45fb2e6835)
Запускаем metasploit. Настраиваем RHOST, USERNAME, PASS_FILE, STOP_ON_SUCCESS. Запускаем
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/2e9a933a-457b-4a43-809d-18164377652c)
Подключаемся к SSH. Заходим в mysql. Находим файл с логином и паролем в зашифрованном виде. Создаем txt файл в который вписываем зашифрованный пароль. Запускаем JohnTheRipper и ищем пароль
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/549834ef-ae1d-459d-842f-c045428d4077)
# Анализ трафика с помощью wireshark
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/0efbded6-5e2e-4e85-9485-86bf73aad33b)
# Snort правила
![image](https://github.com/KOSTILET/PZ6_Lr3/assets/64083435/aa6ea7a8-9540-4f23-9bab-884728cf0064)
