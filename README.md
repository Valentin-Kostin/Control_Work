# Итоговая контрольная работа по блоку специализация


## Урок 2. Итоговая контрольная работа



**Информация о проекте**

* Необходимо организовать систему учета для питомника в котором живут домашние и вьючные животные.

**Как сдавать проект**

Для сдачи проекта необходимо создать отдельный общедоступный репозиторий (Github, Gitlub или Bitbucket).
Разработку вести в этом репозитории, использовать пул реквесты на изменения. Программа должна запускаться и работать,
ошибок при выполнении программы быть не должно. Программа может использоваться в различных системах, поэтому необходимо
разработать класс в виде конструктора.

### Задание

1. Используя команду cat в терминале операционной системы Linux, создать два файла "Домашние животные"
   (заполнив файл "собаками", "кошками", "хомяками") и "Вьючные животные" (заполнив файл "лошадьми", "верблюдами" и "
   ослами"),
   а затем объединить их. Просмотреть содержимое созданного файла. Переименовать файл, дав ему новое имя "Друзья
   человека".
2. Создать директорию, переместить файл туда.
3. Подключить дополнительный репозиторий MySQL. Установить любой пакет из этого репозитория.
4. Установить и удалить deb-пакет с помощью dpkg.
5. Выложить историю команд в терминале Ubuntu.
6. Нарисовать диаграмму, в которой есть классы - родительский, домашние животные и вьючные животные,
   в составы которых в случае домашних животных войдут классы: собаки, кошки, хомяки, а в класс вьючные животные войдут:
   лошади, верблюды и ослы.
7. В подключенном MySQL репозитории создать базу данных “Друзья человека”.
8. Создать таблицы с иерархией из диаграммы в БД.
9. Заполнить низкоуровневые таблицы именами (животных), командами которые они выполняют и датами рождения.
10. Удалить из таблицы верблюдов, т.к. верблюдов решили перевезти в другой питомник на зимовку.
    Объединить таблицы "лошади", и "ослы" в одну таблицу.
11. Создать новую таблицу "молодые животные" в которую попадут все животные старше 1 года, но младше 3 лет
    и в отдельном столбце, с точностью до месяца, подсчитать возраст животных в новой таблице.
12. Объединить все таблицы в одну, при этом сохраняя поля, указывающие на прошлую принадлежность к старым таблицам.
13. Создать класс с Инкапсуляцией методов и наследованием по диаграмме.
14. Написать программу, имитирующую работу реестра домашних животных.
    В программе должен быть реализован следующий функционал:

    14.1. Завести новое животное;

    14.2. Определять животное в правильный класс;

    14.3. Увидеть список команд, которое выполняет животное;

    14.4. Обучить животное новым командам;

    14.5. Реализовать навигацию по меню.

15. Создайте класс Счетчик, у которого есть метод add(), увеличивающий̆ значение внутренней̆ int переменной̆ на 1
    при нажатии “Завести новое животное”. Сделайте так, чтобы с объектом такого типа можно было работать в блоке
    try-with-resources.
    Нужно бросить исключение, если работа с объектом типа счетчик была не в ресурсном try и/или ресурс остался открыт.
    Значение считать в ресурсе try, если при заведения животного заполнены все поля.

### Решение

1.
<details>
    <summary>Команды Bash (развернуть)</summary>

```bash
cat > "Домашние животные"
Собаки
Кошки
Хомяки

'Ctrl+d'
```

```bash
cat > "Вьючные животные"
Лошади
Верблюды
Ослы

'Ctrl+d'
```

```bash
cat "Домашние животные" "Вьючные животные" > "Животные"
cat "Животные"
mv "Животные" "Друзья человека"
```

</details>

![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/01.jpg)

2.

<details>
    <summary>Команды Bash (развернуть)</summary>

```bash
mkdir for_control
mv 'Друзья человека' for_control/
ls
cd for_control/
ls
ls -l
```

</details>

![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/02.jpg)

3.

<details>
    <summary>Команды Bash (развернуть)</summary>

```bash
sudo apt-get update
sudo apt update
sudo apt install mysql-server
sudo service mysql status
```

</details>

![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/03_01.jpg)
![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/03_02.jpg)
![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/03_03.jpg)

4.

<details>
    <summary>Команды Bash (развернуть)</summary>

```bash
wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-j_8.0.32-1ubuntu22.04_all.deb
sudo dpkg -i mysql-connector-j_8.0.32-1ubuntu22.04_all.deb
sudo dpkg -r mysql-connector-j
sudo apt-get autoremove
```

</details>

![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/04_01.jpg)
![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/04_02.jpg)

5.

<details>
    <summary>Команды Bash (развернуть)</summary>

```bash
  465  ls -l

  466  mkdir attestation

  467  ls -l

  468  cd attestation/

  469  cat > "Домашние животные"

  470  ls -l

  471  cd /

  472  ls -l

  473  mkdir attestation

  474  cd attestation/

  475  cat > "Домашние животные"

  476  cat > "Вьючные животные"

  477  cat "Домашние животные" "Вьючные животные" > "Животные"

  478  cat "Животные"

  479  mv "Животные" "Друзья человека"

  480  mkdir for_control

  481  mv "Друзья человека" for_control/

  482  ls

  483  cd for_control/

  484  ls

  485  ls -l

  486  cd ..

  487  sudo apt-get update

  488  sudo apt update

  489  sudo apt install mysql-server

  490  sudo sevice mysql status

  491  sudo service mysql status

  492  clear

  493  https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-j_8.0.32-1ubuntu22.04_all.deb

  494  wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-j_8.0.32-1ubuntu22.04_all.deb

  495  sudo dpkg - i mysql-connector-j_8.0.32-1ubuntu22.04_all.deb

  496  sudo dpg -i Downloads/appgrid_0.298_all.deb

  497  sudo dpkg -i Downloads/appgrid_0.298_all.deb

  498  sudo dpkg - i mysql-connector-j_8.0.32-1ubuntu22.04_all.deb

  499  sudo dpkg -i mysql-connector-j_8.0.32-1ubuntu22.04_all.deb

  500  sudo dpkg -r mysql-connector-j

  501  sudo apt-get autoremove

  502  History

  503  history


```

</details>

![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/05.jpg)

6.

![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/06.png)

7.

```sql
CREATE DATABASE Друзья_человека;
```

![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/07.jpg)

8.

<details>
    <summary>SQL запросы (развернуть)</summary>

```sql
 USE Друзья_человека

CREATE TABLE Родительский_класс (
  id INT PRIMARY KEY AUTO_INCREMENT,
  тип VARCHAR(50)
);


CREATE TABLE Домашние_животные (
  id INT PRIMARY KEY,
  вид VARCHAR(50),
  FOREIGN KEY (id) REFERENCES Родительский_класс(id)
);


CREATE TABLE Собаки (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Домашние_животные(id)
);


CREATE TABLE Кошки (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Домашние_животные(id)
);


CREATE TABLE Хомяки (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Домашние_животные(id)
);


CREATE TABLE Вьючные_животные (
  id INT PRIMARY KEY,
  вид VARCHAR(50),
  FOREIGN KEY (id) REFERENCES Родительский_класс(id)
);


CREATE TABLE Лошади (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
);


CREATE TABLE Верблюды (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
);


CREATE TABLE Ослы (
  id INT PRIMARY KEY,
  имя VARCHAR(50),
  команда VARCHAR(50),
  дата_рождения DATE,
  FOREIGN KEY (id) REFERENCES Вьючные_животные(id)
);

show databases;
show tables;
```

</details>

![pictures for project](https://github.com/Valentin-Kostin/Control_Work/blob/main/pictures/08.jpg)

9.

<details>
    <summary>SQL запросы (развернуть)</summary>

```sql
INSERT INTO Верблюды ( имя, команда, дата_рождения)
VALUES ('Зефир', 'Но, пошел', '2019-09-01'),
       ('Багдад', 'На месте' '2020-11-12'),
       ('Скорость', 'Ждать' '2021-04-05');

INSERT INTO Кошки ( имя, команда, дата_рождения)
VALUES ('Маркиз', 'Кис-кис', '2021-01-20'),
       ('Снежка', 'Давай играть', '2022-03-08');

INSERT INTO Лошади ( имя, команда, дата_рождения)
VALUES ('Спирит', 'Но', '2020-01-21'),
       ('Воронок', 'Бррррр', '2022-03-08');

INSERT INTO Ослы ( имя, команда, дата_рождения)
VALUES ('Нарик', 'Пошёл', '2019-01-21'),
       ('Степан', 'Стой', '2021-03-08');

INSERT INTO Собаки ( имя, команда, дата_рождения)
VALUES ('Шарик', 'Дай лапу', '2019-01-21'),
       ('Бим', 'Лежать', '2020-03-08');

INSERT INTO Хомяки ( имя, команда, дата_рождения)
VALUES ('Долгожитель', 'Кушать', '2022-01-21'),
       ('Хома', 'Отойди', '2023-03-08');
```

</details>

10.

<details>
    <summary>SQL запросы (развернуть)</summary>

```sql
TRUNCATE TABLE Верблюды;
```

```sql
CREATE TABLE Парнокопытные AS
SELECT * FROM Лошади
UNION
SELECT * FROM Ослы;
```

</details>

11.

<details>
    <summary>SQL запросы (развернуть)</summary>

```sql
CREATE TABLE Парнокопытные AS
SELECT *, TIMESTAMPDIFF(MONTH, дата_рождения, CURDATE()) AS возраст_в_месяцах
FROM (
    SELECT 'Собаки' AS тип_животного, имя, команда, дата_рождения FROM Собаки
    UNION ALL
    SELECT 'Кошки' AS тип_животного, имя, команда, дата_рождения FROM Кошки
    UNION ALL
    SELECT 'Хомяки' AS тип_животного, имя, команда, дата_рождения FROM Хомяки
    UNION ALL
    SELECT 'Лошади' AS тип_животного, имя, команда, дата_рождения FROM Лошади
    UNION ALL
    SELECT 'Ослы' AS тип_животного, имя, команда, дата_рождения FROM Ослы
) AS животные
WHERE дата_рождения >= DATE_SUB(CURDATE(), INTERVAL 3 YEAR)
AND дата_рождения <= DATE_SUB(CURDATE(), INTERVAL 1 YEAR);

```

</details>

12.

<details>
    <summary>SQL запросы (развернуть)</summary>

```sql
CREATE TABLE Полный_состав AS
SELECT 'Собаки' AS тип_животного, имя, команда, дата_рождения FROM Собаки
UNION ALL
SELECT 'Кошки' AS тип_животного, имя, команда, дата_рождения FROM Кошки
UNION ALL
SELECT 'Хомяки' AS тип_животного, имя, команда, дата_рождения FROM Хомяки
UNION ALL
SELECT 'Лошади' AS тип_животного, имя, команда, дата_рождения FROM Лошади
UNION ALL
SELECT 'Ослы' AS тип_животного, имя, команда, дата_рождения FROM Ослы;

```

</details>

13. , 14. , 15. - [-= Перейти к коду Java =-](https://github.com/Valentin-Kostin/Control_Work/tree/main/Java)