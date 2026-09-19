Semua jenis character bisa memiliki state berikut walaupun mungkin terdapat beberapa detil yang berbeda:

### Idle

- Idle adalah state yang menandakan character tidak melakukan action apa-apa dan tidak mendeteksi apa-apa dalam radiusnya

### Hidup

- Hidup adalah state yang menandakan character masih berada dalam game space dan bisa melakukan beragam action
- Character hidup jika [[HealthPoint|health point]] > 0

### Mati

- Mati adalah state yang menandakan character dihapus dari game space
- Character mati jika [[HealthPoint|health point]] <= 0

### Aggressive

- Aggresive adalah state yang menandakan character dalam proses melakukan action [[CharacterAction#Menyerang|menyerang]] character lain

### Moving

- Moving adalah state yang menandakan character dalam proses melakukan action [[CharacterAction#Berjalan|berjalan]]

### State Khusus

Terdapat sejumlah state yang dimiliki beberapa character saja. Berikut adalah state tersebut:

- ![[CivilianState|Civilian state]]

- ![[PlayerCharacterState|Player character state]]
