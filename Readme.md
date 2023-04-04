# Лабораторна робота №2
## з дисципліни "Автоматизація тестування програмного забезпечення"

**Виконав:** студент групи ІН.м-25 Пономаренко Олександр Володимирович

**Мета роботи:** Використання систем управління версіями є обов'язковим елементом сучасної розробки. Так само, як і навички володіння ними. Принаймні найбільш розповсюдженою - GIT.

**Хід роботи:**
1. Створіть публічний репозіторій та додайте кілька файлів у нього із довільним вмістом. Обов'язково - файл Readme.md із Вашим прізвищем.
2. Створіть всі необхідні згідно до обраної Long-living branches (Git-flow), гілки.

     `master` - це головна гілка, яка містить стабільний, випробуваний і затверджений код вашого проекту.
        
     `develop` - це гілка, на якій ви розробляєте ваш проект. Вона містить останні зміни, які ще не готові для продакшну.
        
     `feature/<feature-name>` - ці гілки використовуються для розробки нових функцій у вашому проекті. Вони виходять від гілки develop і зливаються назад до неї, коли функція готова.
        
     `release/<release-version>` - ця гілка використовується для підготовки нового релізу вашого проекту. Вона виходить від гілки develop, і коли вона готова до релізу, вона зливається як в master, так і в develop.
        
     `hotfix/<hotfix-description>` - ця гілка використовується, коли виникає критична помилка на вашому продакшні. Вона виходить від гілки master, щоб виправити помилку, а потім зливається як в master, так і в develop.

3. Уявимо, що Вам додати нову фічу у Ваш проект. Зміст змін полягає у додаванні довільного файлу та оновленні файлу Readme.md. Які коміти та злиття вам треба виконати, щоб оновлення зя'вились у гілці що відповідає стану проекту готовому для передачі у production?
    
    Щоб оновлення з'явились у гілці, що відповідає стану готовому для передачі у production (тобто в гілці master), потрібно виконати наступні коміти та злиття:

    Запустити команду `git checkout develop`, щоб перейти на гілку develop.
    
    Запустити команду `git pull origin develop`, щоб отримати останні зміни з гілки develop.
    
    Запустити команду `git checkout -b feature/my-new-feature`, щоб створити нову гілку для додавання нової функції.
    
    Внести зміни у проект, додавши новий файл та оновивши файл README.md.
    
    Запустити команду `git add .`, щоб додати зміни до індексу.
    
    Запустити команду `git commit -m "Add new file and update README.md"` для збереження змін.
    
    Запустити команду `git checkout develop`, щоб перейти на гілку develop.
    
    Запустити команду `git pull origin develop`, щоб отримати останні зміни з гілки develop.
    
    Запустити команду `git merge --no-ff feature/my-new-feature`, щоб злити гілку feature/my-new-feature з гілкою develop.
    
    Запустити команду `git checkout master`, щоб перейти на гілку master.
    
    Запустити команду `git pull origin master`, щоб отримати останні зміни з гілки master.
    
    Запустити команду `git merge --no-ff develop`, щоб злити гілку develop з гілкою master.
    
    Запустити команду `git tag -a v1.0.0 -m "Version 1.0.0"`, щоб позначити реліз.
    
    Запустити команду `git push origin master --tags`, щоб відправити зміни на віддалений репозиторій.



4. Додайте у звіт адресу репозиторію та кроки, які ви зробити для виконання пункту "3".
  
     Адреса репозиторію: https://github.com/webturist/Block2.git    
     Кроки вище  👆👆👆

**Висновки:** Git-flow - це методологія розробки програмного забезпечення, яка заснована на використанні Git для керування гілками. Вона дозволяє розробникам ефективно співпрацювати в команді та забезпечує стабільність коду під час розробки.

Git-flow включає в себе ряд основних гілок, таких як master, develop, feature, release та hotfix. Кожна з цих гілок має свою роль у процесі розробки та дозволяє здійснювати різні типи змін.

Під час додавання нової функції до проекту в рамках Git-flow необхідно створити гілку feature, внести зміни у проект та злити їх з гілкою develop. Після цього необхідно злити гілку develop з гілкою master, щоб оновлення з'явилися у готовому для передачі у production стані проекту.

Git-flow дозволяє структурувати розробку проектів та забезпечує стабільність коду під час розробки. Використання Git-flow може покращити ефективність розробки та зменшити кількість конфліктів під час роботи над проектом в команді.