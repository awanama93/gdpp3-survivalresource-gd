### Interactive Prop State

Suatu interactive prop bisa memiliki satu atau lebih dari satu state, yaitu:

##### Functional

Semua interactive prop bisa memiliki state functional
Sebuah interactive prop akan functional jika break pointnya > 0
Ketika sebuah interactive prop ada dalam keadaan functional, maka character yang relevan bisa melakukan sesuatu terhadapnya

##### Broken

Sejumlah interactive prop bisa memiliki state broken. Sejumlah interactive prop tidak bisa memiliki state broken
Interactive prop yang ada dalam keadaan broken, bisa diperbaiki oleh ally character

##### Destroyed

Sejumlah interactive prop bisa memiliki state destroyed
Sejumlah interactive prop tidak bisa memiliki state destroyed
Interactive prop yang ada dalam keadaan destroyed, maka akan dihapus dari game space

##### Occupied

Sejumlah interactive prop bisa ditempati (occupied) oleh ally character
Ally character yang menempati interactive prop tersebut menjadi target dari action yang dilakukan pada interactive prop tersebut

##### Operating

Sejumlah interactive prop bisa melakukan suatu action yang membutuhkan waktu. Ketika waktu sedang dihitung saat action sedang dilakukan oleh interactive prop tersebut, maka interactive prop sedang ada dalam state operating
