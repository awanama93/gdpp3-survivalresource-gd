Semua jenis character bisa melakukan hal berikut walaupun mungkin terdapat beberapa detil yang berbeda:

### Idle

Character bisa idle (diam bergeming)

- Player bisa melihat animasi character idle

### Berjalan

Character bisa berjalan

- Selama berjalan, character berjalan dengan kecepatan konstan (Tidak ada percepatan)
- Player bisa melihat animasi character berjalan
- Player bisa melihat VFX character berjalan
- Player bisa mendengar SFX langkah kaki ketika character berjalan
- Tiap character memiliki perbedaan kecepatan berjalan
- Detil perbedaan behaviour dalam berjalan, dijelaskan pada tiap bagian character

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

### Memasang Equipment

Character bisa memasang equipment yang bisa digunakan untuk melakukan action
Terdapat perbedaan antara player character dengan non-player character dalam memasang equipment

![[Weapon]]

- Tiap character memiliki perbedaan dalam tipe weapon yang dimiliki. Detail tentang ini dijelaskan pada bagian masing-masing character.
  - Player character
  - Ally character
  - Enemy character
- Character memiliki sejumlah perbedaan dalam hal target serangan
  - Ally character hanya bisa menyerang enemy character
  - Tetapi, zombie robot, selain bisa menyerang ally character, bisa juga menyerang robber. Ini dijelaskan pada [[ZombieRobotAction#Menyerang robber|bagian ini]]
  - Sebaliknya, robber, selain bisa menyerang ally character, bisa juga menyerang zombie robot. Ini dijelaskan pada [[RobberAction#Menyerang zombie robot|bagian ini]]

### Action Khusus

Terdapat sejumlah action khusus yang hanya dimiliki beberapa character. Action tersebut adalah:

- ![[AllyCharacterAction|Ally character]]
- ![[PlayerCharacterAction|Player character]]
- ![[CivilianAction|Civilian Action]]
- ![[EnemyCharacterAction|Enemy character]]
- ![[ZombieRobotAction|Zombie robot action]]
- ![[RobberAction|Robber action]]
-
