# Documentação da modelagem de classes do banco de dados

### Users table
| FIELD          | TYPE      | MODIFIERS             |
|----------------|-----------|-----------------------|
|_idUser         |ObjectId   |Primary Key, Not Null  |
|name            |string     |Not Null               |
|hashedPassword  |string     |Not Null               |
|isStudent       |bool       |                       |
|isTeacher       |bool       |                       |
---
### Subjects table
| FIELD          | TYPE      | MODIFIERS             |
|----------------|-----------|-----------------------|
|_idSubject      |ObjectId   |Primary Key, Not Null  |
|name            |string     |Not Null               |
|idCourse        |ObjectId   |Foreing Key, Not Null  |
---
### Courses table
| FIELD          | TYPE      | MODIFIERS             |
|----------------|-----------|-----------------------|
|_idCourse       |ObjectId   |Primary Key, Not Null  |
|name            |string     |Not Null               |
---
### Finances table
| FIELD             | TYPE      | MODIFIERS             |
|-------------------|-----------|-----------------------|
|_idFinance         |ObjectId   |Primary Key, Not Null  |
|installmentsNumber |int        |Not Null               |
|fullPrice          |double     |Not Null               |
|idUser             |ObjectId   |Foreing Key, Not Null  |
---
### Finances Installments table
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idFinanceInstallments |ObjectId   |Primary Key, Not Null  |
|price                  |double     |Not Null               |
|installmentNumber      |int        |Not Null               |
|status                 |int        |Not Null               |
|idFinance              |int        |Foreing Key, Not Null  |
|paid                   |double     |                       |
---
### Classes table
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClass               |ObjectId   |Primary Key, Not Null  |
|start                  |timestamp  |Not Null               |
|estimatedEnd           |timestamp  |Not Null               |
|end                    |timestamp  |                       |
|idSubject              |ObjectId   |Foreing Key, Not Null  |
---
### Classes Days table
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClassDay            |ObjectId   |Primary Key, Not Null  |
|date                   |timestamp  |Not Null               |
|idClass                |ObjectId   |Foreing Key, Not Null  |
---
### Classes Users table
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClassUser           |ObjectId   |Primary Key, Not Null  |
|idUser                 |ObjectId   |Foreing Key, Not Null  |
|idClass                |ObjectId   |Foreing Key, Not Null  |
---
### Classes User Day table
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClassUserDay        |ObjectId   |Primary Key, Not Null  |
|presence               |boll       |                       |
|idClassUser            |ObjectId   |Foreing Key, Not Null  |
|idClassDay             |ObjectId   |Foreing Key, Not Null  |
---
### Classes Activities table
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClassActivity       |ObjectId   |Primary Key, Not Null  |
|date                   |timestamp  |Not Null               |
|idClass                |ObjectId   |Foreing Key, Not Null  |
---
### Classes User Activities table
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idClassUserActivity   |ObjectId   |Primary Key, Not Null  |
|grade                  |string     |                       |
|isExam                 |bool       |                       |
|idClassActivity        |ObjectId   |Foreing Key, Not Null  |
|idClassUser            |ObjectId   |Foreing Key, Not Null  |
---
### Warning table
| FIELD                 | TYPE      | MODIFIERS             |
|-----------------------|-----------|-----------------------|
|_idWarning             |ObjectId   |Primary Key, Not Null  |
|description            |string     |Not Null               |
|title                  |string     |Not Null               |
---
### Calendar Events table
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
