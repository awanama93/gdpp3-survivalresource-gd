Civilian bisa memiliki state yang tidak dimiliki character lain:

### Sakit

- Civilian bisa sakit
- Sakit terjadi ketika [[HealthPoint|health point]] civilian mencapai 10% dari total [[HealthPoint|health pointnya]]
- Civilian yang sakit akan langsung memutuskan untuk [[CharacterAction#Berjalan|berjalan]] menuju bunk mana pun yang kosong
- Selama [[CharacterAction#Berjalan|berjalan]] menuju bunk, civilian mungkin diserang oleh enemy character. Jika civilian diserang enemy, maka civilian akan memutuskan untuk [[AllyCharacterAction#Menyerang enemy character|menyerang enemy character]]
- Jika tidak ada bunk yang kosong, maka
- Civilian yang sakit tidak bisa diberikan task apa pun

### Lapar

- Civilian bisa lapar
- Lapar terjadi ketika [[HealthPoint|health point]] civilian...
- Civilian yang lapar bisa memutuskan untuk [[CharacterAction#Berjalan|berjalan]] menuju kitchen
- Civilian yang lapar bisa saja diberikan task

### Menunggu

- Civilian bisa menunggu ketika tidak diberikan pekerjaan atau tidak ada pekerjaan yang bisa dilakukan

### Menambang

- Civilian berada dalam keadaan menambang ketika dia akan melakukan action [[AllyCharacterAction#Menghancurkan resource prop|menghancurkan resource prop]]
- [[AllyCharacterAction#Mengolah resource|mengolah resource]] dari [[Resource#Raw Resource|raw resource]] menjadi [[Resource#Processed Resource|processed resource]] dengan action melalui [[TipeInteractiveProp#Processing prop|processing prop]]

### Merawat

- Civilian berada dalam keadaan merawat ketika dia akan melakukan action berikut:
  - [[AllyCharacterAction#Menyimpan food|menyimpan food]]
  - [[AllyCharacterAction#Menyimpan medicine|menyimpan medicine]]
  - [[AllyCharacterAction#Mengobati civilian|mengobati civilian]]
  - [[AllyCharacterAction#Memperbaiki defense prop dan facility prop|memperbaiki defense prop dan facility prop]]

### Waspada

- Civilian berada dalam keadaan waspada ketika dia akan melakukan action berikut:
  - [[Berpatroli]]
  - [[CharacterAction#Menyerang|Menyerang]]
