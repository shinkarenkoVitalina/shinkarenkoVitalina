
# Лабораторная работа №6

Первым шагом мы форкаем (создаем копию репозитория в личное хранилище) репозиторий: https://github.com/Kurtyanik/LR6/

![1](https://user-images.githubusercontent.com/87824002/195204153-b70fcd8d-687a-4d63-995c-764fcb8390de.jpg)

Далее используем команды git config --global user.name и git config --global user.email для настройки клиента Git и вводим свои данные от GitHub.

![2](https://user-images.githubusercontent.com/87824002/195204811-c8007ac6-4882-44b0-8c96-4aa6e3e092a5.jpg)

Клонируем удаленный репозиторий, используя команду git clone.

![3](https://user-images.githubusercontent.com/87824002/195204877-7d6b59dc-8137-4c44-800e-5b88b3265d2e.jpg)

Добавим файл через интерфейс GitHub. Далее переходим в директорию LR6 командой cd LR6 для дальнейшей работы с файлами.

![4](https://user-images.githubusercontent.com/87824002/195205068-74dbbbb5-c3e9-4ae5-a51e-b1eca3231546.jpg)

Подтянем изменения из веб-интерфейса GitHub для клиента Git. Для этого используем команду git pull.

![5](https://user-images.githubusercontent.com/87824002/195205126-70ca1c95-9e7f-4910-99d1-5bea3316c515.jpg)

Посмотрим коммиты ветки master, используя команду git log.

![6](https://user-images.githubusercontent.com/87824002/195205182-331f7d30-23f3-4a44-b94e-6d5035f2c758.jpg)

Просмотрим существующие ветки в текщем репозитории командой git branch.

![7](https://user-images.githubusercontent.com/87824002/195207238-59d4ec99-d002-4cc5-b82d-00fcabc37f5d.jpg)

Перейдем в ветку branch1 командой git checkout branch1.

![8](https://user-images.githubusercontent.com/87824002/195207268-04448007-a6c5-4ea1-a27a-4188c0b442fd.jpg)

Посмотрим коммиты ветки branch1 с помощью команды git log.

![9](https://user-images.githubusercontent.com/87824002/195209981-95a80a39-7931-43c1-a9ee-82e1f8ffc66d.jpg)

Подробно рассмотрим коммиты с помощью команды git log -p.

![10_1](https://user-images.githubusercontent.com/87824002/195210088-cb5a1ca9-e916-4525-be43-abf9b1ba2e7c.jpg)
![10_2](https://user-images.githubusercontent.com/87824002/195212505-e45d920e-23bf-438a-9bdd-79b7c15ea551.jpg)

Вернемся в ветку master.

![11](https://user-images.githubusercontent.com/87824002/195210798-020e0594-be55-4e46-aec4-86a978bf965d.jpg)

Выполним слияние в ветку master. Слияние производится при помощи команды git merge branch1.

![12](https://user-images.githubusercontent.com/87824002/195210885-62897d21-d065-498d-b512-d1bd3497ec19.jpg)

Произошел конфликт. Скорее всего из-за того, что файл mergefile.txt не отслеживается. Используем команду git status.

![13](https://user-images.githubusercontent.com/87824002/195210994-44bece31-da50-44b1-b604-703d1999afec.png)

Теория оказалась верна. Добавим файл для отслеживания командой git add mergefile.txt.

![14](https://user-images.githubusercontent.com/87824002/195211061-fe7587bf-f76c-4fb1-8216-55e47ac35b8f.png)

Проверим еще раз, отслеживается ли файл.

![15](https://user-images.githubusercontent.com/87824002/195211242-d8f911f9-6829-4358-9c00-cfd22689f680.png)

Конфликт разрешен, оставляем коммит при помощи команды git commit -m "Branches".

![16](https://user-images.githubusercontent.com/87824002/195211442-ce500c0a-136c-473a-859c-1cdc4896442f.jpg)

Удаляем побочную ветку после успешного слияния при помощи команды git branch -d branch1 

![17](https://user-images.githubusercontent.com/87824002/195211844-5a9935ba-195b-418c-a149-c8cd670a96bc.jpg)

Создадим изменения и комментарии для них. Создавать будем текстовые файлы прямо в терминале. Для создания текстовика используем команду echo hello > change1.txt, зафиксируем его git add change1.txt. Оставим комментарий git commit -m "Change1.txt". Повторем все то же самое еще раз, только название указываем другое - change2.txt.

![18](https://user-images.githubusercontent.com/87824002/195217021-fc375a8e-5ed7-47d1-92ee-53b2ab1b8299.jpg)

Посмотрим комментарии.

![19_1](https://user-images.githubusercontent.com/87824002/195217061-b65f3110-6efd-4740-8378-79b6d8a46110.jpg)
![19_2](https://user-images.githubusercontent.com/87824002/195217073-094bf4b0-8915-4996-b6e7-e8d36232e3a6.jpg)

Теперь сделаем "хард" откат коммита. Вводим git reset --hard HEAD~1

![20](https://user-images.githubusercontent.com/87824002/195217114-a54e7c1a-a90a-4f92-af5e-83cc53d05c79.jpg)

Создадим ветку для отчета и перейдем в нее git branch report.

![21](https://user-images.githubusercontent.com/87824002/195217142-f32f6402-2817-48c7-a2c9-66d5d9d657c9.jpg)

Получим итоговую историю операций

![22_1](https://user-images.githubusercontent.com/87824002/195217206-b9985717-101c-4669-956c-dc41cbc2d62d.jpg)
![22_2](https://user-images.githubusercontent.com/87824002/195217218-34d74708-35b9-490b-b46a-48d268f1ccda.jpg)

После редактирования отчета, его нужно будет сохранить и произвести команды git add и git commit.
В конце работы необходимо будет отправить все локальные изменения в сетевое хранилище GitHub командой git push.
