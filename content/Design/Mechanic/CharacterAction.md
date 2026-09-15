Semua jenis character bisa melakukan hal berikut walaupun mungkin terdapat beberapa detil yang berbeda:

### Standing

Character bisa standing (berdiri diam bergeming)

- Player bisa melihat animasi character idle

### Berjalan

Character bisa berjalan

- Selama berjalan, character berjalan dengan kecepatan konstan (Tidak ada percepatan)
- Player bisa melihat animasi character berjalan
- Player bisa melihat VFX character berjalan
- Player bisa mendengar SFX langkah kaki ketika character berjalan
- Tiap character memiliki perbedaan kecepatan berjalan
- Detil perbedaan behaviour dalam berjalan, dijelaskan pada tiap bagian character

#### Arah tuju berjalan

- Character berjalan menuju arah tertentu
- [[Character#Player character|Player character]] berjalan menuju arah yang ditentukan player
- [[Character#Civilian|Civilian]] berjalan menuju arah sesuai dengan role, state, dan actionnya
- [[Character#Zombie robot|Zombie robot]] secara default berjalan menuju arah posisi [[TipeInteractiveProp#Tower radio|tower radio]] tetapi bisa berubah menjadi menuju target serangan (baik character lain maupun [[TipeInteractiveProp#Defense prop|defense prop]]) bergantung pada [[ZombieRobotDecision|decision]]-nya
- [[Character#Robber|Robber]] secara default berjalan untuk [[RobberAction#Berpatroli|berpatroli]] tapi bisa berubah menuju target serangan (baik character lain maupun [[TipeInteractiveProp#Defense prop|defense prop]]) atau [[Resource#Processed Resource|processed resource]] yang [[InteractivePropBehaviour#Containable|disimpan]] di [[TipeInteractiveProp#Facility prop|facility prop]] dan [[TipeInteractiveProp#Tech prop|tech prop]] bergantung pada [[RobberDecision|decision]]-nya

### Terluka

Character bisa terluka

- Character memiliki [[HealthPoint|health point]]
- Player bisa melihat indikator [[HealthPoint|health point]] character pada waktu tertentu. Perbedaan waktu tertentu ini dijelaskan pada tiap bagian character
- [[HealthPoint|health point]] akan berkurang ketika character terkena serangan
- Player bisa melihat partikel teks ketika character terkena serangan
- Player bisa melihat animasi character terkena damage ketika dia terkena serangan
- Player bisa melihat VFX character terkena damage ketika terkena serangan
- Player bisa mendengar SFX terkena serangan ketika character terkena serangan
- Character memiliki perbedaan nilai [[HealthPoint|health point]]. Detail perbedaan [[HealthPoint|health point]] ini dijelaskan pada tabel stat character

### Menyerang

Character bisa menyerang character lain

- Character menyerang secara otomatis ketika ada opponent dalam jangkauan radius senjatanya
- Jika character sedang dalam keadaan menyerang, character bisa berhenti menyerang jika terjadi decision untuk menggerakkan character (berjalan). Jadi, character hanya akan menyerang jika dia sedang tidak berjalan dan ada opponent dalam radiusnya.
- Character memiliki sejumlah perbedaan dalam hal target serangan
  - Ally character hanya bisa menyerang enemy character
  - Tetapi, zombie robot, selain bisa menyerang ally character, bisa juga menyerang robber. Ini dijelaskan pada [[ZombieRobotAction#Menyerang robber|bagian ini]]
  - Sebaliknya, robber, selain bisa menyerang ally character, bisa juga menyerang zombie robot. Ini dijelaskan pada [[RobberAction#Menyerang zombie robot|bagian ini]]

#### Tahapan menyerang

Agar character bisa melakukan action menyerang, maka berikut tahapan yang perlu dilakukan:

- Character memasang equipment
- Character sedang dalam state idle
- Character melakukan deteksi object dalam radius equipmentnya
- Jika terdapat character lain dalam radius equipmentnya
  - atau prop dalam radius equipmentnya
  - maka character masuk dalam state aggressive
- Mulai hitung mundur equipment

### Memasang Equipment

Character bisa memasang equipment yang bisa digunakan untuk melakukan action

- Terdapat perbedaan antara player character dengan nonplayable character dalam memasang equipment
  - Nonplayable character
    - Pada nonplayable character equipment dipasang secara preset berdasarkan [[NPCEquipmentSetup|NPC equipment setup]]
  - Player character
    - Player character memasang equipment secara otomatis ketika [[PlayerCharacterAction#Mengupgrade equipment|mengupgrade equipment]]
    - Pada awal permainan player sudah memasang [[Axe]] level 1

- Tiap character memiliki perbedaan dalam tipe weapon yang dimiliki. Detail tentang ini dijelaskan pada bagian masing-masing character.
  - Player character
    - Player character bisa memasang [[Axe]] maupun [[Pistol]]
  - Ally character
    - Civilian hanya bisa memasang [[Axe]]
  - Enemy character
    - Robber hanya bisa memasang [[Pistol]]
    - ZombieRobot hanya bisa memasang [[Claw]]

### Action Khusus

Terdapat sejumlah action khusus yang hanya dimiliki beberapa character. Action tersebut adalah:

- ![[AllyCharacterAction|Ally character]]
- ![[PlayerCharacterAction|Player character]]
- ![[CivilianAction|Civilian Action]]
- ![[EnemyCharacterAction|Enemy character]]
- ![[ZombieRobotAction|Zombie robot action]]
- ![[RobberAction|Robber action]]
-
