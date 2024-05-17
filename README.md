SQL2
-------------------------------------------------------------
Есть бд “школа”
необходимо спроектировать таблицы “Предмет” и “Преподаватели”
-------------------------------------------------------------
CREATE TABLE IF NOT EXISTS предмет (
ID INT NOT NULL PRIMARY KEY AUTOINCREMENT,
название VARCHAR(10) NOT NULL
);
INSERT INTO предмет (ID, название) VALUES
('121', 'Math'),
('231', 'Eng');

CREATE TABLE IF NOT EXISTS преподаватели (
ID INT NOT NULL PRIMARY KEY AUTOINCREMENT,
имя VARCHAR(10) NOT NULL,
FOREIGN KEY (ID_предмет) REFERENCES предмет (ID)
);
INSERT INTO преподаватели (ID, имя) VALUES
('315', 'Eduard'),
('414', 'Roman');

SELECT ID FROM предмет 
SELECT имя FROM преподаватели
SELECT название FROM предмет
![image](https://github.com/Dmitry11ww33/HW_SQL2/assets/136243924/b6eb1806-1b11-4398-b718-192f512eff32)

