[[Character#Civilian|Civilian]] membuat keputusan didasarkan pada [[CivilianRole|role]]-nya

### Default Decision

Default decision dari civilian adalah [[CharacterAction#Berjalan|berjalan]] [[CharacterAction#Arah tuju berjalan|ke arah]] [[TipeInteractiveProp#Civilian task board|civilian task board]] lalu ketika sampai di sana state-nya menjadi [[CivilianState#Menunggu|menunggu]]

### Attacked decision

Ketika civilian melakukan suatu action, bisa jadi [[Character#Enemy character|Enemy character]] [[CharacterAction#Menyerang|Menyerang]]-nya. Jika hal itu terjadi, maka civilian bisa memilih 2 action:

- Melanjutkan actionnya (40% chance)
- [[CharacterAction#Berjalan|Berjalan]] menuju [[TipeInteractiveProp#Tower radio|Tower radio]] (70% chance)
- Tetapi, jika dia memiliki role [[CivilianRole#Defender|Defender]], maka action [[CharacterAction#Menyerang|Menyerang]] ditambahkan menjadi 1 option lagi. jadi ada 3 available option. Lalu bobot optionnya diubah menjadi:
  - Melanjutkan action (25% chance)
  - Berjalan menuju tower radio (30% chance)
  - Menyerang balik (45% chance)

### Fall-through decision

Jika semua opsi decision tidak mungkin dilakukan oleh civilian, maka walaupun civilian sudah memiliki role, dia akan melakukan [[CivilianDecision#Default Decision|default decision]]
Dia akan baru melakukan action lain, jika opsi lain sudah memungkinkan untuk dilakukan

### Proses Pengambilan Decision

Untuk masuk ke proses ini, seorang civilian harus [[PlayerCharacterAction#Civilian task assignment|diberi role]] terlebih dulu. Jika dia masih [[CivilianRole#Unassigned|unassigned]], maka dia akan langsung memilih [[CivilianDecision#Default Decision|default decision]]

Prosesnya adalah:
Cek [[CivilianState|state]]-nya
Jika statenya adalah [[CivilianState#Lapar|lapar]], maka dia akan:

- mengecek apakah ada [[Resource#Food|food]] di [[TipeInteractiveProp#Dinning station|dinning station]]
  - Jika tidak ada, maka dia akan meneruskan apa pun action yang sedang dia lakukan
  - Jika ada maka, dia akan memutuskan satu dari 2 opsi berikut:
    - [[AllyCharacterAction#Makan|makan]] (50% chance)
    - melanjutkan apa pun action yang sedang dia lakukan (50% chance)

Jika statenya adalah [[CivilianState#Sakit|sakit]], maka dia akan:

- mengecek apakah ada [[TipeInteractiveProp#Stretcher|stretcher]] yang [[InteractivePropBehaviour#Occupiable|tidak ditempati]]
  - Jika tidak ada, maka dia akan meneruskan apa pun action yang sedang dia lakukan
  - Jika ada maka, dia akan memutuskan satu dari 2 opsi berikut:
    - [[CivilianAction#Menempati stretcher|menempati stretcher]] (60% chance)
    - melanjutkan apa pun action yang sedang dia lakukan (40% chance)

Jika statenya bukan sakit atau lapar, maka dia akan melakukan action sesuai dengan rolenya:

#### Gatherer decision

Civilian akan memutuskan dari 2 opsi berikut:

- [[AllyCharacterAction#Menghancurkan resource prop|menghancurkan resource prop]] (60% chance) jika ada [[TipeInteractiveProp#Resource Prop|resource prop]] yang [[InteractivePropState#Functional|functional]] lebih dari 0 di game space. Dia akan memilih resource prop yang tersedia secara random. Jadi bisa jadi dia malah memilih resource prop yang lokasinya jauh dari lokasi dirinya saat itu
- [[AllyCharacterAction#Mengolah resource|mengolah resource]] (40% chance) jika [[Resource#Penyimpanan resource|ally character memiliki resource]] yang cukup untuk melakukan itu

#### Caretaker decision

Civilian akan memutuskan dari 4 opsi berikut:

- [[AllyCharacterAction#Menyimpan food|menyimpan food]]
- [[AllyCharacterAction#Menyimpan medicine|menyimpan medicine]]
- [[AllyCharacterAction#Memperbaiki defense prop dan facility prop|memperbaiki defense prop dan facility prop]]
- [[AllyCharacterAction#Mengobati civilian|mengobati civilian]]

Prosesnya adalah

##### Penentuan available option

pertama, civilian akan mengevaluasi hal-hal berikut:

- jumlah food yang ada pada [[TipeInteractiveProp#Dinning station|Dinning station]]
  - Jika ada dinning station yang memiliki food > 0, maka action menyimpan food akan dijadikan salah satu opsi decision
- jumlah medicine yang ada pada [[TipeInteractiveProp#Stretcher|Stretcher]]
  - Jika ada dinning station yang memiliki medicine > 0, maka action menyimpan medicine akan dijadikan salah satu opsi decision
- jumlah stretcher yang [[InteractivePropState#Occupied|Occupied]]
  - Jika ada stretcher yang occupied, maka action mengobati civilian akan dijadikan salah satu opsi decision
- [[TipeInteractiveProp#Defense prop|Defense prop]] yang [[InteractivePropState#Damaged|Damaged]]
  - Jika ada > 0 defense prop yang damaged, maka memperbaiki defense prop akan dijadikan salah satu opsi decision
- [[TipeInteractiveProp#Facility prop|Facility prop]] yang [[InteractivePropState#Damaged|Damaged]]
  - Jika ada > 0 facility prop yang damaged, maka memperbaiki facility prop akan dijadikan salah satu opsi decision

##### Penentuan decision

kedua, setelah memiliki informasi available option, maka civilian akan memutuskan satu decision berdasarkan option yang tersedia
Bobot decisionnya dibagi rata antara setiap option yang tersedia
Misalnya, hanya ada 2 option yang tersedia, maka chance bagi tiap option untuk dipilih adalah 50%. Jika ada 3 option, maka chance tiap option adalah 30%, dan seterusnya

#### Defender decision

Defender secara default akan melakukan action [[Berpatroli]]
Jika saat berpatroli, dia mendeteksi [[Character#Enemy character|Enemy character]] pada radiusnya, maka ada 2 option yang bisa dia pilih:

- Melanjutkan berpatroli (30% chance)
- [[CharacterAction#Menyerang|Menyerang]] enemy yang ada pada radius tersebut (70% chance)
  - Jika terdapat lebih dari 1 enemy, maka dia akan memilih secara random targetnya. Jadi bisa jadi dia memilih enemy yang berjalan lebih jauh
