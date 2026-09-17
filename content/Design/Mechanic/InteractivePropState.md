### Interactive Prop State

Suatu interactive prop bisa memiliki satu atau lebih dari satu state, yaitu:

##### Functional

Semua interactive prop bisa memiliki state functional
Sebuah interactive prop akan functional jika break pointnya > 0
Ketika sebuah interactive prop ada dalam keadaan functional, maka character yang relevan bisa melakukan sesuatu terhadapnya

##### Damaged

Sejumlah interactive prop bisa memiliki state damaged. Sejumlah interactive prop tidak bisa memiliki state damaged
Sebuah interactive prop akan damaged jika break pointnya < 100% dan lebih dari > 0%
Interactive prop yang ada dalam keadaan damaged, bisa diperbaiki oleh ally

##### Broken

Sejumlah interactive prop bisa memiliki state broken. Sejumlah interactive prop tidak bisa memiliki state broken
Sebuah interactive prop akan broken jika break pointnya <= 0
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

##### Closed

Sejumlah interactive prop bisa berada dalam keadaan ditutup (closed)
Ketika suatu interactive prop berada dalam keadaan closed, dia akan menghalangi jalur [[Character]] untuk berjalan

##### Opened

Sejumlah interactive prop bisa berada dalam keadaan dibuka (opened)
Ketika suatu interactive prop berada dalam keadaan opened, dia akan membuka jalur [[Character]] untuk berjalan
