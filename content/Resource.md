Resource adalah object yang digunakan untuk melakukan beragam [[AllyCharacterAction|ally character action]]

### Tipe Resource

Terdapat 2 jenjang dan 10 tipe resource dalam game ini, yaitu

#### Raw Resource

Raw resource adalah resource yang didapatkan langsung ketika [[Character#Ally character|Ally character]] [[AllyCharacterAction#Menghancurkan resource prop|menghancurkan resource prop]] lalu [[AllyCharacterAction#Mengumpulkan resource|mengumpulkan resource]]

##### Plant

##### Meat

##### Fluid

##### Mechanical scrap

##### Natural scrap

##### Electrical scrap

#### Processed Resource

Processed resource adalah resource yang didapatkan [[Character#Ally character|Ally character]] setelah [[AllyCharacterAction#Mengolah resource|mengolah resource]] melalui [[InteractiveProp|interactive prop]] yang sesuai

##### Food

Food adalah processed resource yang dihasilkan dari [[AllyCharacterAction#Mengolah resource|mengolah resource]] [[Resource#Plant|plant]] dan [[Resource#Meat|meat]] lewat interaksi dengan [[TipeInteractiveProp#Kitchen|kitchen]]

##### Medicine

Medicine adalah processed resource yang dihasilkan dari [[AllyCharacterAction#Mengolah resource|mengolah resource]] [[Resource#Plant|plant]] dan [[Resource#Fluid|fluid]] lewat interaksi dengan [[TipeInteractiveProp#Apotechary Table|apothecary table]]

##### Sparepart

Sparepart adalah processed resource yang dihasilkan dari [[AllyCharacterAction#Mengolah resource|mengolah resource]] [[Resource#Mechanical scrap|mechanical scrap]] dan [[Resource#Electrical scrap|electrical scrap]] lewat interaksi dengan [[TipeInteractiveProp#Machinist bench|machinist bench]]

##### Component

Component adalah processed resource yang dihasilkan dari [[AllyCharacterAction#Mengolah resource|mengolah resource]] [[Resource#Mechanical scrap|mechanical scrap]] dan [[Resource#Natural scrap|natural scrap]] lewat interaksi dengan [[TipeInteractiveProp#Woodwork bench|woodwork bench]]

#### Special Resource

Special resource adalah resource yang memiliki fungsi berbeda dari resource lainnya. Dalam game ini terdapat special resource berikut:

##### Lockpick

Lockpick adalah special resource yang digunakan oleh [[Character#Player character|player character]] untuk [[InteractivePropBehaviour#Openable|membuka]] [[TipeInteractiveProp#Gating prop|gating prop]]

### Penyimpanan resource

Ally character menyimpan resource di resource storage yang sama. Jadi baik ketika player character maupun civilian mendapatkan resource, maka resource yang didapatkan akan diakumulasikan
Player bisa melihat kuantitas semua resource yang dimiliki ally character sepanjang waktu

### Penambahan Resource

Sepanjang permainan ada sejumlah cara agar resource bertambah, yaitu:
[[AllyCharacterAction#Menghancurkan resource prop|Menghancurkan resource prop]]
[[CharacterAction#Menyerang|Menyerang]] enemy character
[[AllyCharacterAction#Mengolah resource|Mengolah resource]]

### Pengurangan Resource

Sepanjang permainan ada sejumlah cara agar resource berkurang, yaitu:
[[AllyCharacterAction#Mengolah resource|Mengolah resource]]
[[AllyCharacterAction#Mengobati civilian|Mengobati civilian]]
[[AllyCharacterAction#Memberi makan civilian|Memberi makan civilian]]
[[AllyCharacterAction#Makan|Makan]]
[[AllyCharacterAction#Membangun defense prop|Membangun defense prop]]
[[AllyCharacterAction#Membangun facility prop|Membangun facility prop]]
[[AllyCharacterAction#Memperbaiki defense prop dan facility prop|Memperbaiki defense prop dan facility prop]]
