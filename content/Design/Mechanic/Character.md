Character adalah object yang bergerak di dalam game ini
Character memiliki action, state, dan property yang informasinya bisa dilihat pada bagian berikut:
[[CharacterAction|Character action]]
[[CharacterState|Character state]]
[[CharacterProperty|Character property]]

Terdapat beberapa jenis character dalam game ini:

### Ally character

Ally character adalah character yang mendukung player dalam mencapai goal dari game ini
[[AllyCharacterAction]]

Terdapat beberapa tipe ally character:

##### Player character

Player character adalah playable character yang bisa dikontrol oleh player
[[PlayerCharacterAction]]
[[PlayerCharacterState]]

##### Civilian

Civilian adalah nonplayable ally character yang akan membantu player dalam mencapai goal dari game ini.
[[CivilianAction]]
[[CivilianState]]
[[CivilianRole]]
[[CivilianDecision]]

### Enemy character

Enemy character adalah character yang menghalangi player dalam mencapai goal dari game ini
[[EnemyCharacterAction]]
[[EnemyCharacterDecision]]

Terdapat beberapa tipe enemy character:

##### Zombie robot

Zombie robot adalah nonplayable enemy character yang akan menyerang ally character
[[ZombieRobotAction]]
[[ZombieRobotDecision]]

##### Robber

Robber adalah nonplayable enemy character yang akan menyerang ally character, tapi juga menyerang robot zombie
[[RobberAction]]
[[RobberDecision]]
