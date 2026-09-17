[[Character#Zombie robot|Zombie robot]] membuat keputusan dengan pertimbangan berikut:

### Default Decision

Default decision dari zombie robot adalah [[CharacterAction#Berjalan|Berjalan]] [[CharacterAction#Arah tuju berjalan|menuju]] [[TipeInteractiveProp#Tower radio|Tower radio]]
Jadi begitu di-spawn di game space, zombie robot akan langsung memilih default decision

### Perubahan Decision

Zombie robot akan mungkin memilih opsi lain jika:
Dalam radiusnya, terdapat lebih dari nol object berikut:

- Character lain, yang meliputi [[Character#Ally character|Ally character]] maupun [[Character#Robber|Robber]] yang [[CharacterState#Hidup|Hidup]]
- [[TipeInteractiveProp#Defense prop|Defense prop]] yang [[InteractivePropState#Functional|Functional]]
- [[TipeInteractiveProp#Tower radio|Tower radio]]

Ketika ada object tersebut ada dalam radius zombie robot, maka dia akan memasukkan object tersebut sebagai opsi target serangan

Lalu, setelah dia memiliki list opsi target serangan, dia akan membuat keputusan dari opsi berikut:

- Melanjutkan default decision (berjalan menuju tower radio) (25% chance)
- [[CharacterAction#Menyerang|Menyerang]] target serangan (75% chance)

#### Prioritas target serangan

Berikut adalah urutan prioritas target serangan zombie robot, jika ada lebih dari satu target serangan yang dimiliki oleh zombie robot. Urutan dimulai dari most prioritized ke least prioritized

- Tower radio
- Player character
- Defense prop
- Civilian
- Robber

#### Attacked decision

Ketika zombie robot melakukan action-nya, bisa jadi ada [[Character]] lain menyerangnya. Jika itu terjadi, zombie akan memutuskan untuk menyerang character yang sedang menyerangnya itu
