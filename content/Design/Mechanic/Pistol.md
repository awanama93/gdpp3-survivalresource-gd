Pistol adalah equipment yang bisa digunakan ([[Equipment Behaviour#Usable|usable]]) untuk:
[[CharacterAction#Menyerang|Menyerang]] jika dipakai oleh semua [[Character]]

Pistol memiliki [[ActionRadius|action radius]] yang relatif luas

### Penentuan target serangan

Jika ada lebih dari satu target serangan dalam action radius, maka sebelum serangan dilakukan, akan dilakukan proses penentuan target serangan

#### Random target

Pada level rendah, ketika menyerang, pistol akan memilih satu target dari sekian object yang ada dalam action radius secara sembarang. Dengan demikian, bisa jadi serangan dilakukan ke object yang justru berada di posisi paling jauh dari character yang menyerang

##### Target terdekat

Pada level tinggi, ketika menyerang, pistol akan memilih object dengan posisi paling dekat dengan character yang menggunakan pistol

### Penentuan kena serang

Ketika target serangan telah ditentukan, maka pistol akan meluncurkan proyektil
Arah gerak proyektil ditentukan dari posisi object yang menggunakan pistol dengan posisi target serangan ketika serangan dilakukan
Proyektil bergerak lurus dari posisi object yang menggunakan pistol menuju posisi target serangan
Jadi bisa jadi target serangan tidak kena serang jika target serangan tersebut berjalan tidak pada jalur arah gerak proyektil

### Kalkulasi serangan

Jika proyektil kena ke target serangan maka, [[HealthPoint|health point]] atau [[Break point|break point]] target serangan dikurangi [[Action power|action power]] dari pistol
Tidak ada kalkulasi yang kompleks
