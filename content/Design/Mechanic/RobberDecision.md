[[Character#Robber|Robber]] membuat keputusan dengan pertimbangan berikut:

### Default decision

Default decision dari robber adalah [[Berpatroli]]
Jadi begitu di-spawn di game space, robber akan langsung memilih default decision

### Attacked decision

Ketika robber melakukan action-nya, bisa jadi ada [[Character]] lain menyerangnya. Jika itu terjadi, robber akan memutuskan untuk menyerang character yang sedang menyerangnya itu

### Perubahan Decision

Robber akan mungkin memilih opsi lain jika:
Dalam radiusnya, terdapat lebih dari nol object berikut:

- Character lain, yang meliputi [[Character#Ally character|Ally character]] maupun [[Character#Zombie robot|Zombie robot]] yang [[CharacterState#Hidup|Hidup]]
- [[TipeInteractiveProp#Defense prop|Defense prop]] yang [[InteractivePropState#Functional|Functional]]
- [[TipeInteractiveProp#Facility prop|Facility prop]] yang [[InteractivePropState#Functional|Functional]]
- [[Resource#Processed Resource|Processed Resource]] yang disimpan di [[InteractivePropBehaviour#Containable|Containable]] [[TipeInteractiveProp|interactive prop]]

Ketika ada object tersebut ada dalam radius zombie robot, maka dia akan memasukkan object tersebut sebagai opsi target serangan

Lalu, setelah dia memiliki list opsi target serangan, dia akan membuat keputusan dari opsi berikut:

- Melanjutkan default decision (berpatroli) (20% chance)
- [[RobberAction#Mencuri processed resource|Mencuri processed resource]] (40% chance)
- [[CharacterAction#Menyerang|Menyerang]] target serangan (40% chance)

#### Prioritas target serangan

Berikut adalah urutan prioritas target serangan zombie robot, jika ada lebih dari satu target serangan yang dimiliki oleh zombie robot. Urutan dimulai dari most prioritized ke least prioritized

- Facility prop
- Player character
- Zombie robot
- Defense prop
- Civilian
