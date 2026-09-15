Axe adalah equipment yang bisa digunakan ([[Equipment Behaviour#Usable|usable]]) untuk:
[[CharacterAction#Menyerang|Menyerang]] jika dipakai oleh semua [[Character]]
[[AllyCharacterAction#Menghancurkan resource prop|Menghancurkan resource prop]] jika dipakai oleh [[Character#Ally character|ally character]]
Axe memiliki [[ActionRadius|action radius]] yang relatif sempit. Jangkauannya hanya mencapai sebelah dari character yang menggunakannya

## Menyerang

### Penentuan target serangan

Jika ada lebih dari satu target serangan di hadapan character, maka ketika action menyerang dilakukan, maka semua character yang ada di hadapan character tersebut terkena serangan

### Penentuan kena serang

Suatu target serangan akan kena serang axe jika dia berada di area serang ketika animasi attack dilakukan
Jadi bisa jadi target tidak kena jika pada saat animasi attack dilakukan dia berjalan menjauh

### Kalkulasi serangan

Jika axe kena ke target serangan maka, [[HealthPoint|health point]] atau [[Break point|break point]] target serangan dikurangi [[Action power|action power]] dari axe
Tidak ada kalkulasi yang kompleks

## Menghancurkan resource prop

### Mulai menghancurkan

[[Character#Ally character|Ally character]] yang menggunakan axe akan mulai [[AllyCharacterAction#Menghancurkan resource prop|menghancurkan]] [[TipeInteractiveProp#Resource Prop|resource prop]] jika pada [[ActionRadius|action radius]]-nya terdapat resource prop yang [[InteractivePropState#Functional|functional]]

### Penentuan target penghancuran

[[Character#Ally character|Ally character]] bisa saja menghancurkan lebih dari satu resource prop dalam waktu yang bersamaan jika ketika action menghancurkan terjadi, ada lebih dari satu resource prop dalam area serang

### Kalkulasi penghancuran

Setiap kali axe mengenai resource prop, maka [[Break point|break point]] prop tersebut dikurangi [[Action power|action power]] dari axe
Tidak ada kalkulasi yang kompleks
