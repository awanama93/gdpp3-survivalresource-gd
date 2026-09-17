[[Character#Player character|Player character]] bisa melakukan sejumlah action yang tidak bisa dilakukan character lain, yaitu:

## Mengeksplorasi

### Mengisi ulang light point

- Player character bisa mengisi ulang [[LightPoint|light point]]
- Player character mengisi ulang light point dengan cara berada pada radius dari [[TipeInteractiveProp#Generator|generator]]

### Menyalakan activable prop

- Player character bisa menyalakan [[InteractivePropBehaviour#Activeable|activable prop]], yang salah satunya adalah [[TipeInteractiveProp#Generator|generator]]
- Untuk menyalakan generator, player character perlu menyentuh trigger generator

### Membuka gating prop

- Player character bisa membuka [[TipeInteractiveProp#Gating prop|gating prop]] jika menyentuhnya ketika memiliki [[UnlockMaterials|unlock material]] yang dibutuhkan

## Membangun dan mengupgrade

### Membangun tower radio

- Player character bisa membangun [[TipeInteractiveProp#Tower radio|tower radio]] jika memiliki [[Upgrade materials|upgrade material]] atau [[Upgrade materials#Build materials|build material]] yang dibutuhkan
- Player character bisa membangun tower radio dengan menyentuh trigger tower radio ketika memiliki material yang dibutuhkan

### Membangun facility prop

- Player character bisa membangun [[TipeInteractiveProp#Facility prop|facility prop]] jika memiliki [[Upgrade materials|upgrade material]] atau [[Upgrade materials#Build materials|build material]] yang dibutuhkan
- Player character bisa membangun tower radio dengan menyentuh trigger facility prop ketika memiliki material yang dibutuhkan

### Membangun defense prop

- Ally character bisa membangun [[TipeInteractiveProp#Defense prop|defense prop]]
- Membangun defense prop dilakukan dengan cara ally character menyentuh trigger pembangunan defense prop
- Agar ally character bisa melakukan action membangun defense prop, berikut syarat yang harus dipenuhi:
  - Ally character harus memiliki resource sesuai dengan [[Upgrade materials#Build materials|build material]] dari defense prop tersebut
- Action membangun defense prop tidak terjadi secara instan melainkan membutuhkan [[InteractivePropBehaviour#Timer|waktu]] untuk dilakukan
- Terdapat perbedaan dalam proses membangun defense prop antara player character dan civilian

### Mengupgrade equipment

- Player character bisa mengupgrade [[Equipment]] jika memiliki [[Upgrade materials|upgrade material]]  yang dibutuhkan ketika menyentuh [[TipeInteractiveProp#Tool rack|tool rack]] atau [[TipeInteractiveProp#Weaponry|weaponry]]
- Jika player character melakukan upgrade equipment, maka bukan hanya equipment milik player character yang di-upgrade, melainkan juga equipment yang dimiliki oleh semua character lain, mulai dari [[Character#Civilian|civilian]] sampai [[Character#Enemy character|enemy character]] yang tipenya sama. Misalnya, player character mengupgrade axe, maka axe yang dimiliki character lain akan ikut ter-upgrade

### Mengupgrade interactive prop

- Player character bisa mengupgrade [[InteractiveProp|interactive prop]] jika memiliki [[Upgrade materials|upgrade material]]  yang dibutuhkan ketika menyentuh [[TipeInteractiveProp#Bookcase|bookcase]] yang relevan
- Jika player character melakukan upgrade interactive prop, maka semua prop yang bertipe sama akan ikut ter-upgrade. Misalnya, player character mengupgrade turret, maka semua turret yang ada di game space akan ikut ter-upgrade

## Mengelola civilian

### Civilian task assignment

- Player character bisa melakukan civilian task assignment
- Civilian task assignment adalah action di mana player memberikan task pada civilian
- Untuk memulai civilian task assignment, player character harus menyentuh [[TipeInteractiveProp#Civilian task board|Civilian task board]]
- Ketika player character menyentuh civilian task board, player bisa melihat task board user interface muncul
- Pada task board user interface, player bisa melihat informasi berikut:
  - Daftar civilian beserta state dan action-nya
  - Opsi task yang diberikan pada civilian
