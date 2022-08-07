# Documentação da modelagem de classes do banco de dados

### Users collection
| FIELD          | TYPE      | MODIFIERS             |
|----------------|-----------|-----------------------|
|_idUser         |ObjectId   |Primary Key, Not Null  |
|name            |string     |Not Null               |
|hashedPassword  |string     |Not Null               |
|isStudent       |bool       |                       |
|isTeacher       |bool       |                       |
---
### Subjects collection
| FIELD          | TYPE      | MODIFIERS             |
|----------------|-----------|-----------------------|
|_idSubject      |ObjectId   |Primary Key, Not Null  |
|name            |string     |Not Null               |
|idCourse        |ObjectId   |Foreing Key, Not Null  |
---
### Courses collection
| FIELD          | TYPE      | MODIFIERS             |
|----------------|-----------|-----------------------|
|_idCourse       |ObjectId   |Primary Key, Not Null  |
|name            |string     |Not Null               |
---
### Finances collection
| FIELD             | TYPE      | MODIFIERS             |
|-------------------|-----------|-----------------------|
|_idFinance         |ObjectId   |Primary Key, Not Null  |
|installmentsNumber |int        |Not Null               |
|fullPrice          |double     |Not Null               |
|idUser             |ObjectId   |Foreing Key, Not Null  |
---
### Finances Installments collection
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idFinanceInstallments |ObjectId   |Primary Key, Not Null  |
|price                  |double     |Not Null               |
|installmentNumber      |int        |Not Null               |
|status                 |int        |Not Null               |
|idFinance              |int        |Foreing Key, Not Null  |
|paid                   |double     |                       |
---
### Classes collection
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClass               |ObjectId   |Primary Key, Not Null  |
|start                  |timestamp  |Not Null               |
|estimatedEnd           |timestamp  |Not Null               |
|end                    |timestamp  |                       |
|idSubject              |ObjectId   |Foreing Key, Not Null  |
---
### Classes Days collection
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClassDay            |ObjectId   |Primary Key, Not Null  |
|date                   |timestamp  |Not Null               |
|idClass                |ObjectId   |Foreing Key, Not Null  |
---
### Classes Users collection
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClassUser           |ObjectId   |Primary Key, Not Null  |
|idUser                 |ObjectId   |Foreing Key, Not Null  |
|idClass                |ObjectId   |Foreing Key, Not Null  |
---
### Classes User Day collection
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClassUserDay        |ObjectId   |Primary Key, Not Null  |
|presence               |boll       |                       |
|idClassUser            |ObjectId   |Foreing Key, Not Null  |
|idClassDay             |ObjectId   |Foreing Key, Not Null  |
---
### Classes Activities collection
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClassActivity       |ObjectId   |Primary Key, Not Null  |
|date                   |timestamp  |Not Null               |
|idClass                |ObjectId   |Foreing Key, Not Null  |
---
### Classes User Activities collection
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClassUserActivity   |ObjectId   |Primary Key, Not Null  |
|grade                  |string     |                       |
|isExam                 |bool       |                       |
|idClassActivity        |ObjectId   |Foreing Key, Not Null  |
|idClassUser            |ObjectId   |Foreing Key, Not Null  |
---
### Warning collection
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idWarning             |ObjectId   |Primary Key, Not Null  |
|description            |string     |Not Null               |
|title                  |string     |Not Null               |
---
### Calendar Events collection
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idCalendarEvent       |ObjectId   |Primary Key, Not Null  |
|start                  |timestamp  |Not Null               |
|end                    |timestamp  |Not Null               |
|description            |string     |Not Null               |
|idSubject              |ObjectId   |Foreing Key            |
|idClassUser            |ObjectId   |Foreing Key            |
|idClass                |ObjectId   |Foreing Key            |
|idWarning              |ObjectId   |Foreing Key            |
