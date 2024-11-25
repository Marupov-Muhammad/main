Барои сохтани як branch (шоха) дар Git, шумо бояд дастурҳои зеринро пайравӣ кунед:

Мо роҳи лозим барои сохтани шоха (branch)-ро мекорем. Барои сохтани як шоха, ки ба нишони гузашта пайваст намешавад (нишонаи шохаи маъмул), команди зеринро истифода мебарем:

php
git branch <branch_name>
Мисол: Агар шумо хоҳед, ки шохаи навро бо номи feature-xyz созед:

git branch feature-xyz
Ба шохаи нав гузаред. Вақте ки шумо шохаеро созед, барои шенасоии шоха, ки мехоҳед дар он кор кунед, ба шохаи нав гузаред. Барои ин, истифода баред:

php
git checkout <branch_name>
Мисол:

git checkout feature-xyz
Аз версияи нави Git (аз версияи 2.23 ва баъд), шумо метавонед ҳамзамон як шохаи нав созед ва ба он гузаред бо истифода аз командаи зерин:

r
git switch -c <branch_name>
Мисол:

r
git switch -c feature-xyz
Ҳолати шохаро санҷидан: Пас аз гузариш, агар шумо мехоҳед, ки тасдиқ кунед, ки дар шохаи дурусте ҳастед, командаи зеринро истифода баред:

git branch
Ҳамин тавр, шохаи ҳозира бо * нишон медиҳад.

Ҳамин тавр, шохаи нав созиш ва дар он кор кардан мумкин аст!



Вы сказали:
чи тавр repository созем
ChatGPT сказал:
ChatGPT
Барои сохтани як Git repository (репозитории Git) нав, шумо метавонед қадамҳои зеринро пайравӣ кунед:

1. Сохтани директорияи нав
Агар шумо хоҳед, ки репозитории Git нав дар як директорияи муайян сохта шавад, аввал як директорияи нав эҷод кунед:

bash
mkdir <name_of_directory>
cd <name_of_directory>
Мисол:

bash
mkdir my-project
cd my-project
2. Инициализатсияи репозитории Git
Пас аз дохил шудан ба директорияи интихобшуда, командаро барои оғоз кардани репозитории Git истифода баред:

bash
git init
Ин команда як репозитории холӣ ва пӯшида дар директорияи шумо эҷод мекунад, ки бо файлҳои .git таъриф мешавад. Аз ин ҷо ба пас, ҳамаи файлҳо ва тағйиротҳо дар ин директория бо истифода аз Git пайгирӣ мешаванд.

3. Қабул кардани файлҳо ба репозитории Git
Шумо бояд файлҳоятонро барои пайгирӣ ба Git илова кунед. Барои илова кардани ҳамаи файлҳои мавҷуд дар директория ба репозитории Git, командаи зеринро истифода баред:

bash
git add .
Эзоҳ: . ба маънои "ҳамаи файлҳо" аст. Агар шумо танҳо як файл ё директорияро мехоҳед илова кунед, номи онҳоро истифода баред.

Мисол:

bash
git add index.html
4. Сохтани аввалин commit
Пас аз илова кардани файлҳо, шумо бояд барои нигоҳ доштан ва сабт кардани тағйиротҳо як commit созед. Комментарии барои commit хеле муҳим аст, ки зоҳир мекунад, ки чӣ гуна тағйиротҳо дода шудаанд.

bash
git commit -m "Initial commit"
5. (Опционалӣ) Пайваст кардани репозитории Git ба сервери дури (remote repository)
Агар шумо мехоҳед репозитории худро ба як хидматдори Git (масалан GitHub, GitLab ё Bitbucket) пайваст кунед, шумо бояд URL-и репозитории дурро истифода баред. Масалан, агар шумо репозитории GitHub эҷод карда бошед, URL-и он метавонад чунин бошад:

bash
git remote add origin https://github.com/username/my-project.git
6. (Опционалӣ) Лағжондан ва пуш кардани тағйирот ба сервер
Барои пуш кардани файлатон ба сервери GitHub ё дигар хидматҳо, шумо метавонед командаи зеринро истифода баред:

bash
git push -u origin master
(Ё агар шумо шохаи асосии худро main номгузорӣ кунед, пас истифода баред:)

bash
git push -u origin main
Натиҷа: Ҳоло шумо як репозитории Git дар локал (дар компютери худ) ё сервери онлайн доред. Аз ин ба баъд, шумо метавонед тағйиротҳоро пайгирӣ кунед, онҳоро ба репозитории локалӣ ва дури пуш кунед.