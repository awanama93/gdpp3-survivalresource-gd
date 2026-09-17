[[Character#Ally character|Ally character]] bisa melakukan sejumlah action yang tidak bisa dilakukan character lain, yaitu:

## Mengelola resource

### Menghancurkan resource prop

- Ally character bisa menghancurkan [[TipeInteractiveProp#Resource Prop|resource prop]]
- Ally character menghancurkan resource prop untuk mengumpulkan resource
- Ally character menghancurkan resource prop dengan menggunakan [[Axe#Menghancurkan resource prop|axe]]
- Daftar resource prop yang bisa dihancurkan oleh ally character ada pada begian berikut: [[TipeInteractiveProp#Resource Prop|resource prop]]
- Terdapat perbedaan dalam pengambilan keputusan menghancurkan resource prop antara player character dan civilian

### Mengumpulkan resource

- Ally character bisa mengumpulkan [[Resource|resource]] setelah [[TipeInteractiveProp#Resource Prop|resource prop]] hancur
- Semua resource yang dikumpulkan ally character dimasukkan ke dalam data yang sama. Jadi, baik player character maupun civilian, ketika mengumpulkan resource, akan ditambahkan ke data resource yang sama
- Daftar resource yang bisa dikumpulkan ally character dari resource prop bisa dilihat pada bagian ini: [[Resource#Raw Resource|raw resource]] dan [[Resource#Special Resource|special resource]]
- Action mengumpulkan resource terjadi secara instan begitu resource prop tersebut [[InteractivePropState#Destroyed|hancur]]
- Terdapat perbedaan dalam proses mengumpulkan resource antara player character dan civilian

### Mengolah resource

- Ally character bisa mengolah resource menggunakan [[TipeInteractiveProp#Processing prop|processing prop]]
- Untuk mengolah resource, ally character cukup berinteraksi dengan processing prop jika memiliki resource yang cukup
- Berbeda dari mengumpulkan resource, mengolah resource dengan processing prop akan menghasilkan [[Resource#Processed Resource|processed resource]] yang memiliki wujud dalam game space
- Action mengolah resource terjadi tidak secara instan, melainkan membutuhkan [[InteractivePropBehaviour#Timer|waktu]] untuk dilakukan
- Terdapat perbedaan dalam proses mengolah resource antara player character dan civilian

### Membawa processed resource

- Ally character bisa membawa [[Resource#Processed Resource|processed resource]]
- Ketika ally character membawa [[Resource#Processed Resource|processed resource]], player bisa melihatnya dalam wujud object yang ada pada game space
- Ally character hanya bisa membawa satu tipe processed resource pada satu waktu
- Tipe processed resource yang dibawa ditentukan oleh processed resource pertama yang dibawa oleh ally character
- Jika ingin membawa tipe processed resource yang lain, maka ally character harus menyimpan dulu semua processed resource yang sedang dia bawa di [[InteractivePropBehaviour#Containable|containable interactive prop]]
- Jika ally character sedang membawa processed resource lalu dia menyentuh processed resource tipe lain, maka tipe lain itu akan diabaikan dan tidak dibawa

### Menyimpan processed resource

- Ally character bisa menyimpan [[Resource#processed resource|processed resource]] di [[InteractivePropBehaviour#Containable|containable interactive prop]]
- Ketika suatu [[Resource#processed resource|processed resource]] disimpan di [[InteractivePropBehaviour#Containable|containable interactive prop]], maka secara visual player bisa melihat wujud fisiknya disimpan bertumpuk di sebelah containable interactive prop tersebut
- Action menyimpan processed resource tidak terjadi secara instan melainkan selama object fisik processed resource tersebut dipindahkan dari character ke samping prop tersebut

### Menyimpan medicine

- Ally character bisa menyimpan [[Resource#Medicine|medicine]] yang sudah diolah lewat [[TipeInteractiveProp#Apotechary Table|apotechary table]] di [[TipeInteractiveProp#Stretcher|stretcher]]
- Medicine yang disimpan di stretcher akan digunakan untuk mengobati civilian
- Ally character menyimpan medicine dengan menyentuh stretcher ketika membawa medicine
- Action menyimpan medicine tidak terjadi secara instan melainkan selama object fisik medicine tersebut dipindahkan dari character ke samping stretcher tersebut

### Menyimpan food

- Ally character bisa menyimpan [[Resource#Food|food]] di [[TipeInteractiveProp#Dinning station|dinning station]]
- Food yang disimpan di dinning station akan digunakan untuk character makan
- Action menyimpan food tidak terjadi secara instan melainkan selama object fisik food tersebut dipindahkan dari character ke samping dinning station tersebut
- Terdapat perbedaan dalam proses menyimpan food antara player character dan civilian

### Memperbaiki defense prop dan facility prop

- Ally character bisa memperbaiki [[TipeInteractiveProp#Defense prop|defense prop]] maupun [[TipeInteractiveProp#Facility prop|facility prop]]
- Memperbaiki prop tersebut dilakukan dengan cara ally character menyentuh trigger perbaikan dari prop tersebut
- Agar ally character bisa melakukan action memperbaiki tersebut, berikut syarat yang harus dipenuhi:
  - Ally character harus memiliki resource sesuai dengan [[RepairMaterials|repair materials]] yang dibutuhkan prop tersebut
- Action memperbaiki prop tidak terjadi secara instan melainkan membutuhkan [[InteractivePropBehaviour#Timer|waktu]] untuk dilakukan
- Terdapat perbedaan dalam proses memperbaiki antara player character dan civilian

## Survival

### Mengobati civilian

- Ally character bisa mengobati [[Character#Civilian|civilian]] yang [[CivilianState#Sakit|sakit]]
- Agar ally character bisa mengobati civilian, berikut adalah syarat yang harus dipenuhi:
  - Civilian yang sakit tersebut [[CivilianAction#Menempati stretcher|menempati stretcher]]
  - [[TipeInteractiveProp#Stretcher|Stretcher]] tersebut [[InteractivePropBehaviour#Containable|menyimpan]] minimal 1 [[Resource#Medicine|medicine]]
  - Ally character berinteraksi dengan stretcher tersebut
- Jika salah satu syarat tersebut tidak terpenuhi, maka ally character tidak bisa mengobati civilian
- Action mengobati civilian tidak terjadi secara instan melainkan membutuhkan [[InteractivePropBehaviour#Timer|waktu]] untuk dilakukan
- Terdapat perbedaan dalam proses mengobati civilian sakit antara player character dan civilian

### Makan

- Ally character bisa melakukan action makan
- Makan dilakukan dengan cara berinteraksi dengan [[TipeInteractiveProp#Dinning station|dinning station]]
- Agar ally character bisa makan, berikut syarat yang harus dipenuhi:
  - Dinning station tersebut harus [[InteractivePropBehaviour#Containable|menyimpan]] minimal 1 [[Resource#Food|food]]
  - Jika [[Character#Civilian|civilian]], maka state-nya harus sedang [[CivilianState#Lapar|lapar]]
  - Jika [[Character#Player character|player character]], maka bisa langsung melakukan action makan ketika berinteraksi dengan dinning station ketika [[HealthPoint|health point]] < 100% total health point
- Action makan tidak terjadi secara instan melainkan membutuhkan [[InteractivePropBehaviour#Timer|waktu]] untuk dilakukan
- Terdapat perbedaan dalam proses makan antara civilian dan player character

### Menyerang enemy character

- Ally character HANYA bisa menyerang [[Character#Enemy character|enemy character]]
- Detil tentang menyerang, bisa dibaca pada [[CharacterAction#Menyerang|bagian ini]]
