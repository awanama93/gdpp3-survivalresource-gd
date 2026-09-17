Sebuah interactive prop bisa memiliki satu atau lebih behaviour. Berikut adalah daftar behaviournya:

##### Breakable

Suatu interactive prop bisa dihancurkan (breakable) oleh character (baik oleh ally character maupun enemy character) yang melakukan action [[CharacterAction#Menyerang|menyerang]] atau [[AllyCharacterAction#Menghancurkan resource prop|menghancurkan resource prop]]
Kalkulasi: ketika character melakukan action tersebut, maka [[Action power]] dari [[Equipment]] character tersebut mengurangi [[Break point]] dari interactive prop tersebut
Timing kalkulasi: proses kalkulasi dilakukan ketika animasi menyerang atau menghancurkan mencapai frame di mana axe menyentuh prop targetnya

##### Occupiable

Suatu interactive prop bisa ditempati oleh [[Character#Ally character|ally character]] (occupiable)
Ketika [[Character#Ally character|ally character]] menempati suatu interactive prop, maka [[Occupancy]] dari interactive prop tersebut bertambah 1
Jika [[Occupancy]] interactive prop tersebut mencapai nilai maksimal (biasanya 1), maka statenya berubah menjadi [[InteractivePropState#Occupied|occupied]]
Jika interactive prop sedang ada dalam state [[InteractivePropState#Occupied|occupied]], maka [[Character#Ally character|ally character]] lain tidak bisa menempati lagi interactive prop tersebut
Jika interactive prop sedang ada dalam state [[InteractivePropState#Occupied|occupied]], lalu [[Character#Ally character|ally character]] melakukan [[InteractivePropBehaviour#Actioncapable|action]] yang relevan dengan interactive prop tersebut, maka statenya berubah menjadi [[InteractivePropState#Operating|operating]]
Ketika suatu occupiable interactive prop sudah occupied dan syarat action-nya sudah terpenuhi, maka action tersebut dimulai
Action yang berkaitan dengan occupiable interactive prop adalah:

- [[AllyCharacterAction#Makan|makan]]
- [[CivilianAction#Menempati stretcher|menempati stretcher]]

##### Productive

Suatu interactive prop bisa menghasilkan satu atau lebih dari satu [[Resource]] (productive) setelah [[Character#Ally character|ally character]] [[AllyCharacterAction#Menghancurkan resource prop|menghancurkan resource prop]] atau [[AllyCharacterAction#Mengolah resource|mengolah resource]]
Setelah menghasilkan [[Resource]], [[TipeInteractiveProp#Resource Prop|resource prop]] akan [[InteractivePropState#Destroyed|destroyed]] dan harus menunggu waktu [[BuildTime]] sampai dia [[InteractivePropBehaviour#Spawnable|di-spawn]] kembali
Tetapi, bagi [[TipeInteractiveProp#Processing prop|processing prop]], setelah menghasilkan [[Resource]], dia tidak akan [[InteractivePropState#Destroyed|destroyed]] tetapi akan tetap [[InteractivePropState#Functional|functional]]
Suatu interactive menghasilkan resource sesuai dengan [[Resource pool]] yang dimilikinya
Kuantitas maupun tipe resource pool tidak akan berubah sepanjang permainan

##### Containable

Suatu interactive prop bisa menyimpan [[Resource]] (containable)
Resource yang disimpan dalam interactive prop adalah resource yang nanti akan dipakai ketika dia [[InteractivePropState#Operating|beroperasi]]
Jadi yang dimaksud resource yang containable ini bukanlah resource yang dihasilkan oleh prop tersebut. Untuk resource yang dihasilkan oleh interactive prop, cek behaviour [[InteractivePropBehaviour#Productive|productive]]
Containable interactive prop memiliki informasi tentang [[ContainedResource|contained resource]]
Jumlah contained resource dalam containable interactive prop bisa bertambah maupun berkurang

##### Spawnable

Suatu interactive prop bisa di-spawn pada game space
Spawnable interactive prop di-spawn pada tempat tertentu
Lokasi spawn suatu spawnable interactive prop adalah sesuatu yang preset
Ketika suatu spawnable interactive prop sudah di-spawn, maka prop tersebut harus [[InteractivePropState#Destroyed|dihancurkan]] terlebih dulu baru [[BuildTime]] dimulai dan setelah itu selesai, maka prop tersebut di-spawn kembali

##### Spawncapable

Suatu interactive prop bisa memicu terjadinya spawn object lain
Jika character, khususnya [[Character#player character|player character]] melakukan action dengan spawncapable interactive prop, bisa saja object lain di-spawn
Ketika player character melakukan action dengan spawncapable interactive prop, maka object lain akan di-spawn pada lokasi spawn-nya
Jika pada saat seharusnya object tersebut di-spawn tetapi jumlah object tersebut yang ada di game space sudah mencapai nilai maksimal, maka object tersebut tidak di-spawn lagi
Ketika player character melakukan action dengan spawncapable interactive prop, dan object yang harus di-spawn sudah di-spawn, maka [[Quest]] otomatis menunjukkan agar player character membunuh semua [[Character#Zombie robot|zombie robot]] terlebih dahulu sebelum bisa melakukan quest lain

##### Spawnincrementor

Suatu interactive prop bisa menambah jumlah maksimal object yang di-spawn, jika character melakukan interaksi dengan interactive prop tersebut
Suatu spawnincrementor interactive prop memiliki akses terhadap data tentang penambahan jumlah maksimal object yang bisa di-spawn di game space
Spawnincrementor menambah jumlah maksimal spawn object berikut:

- [[Character#Civilian|Civilian]]
- [[Character#Zombie robot|Zombie robot]]
- [[Character#Robber|Robber]]

##### Presettable

Lokasi suatu interactive prop bisa preset (presettable) sebelum game dimulai
Nilai prop?

##### Buildable

Suatu interactive prop bisa dibangun oleh HANYA [[Character#Player character|player character]] (buildable)
Lokasi buildable interactive prop ditentukan secara preset
Buildable prop bisa dibangun jika [[Character#Player character|player character]] memiliki sejumlah [[Resource]] sesuai dengan [[Upgrade materials|upgrade materials]] dari interactive prop tersebut dari level 0 ke level 1
Buildable prop memiliki data [[Upgrade materials#Upgrade materials and build materials|build materials]]
Suatu buildable interactive prop memerlukan waktu selama [[BuildTime|build time]] untuk bisa sampai [[InteractivePropState#Functional|functional]] setelah [[Character#Player character|player character]] mulai membangunnya

##### Repairable

Suatu interactive prop bisa diperbaiki oleh ally character (repairable)
Suatu repairable interactive prop bisa memiliki state [[InteractivePropState#Broken|broken]]
Suatu repairable interactive prop baru bisa diperbaiki ketika statenya sudah [[InteractivePropState#Broken|broken]]
Suatu repairable interactive prop akan [[InteractivePropState#Broken|broken]] jika [[Break point]]-nya adalah...
Suatu repairable interactive prop memiliki [[RepairMaterials]]
Ketika suatu repairable interactive prop [[AllyCharacterAction#Memperbaiki defense prop dan facility prop|diperbaiki]] maka [[Break point]]-nya akan menjadi 100% kembali
Suatu buildable interactive prop memerlukan waktu selama [[BuildTime|build time]] untuk bisa sampai [[InteractivePropState#Functional|functional]] setelah [[Character#Ally character|ally character]] mulai memperbaikinya

##### Openable

Suatu interactive prop bisa dibuka HANYA oleh [[Character#Player character|player character]] (openable)
Untuk membuka suatu openable interactive prop, player character harus memiliki sejumlah [[Resource#Lockpick|lockpick]]. Player membutuhkan minimal 1 lockpick dan maksimal 10 lockpick
Suatu openable interactive prop akan berpengaruh terhadap bisa atau tidaknya [[Character]] melewati bagian tempat prop tersebut berada
Suatu openable interactive prop memiliki informasi tentang jumlah lockpick yang dibutuhkan untuk membukanya pada [[UnlockMaterials|unlock materials]]

##### Upgradive

Suatu interactive prop bisa meng-upgrade interactive prop lain atau equipment
Suatu upgradive interactive prop memiliki informasi tentang [[UpgradeTarget|upgrade target]]-nya
Mengupgrade sesuatu dengan upgradive interactive prop terjadi secara instan. Tidak ada waktu tunggu dulu
Agar upgradive interactive prop bisa [[InteractivePropState#Operating|beroperasi]] mengupgrade object lain, maka [[Character#Player character|player character]] harus berinteraksi dengan prop tersebut terlebih dulu
Suatu upgradive memiliki informasi tentang [[Upgrade materials]]

![[Upgradable]]

##### Actioncapable

Suatu interactive prop bisa menjadi tempat character melakukan suatu action

###### Timer

Ketika suatu action dilakukan pada interactive prop, maka akan dimulai waktu pengerjaan action tersebut. Penghitung waktu tersebut adalah [[OperationCooldown|operation cooldown]]

###### Action

Yang dimaksud dengan action pada suatu actioncapable interactive prop adalah action yang dilakukan [[Character#Ally character|ally character]] melalui interaksi dengan interactive prop, yang meliputi:

- [[PlayerCharacterAction#Civilian task assignment|civilian task assignment]]
- [[AllyCharacterAction#Menyimpan food|menyimpan food]]
- [[AllyCharacterAction#Menyimpan medicine|menyimpan medicine]]
- [[AllyCharacterAction#Mengobati civilian|mengobati civilian]]
- [[AllyCharacterAction#Mengolah resource|mengolah resource]]
  Action yang bisa dilakukan pada actioncapable interactive prop bergantung pada tipe interactive prop-nya, silakan cek pada bagian berikut: [[TipeInteractiveProp|tipe interactive prop]]

##### Aggroable

Suatu interactive prop bisa melakukan action [[CharacterAction#Menyerang|menyerang]] [[Character#Enemy character|enemy character]]
Suatu aggroable interactive prop memiliki daya serang sesuai dengan [[Action power|action power]]-nya
Secara behaviour, aggroable interactive prop itu mirip seperti character yang [[CharacterAction#Menyerang|menyerang]] menggunakan [[Pistol]] tetapi tidak bisa berjalan

##### Activeable

Suatu interactive prop bisa diaktifkan oleh [[Character#Player character|player character]] (activeable)
Suatu activable interactive prop memiliki informasi tentang waktu yang dibutuhkan untuk [[PlayerCharacterAction#Menyalakan activable prop|menyalakannya]]
Informasi waktu tersebut berada pada [[OperationCooldown|operation cooldown]] dari prop tersebut
Jika suatu activable prop sudah [[InteractivePropState#Functional|functional]] maka dia akan menjadikan dirinya sendiri sebagai routable
Jika player character berada dalam radius activable interactive prop, maka light pointnya akan terisi ulang secara instan

##### Routeable

Suatu interactive prop bisa menjadi suatu waypoint untuk [[Character#Civilian|civilian]] (routable)
Suatu routable interactive prop memiliki [[InteractivePropProperty#Radius|radius]]
Radius tersebut digunakan untuk mendeteksi apa saja [[TipeInteractiveProp#Resource Prop|resource prop]] yang ada dalam jangkauannya
Ketika suatu routable interactive prop [[InteractivePropState#Functional|functional]], maka:

- Dia akan mendeteksi apa saja [[TipeInteractiveProp#Resource Prop|resource prop]] yang ada dalam jangkauannya
- [[Character#Civilian|civilian]] akan menjadikan resource prop tersebut sebagai opsi resource prop yang bisa dia [[AllyCharacterAction#Menghancurkan resource prop|hancurkan]] agar resourcenya bisa [[AllyCharacterAction#Mengumpulkan resource|dia kumpulkan]]

##### Endtriggerable

Suatu interactive prop bisa memicu selesainya permainan (endtriggerable)
Endtriggrrable interactive prop memiliki informasi tentang [[InteractivePropProperty#End Trigger Requirement|end trigger requirement]] yang berisi syarat untuk memicu terjadinya akhir permainan (tamat)
