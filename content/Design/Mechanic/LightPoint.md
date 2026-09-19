Light point adalah property yang menentukan apakah [[Character#Player character|Player character]] sedang dalam state [[PlayerCharacterState#Gelap|Gelap]] atau [[PlayerCharacterState#Terang|Terang]]
Light point bertambah seiring waktu jika player character berada di radius [[TipeInteractiveProp#Generator|Generator]]
Light point berkurang seiring waktu jika player character berada di luar radius generator

### Default value

Kecepatan pengurangan light point adalah 5% dari total light point per detik

### Visual information

Secara visual, player bisa melihat perubahan nilai light point melalui user interface maupun dari tingkat keterangan game space
Semakin kecil nilai light point maka game space akan terlihat semakin gelap

TO BE DECIDED: Player bisa membuat light point berkurang lebih lambat dengan melakukan upgrade lamp
