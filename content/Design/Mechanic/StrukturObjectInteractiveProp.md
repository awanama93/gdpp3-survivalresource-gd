Suatu interactive prop bisa memiliki struktur object sebagai berikut:

### Visual mesh

Visual mesh adalah bagian dari interactive prop yang menunjukkan bentuk visual dari prop tersebut

### Break point indicator

Interactive prop yang [[InteractivePropBehaviour#Breakable|breakable]] akan memunculkan indikator [[Break point|break point]] di atas object tersebut di game space ketika [[Character]] [[CharacterAction|menyerang]]-nya
Selain itu, interactive prop yang [[InteractivePropBehaviour#Repairable|repairable]] akan memunculkan juga indikator [[Break point|break point]] di atas object tersebut di game space ketika [[Character#Ally character|ally character]] [[AllyCharacterAction#Memperbaiki defense prop dan facility prop|memperbaiki]]-nya

### Action trigger box

Action trigger box adalah bagian dari interactive prop yang bisa:

- Dimunculkan agar player bisa melihat bahwa object tersebut adalah interactive prop yang bisa diinteraksi oleh [[Character#Player character|player character]], setidaknya
- Ditabrak oleh [[Character#Ally character|ally character]] untuk melakukan action yang berkaitan dengan interactive prop tersebut

Secara visual, action trigger box tampak seperti plane yang ada di dekat interactive prop dan menunjukkan sejumlah informasi [[Resource]], seperti  yang relevan dengan interactive prop tersebut

Action trigger box bisa saja digunakan untuk memicu terjadinya action berikut:

#### Buildable

Pada [[InteractivePropBehaviour#Buildable|buildable]] interactive prop ketika [[Character#Player character|player character]] menyentuh action trigger box dan [[Character#Ally character|ally character]] memiliki [[Resource]] sejumlah [[Upgrade materials#Build materials|build materials]]-nya, maka akan action membangun akan dimulai
Jika resource yang dimiliki ally character tidak mencukupi build materials, maka:

- player akan melihat dan mendengar notifikasi tentang resource tidak mencukupi,
- lalu quest akan...

#### Repairable

Pada [[InteractivePropBehaviour#Repairable|repairable]] interactive prop ketika  [[Character#Ally character|ally character]] menyentuh action trigger box dan [[Character#Ally character|ally character]] memiliki [[Resource]] sejumlah [[RepairMaterials|repair materials]]-nya, maka akan action memperbaiki akan dimulai
Jika resource yang dimiliki ally character tidak mencukupi repair materials, maka:

- player akan melihat dan mendengar notifikasi tentang resource tidak mencukupi,
- lalu quest akan...

#### Occupiable

Pada [[InteractivePropBehaviour#Occupiable|occupiable]] interactive prop ketika [[Character#Ally character|ally character]] yang relevan menyentuh action trigger box, maka action berikut (sesuai dengan interactive prop-nya) akan dimulai:

- [[AllyCharacterAction#Makan|makan]]
- [[CivilianAction#Menempati stretcher|menempati stretcher]]
  Relevansi [[Character#Civilian|civilian]] didasarkan pada [[CivilianState|state]]-nya:
  Jika [[CivilianState#Lapar|lapar]] maka bisa [[AllyCharacterAction#Makan|makan]]
  Jika [[CivilianState#Sakit|sakit]] maka bisa [[CivilianAction#Menempati stretcher|menempati stretcher]]
  Sementara itu, [[Character#Player character|player character]] bisa melakukan action makan ketika [[HealthPoint|health point]]-nya < 100%
  Player character tidak bisa menempati stretcher

#### Containable

Pada [[InteractivePropBehaviour#Containable|containable]] interactive prop ketika [[Character#Ally character|ally character]] menyentuh action trigger box dan ally character membawa [[Resource#Processed Resource|processed resource]] yang sesuai dengan interactive prop tersebut, maka action [[AllyCharacterAction#Menyimpan processed resource|menyimpan processed resource]] akan dimulai dan player bisa melihat object processed resource berpindah ke processed resource space
Proses penyimpanan processed resource tersebut akan terus berlangsung selama ally character masih menyentuh action trigger box
Kapan pun begitu ally character keluar dari action trigger box tersebut, maka proses penyimpanan processed resource tersebut berhenti, walaupun belum semua resource disimpan

#### Openable

Pada [[InteractivePropBehaviour#Openable|openable]] interactive prop ketika [[Character#Player character|player character]] menyentuh action trigger box dan player character membawa [[Resource#Lockpick|lockpick]] sejumlah [[UnlockMaterials|unlock materials]]-nya, maka action [[PlayerCharacterAction#Membuka gating prop|membuka gating prop]] akan dimulai
Player bisa melihat dan mendengar [[TipeInteractiveProp#Gating prop|gating prop]] terbuka (gating prop menjalankan animasi terbuka)

#### Upgradive

Pada [[InteractivePropBehaviour#Upgradive|upgradive]] interactive prop ketika [[Character#Player character|player character]] menyentuh action trigger box dan player character membawa sejumlah [[Upgrade materials|upgrade materials]] yang cukup, maka action [[PlayerCharacterAction#Mengupgrade interactive prop|mengupgrade interactive prop]] atau [[PlayerCharacterAction#Mengupgrade equipment|equipment]] akan dimulai

#### Actioncapable

Pada [[InteractivePropBehaviour#Actioncapable|actioncapable]] interactive prop ketika [[Character#Ally character|ally character]] yang relevan menyentuh action trigger box, maka action yang relevan dengan interactive prop tersebut akan dimulai
Relevansi character dan relevansi action didasarkan pada [[TipeInteractiveProp|tipe interactive prop]]-nya dan [[Resource]] yang dimiliki

### Processed resource space

Suatu interactive prop yang [[InteractivePropBehaviour#Containable|containable]] untuk menyimpan [[Resource#Processed Resource|processed resource]], memiliki satu bagian di mana processed resource yang disimpan di situ diletakkan
Jadi secara visual, player bisa melihat di sebelah mana location dari object processed resource tersebut
Object processed resource yang disimpan di interactive prop tersebut disusun secara rapi dan bertumpuk ketika [[Character#Ally character|ally character]] menyimpannya
Ketika [[Character#Robber|robber]] [[RobberAction#Mencuri processed resource|mencuri processed resource]], maka secara visual object processed resource yang paling atas dan paling awal (pinggir) dari tumpukan itu yang diambil terlebih dulu

### Occupying character space

Suatu interactive prop yang [[InteractivePropBehaviour#Occupiable|occupiable]] untuk ditempati oleh [[Character#Ally character|ally character]], memiliki suatu bagian di mana ally character yang sedang menempati interactive prop itu berada
Ketika suatu character menempati interactive prop tersebut, maka player bisa melihat animasi character yang sesuai dengan interactive prop tersebut

### Radius

Suatu interactive prop yang [[InteractivePropBehaviour#Aggroable|aggroable]] memiliki [[ActionRadius|action radius]] dengan cara kerja yang sama seperti action radius milik [[Equipment]]
