Character bisa memiliki satu atau lebih property yang dijelaskan pada bagian ini:

![[HealthPoint]]

### Active State

Active state adalah property yang menunjukkan state apa saja yang aktif dimiliki character

Suatu character bisa jadi memiliki lebih dari satu:
Misalnya, Civilian bisa memiliki active state [[CharacterState#Hidup|Hidup]], [[CharacterState#Moving|Moving]], dan [[CivilianState#Lapar|Lapar]] dalam waktu yang sama

### Action Decision

Action decision adalah property yang menunjukkan apa [[CharacterAction|action]]  yang sedang dipilih oleh character dan apa target dari action tersebut
Contoh: Zombie robot memutuskan untuk melakukan default decisionnya, yaitu berjalan menuju tower radio

- Action: [[CharacterAction#Berjalan|Berjalan]]
- Target: [[TipeInteractiveProp#Tower radio|Tower radio]]

### Equipment

Equipment adalah property yang menunjukkan tentang [[Equipment]] apa yang digunakan oleh character

## Property khusus

Beberapa character memiliki property yang tidak dimiliki character lainnya, misalnya

### Role

[[CivilianRole|Role]] adalah property yang HANYA dimiliki oleh [[Character#Civilian|Civilian]]
Role adalah property yang akan memengaruhi bagaimana [[CivilianDecision|civilian memutuskan decision]]

### Light point

[[LightPoint|Light point]] adalah property yang HANYA dimiliki oleh [[Character#Player character|Player character]]
