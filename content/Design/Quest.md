Quest adalah pemberi arah bagi player tentang apa yang harus dilakukan dalam waktu dekat
Tujuan dari kehadiran quest dalam game ini adalah agar player bisa menyadari apa momen-to-moment objective dalam game ini

### Informasi Quest

Pada satu waktu player hanya bisa melihat satu active quest
Struktur informasi yang disajikan pada quest adalah:

- Informasi action yang perlu dilakukan oleh player
- Satu tipe object yang relevan dengan quest
- Property yang relevan dengan quest
- Nilai kuantitas dari property tersebut
- Progress penyelesaian quest dalam hal kuantitas

Format deskripsi quest: action - objectA - objectB (jika diperlukan lebih dari satu object) - nilai kuantitas - property
Contoh:

- Upgrade tower radio to level 10 (current level: 1)
- Prepare 1 food for the dinning station (current food in dinning station: 0)
- Tend 1 civilian in the stretcher (current tended civilian: 0)
- Kill 10 zombie robot (current killed zombie: 3)

### Aktivasi Quest

Suatu quest bisa diaktifkan dengan cara [[Character#Player character|Player character]] berinteraksi dengan [[Object]]

### Tipe Quest

Upgrade tower
Kill zombie robot wave

Incidental quest
Upgrade equipment

### Interaksi Quest

Player bisa menekan quest user interface
Ketika player menekan quest interface permainan akan di-pause lalu kamera akan bergeser untuk menyorot relevant object dengan active quest
