## задание 1
первоначально я создала новый репозиторий git-practice2 и клонировала его
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05%201.jpg)
далее я создала файл, где прописала следующий скрипт 
   ```
    #!/bin/bash

chmod +x "$0"

for file in $(git diff --cached --name-only); do
  echo "Проверка файла: $file"
  
  if [[ "$file" == *.txt ]]; then
    echo "Файл $file - текстовый"
    
    if [[ ! -s "$file" ]]; then
      echo "Ошибка: Файл '$file' пустой." >&2
      exit 1
    fi
    
    if ! grep -q '[^[:space:]]' "$file"; then
      echo "Ошибка: Файл '$file' не содержит текста." >&2
      exit 1
    fi
  fi
done

exit 0
   ```
потом я создала файл и начала пытаться его закомитить
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB.JPG)

теперь редактируем файл и добавляем в него текст

![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%B6.JPG)

## задание 2
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05.2%201.JPG)
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05.2%202.JPG)
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05.2%203.JPG)
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05.2%204.JPG)
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05.2%205.JPG)
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05.2%206.JPG)
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05.2%207.JPG)
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05.2%208.JPG)
![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05.2%209.JPG)

после gedit file_witch_errer.py я прописала error=0

![Screenshot from 2024-12-23 13-24-53](https://github.com/patimakerr/patimakerr-in-ITMO/blob/main/%D0%BB%D0%B0%D0%B1%D0%B05.2%2010.JPG)

в конце выполнения лабораторной работы нам необходимо прописать еще 2 комманды

   ```
git push origin develop
git push origin main
   ```
где git push origin develop отправляет наши локальные изменения из ветки develop в удалённый репозиторий (ветку develop), а git push origin main отправляет (загружает) все коммиты, которые мы сделали в нашей локальной ветке develop, в удалённую ветку develop в репозитории, который называется origin.
