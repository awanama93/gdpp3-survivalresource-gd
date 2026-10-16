Quest adalah pemberi arah bagi player tentang apa yang harus dilakukan dalam waktu dekat
Tujuan dari kehadiran quest dalam game ini adalah agar player bisa menyadari apa momen-to-moment objective dalam game ini

### Informasi Quest

Pada satu waktu player hanya bisa melihat satu active quest
Struktur informasi yang disajikan pada quest adalah:

- Informasi action yang perlu dilakukan oleh player
- Satu tipe object yang relevan dengan quest
- Property yang relevan dengan quest
- Nilai kuantitas dari property tersebut
- Progress penyelesaian quest dalam hal kuantitas

Format deskripsi quest: action - objectA - objectB (jika diperlukan lebih dari satu object) - nilai kuantitas - property
Contoh:

- Upgrade tower radio to level 10 (current level: 1)
- Prepare 1 food for the dinning station (current food in dinning station: 0)
- Tend 1 civilian in the stretcher (current tended civilian: 0)
- Kill 10 zombie robot (current killed zombie: 3)

### Aktivasi Quest

Suatu quest bisa diaktifkan dengan cara [[Character#Player character|Player character]] berinteraksi dengan [[Object]] atau setelah event tertentu

### Interaksi Quest

Player bisa menekan quest user interface
Ketika player menekan quest interface permainan akan di-pause lalu kamera akan bergeser untuk menyorot relevant object dengan active quest

### Tipe Quest

#### Upgrade tower

Ini adalah default quest
Default quest berarti jika tidak ada quest lain yang perlu diselesaikan player character, maka quest yang aktif adalah default quest

##### Objective

Untuk menyelesaikan quest ini, player character harus melakukan 10x upgrade tower
Jika player sudah melakukan upgrade sebanyak 10x maka permainan dinyatakan selesai dan player dinyatakan memenangkan game ini

##### Trigger

Quest ini akan aktif jika tidak ada quest lain yang perlu diselesaikan player character

##### Tracked information

- Jumlah dan tipe resource yang diperlukan untuk mengupgrade 1x tower
- Level tower saat ini

##### Perubahan quest aktif

Jika player character berinteraksi dengan object lain, maka bisa jadi quest yang berkaitan dengan object tersebut akan menjadi quest aktif.

#### Kill zombie robot wave

##### Objective

Mengalahkan semua zombie robot yang di-spawn dalam pembagian wave pada waktu tertentu
Quest ini akan selesai jika semua zombie robot pada semua wave tersebut sudah dikalahkan

##### Trigger

Quest ini akan aktif setelah zombie pertama di-spawn setelah [[TipeInteractiveProp#Tower radio|Tower radio]] di-upgrade

##### Tracked information

- Informasi tentang wave (wave saat ini dan wave total)
- Total zombie robot pada wave tersebut
- Total zombie robot yang sudah dikalahkan pada wave tersebut

##### Perubahan quest aktif

Jika player character berinteraksi dengan object lain, quest tidak akan berubah, quest aktif akan tetap kill zombie robot wave. Perubahan quest hanya akan terjadi jika semua zombie robot sudah dikalahkan.

#### Incidental quest

Incidental quest adalah quest yang diaktifkan jika player character melakukan interaksi tertentu dengan object
Intensi dari quest ini adalah untuk memberikan player sense of objective pada moment-to-moment gameplay. Jadi player selalu merasa ada saja hal yang perlu dikerjakan olehnya
Objective, trigger, dan tracked information dari incidental quest berbeda-beda bergantung tipenya

##### Perubahan quest aktif

Suatu incidental quest akan menjadi quest aktif jika player character melakukan interaksi dengan object kapan pun saat permainan, baik ketika ada incidental quest lain sedang qjadi quest aktif maupun ketika upgrade tower sedang jadi quest aktif. Tetapi, incidental quest tidak akan jadi aktif ketika quest aktifnya adalah [[Quest#Kill zombie robot wave|Kill zombie robot wave]]

##### Tipe incidental quest

![[UpgradeAxe]]

![[UpgradePistol]]

![[KillTheRobber]]

![[AssignCivilianRole]]

![[PrepareFoodAtDinningStation]]

![[EatFood]]

![[PrepareMedicineAtStretcher]]

![[TendTheSick]]

![[GatherProcessedResourceIngredients]]

![[GatherResourcesForUpgradingProp]]

![[GatherResourcesForBuildingDefenseProp]]
![[GatherResourcesForRepairingDefenseProp]]

![[FindLockpick]]
