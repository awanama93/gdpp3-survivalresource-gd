Terdapat sejumlah tipe interactive prop dalam game ini, yaitu:

### Resource Prop

Resource prop adalah interactive prop yang:
[[InteractivePropBehaviour#Breakable|Breakable]] oleh [[Character#Ally character|ally character]]
[[InteractivePropBehaviour#Productive|Productive]] menghasilkan [[Resource#Raw Resource|raw resource]]
[[InteractivePropBehaviour#Spawnable|Spawnable]]

#### Street planter

Street planter adalah resource prop yang:
[[InteractivePropBehaviour#Productive|Producing]] [[Resource#Plant|plant]]

- Visual

#### Wooden crate

Wooden crate adalah resource prop yang:
[[InteractivePropBehaviour#Productive|Producing]] [[Resource#Natural scrap|natural scrap]]

#### Barrel

Barrel adalah resource prop yang:
[[InteractivePropBehaviour#Productive|Producing]] [[Resource#Fluid|fluid]]

#### Dumpster

Dumpster adalah resource prop yang:
[[InteractivePropBehaviour#Productive|Producing]] [[Resource#Meat|meat]]

#### Vending machine

Dumpster adalah resource prop yang:
[[InteractivePropBehaviour#Productive|Producing]] [[Resource#Electrical scrap|electric scrap]]

#### Maintenance locker

Maintenance locker adalah resource prop yang:
[[InteractivePropBehaviour#Productive|Producing]] [[Resource#Lockpick|lockpick]]

### Facility prop

Facility prop adalah interactive prop yang:
[[InteractivePropBehaviour#Buildable|Buildable]]
[[InteractivePropBehaviour#Occupiable|Occupiable]] oleh [[Character#Ally character|ally character]]
[[InteractivePropBehaviour#Breakable|Breakable]] oleh [[Character#Enemy character|enemy character]]
Mungkin [[InteractivePropBehaviour#Containable|Containable]]
[[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Ally character|ally character]]
Mungkin [[Upgradable]]

Tipe facility prop

#### Civilian task board

Civilian task board adalah facility prop yang:
[[InteractivePropBehaviour#Actioncapable|Action-capable]] HANYA bagi [[Character#Player character|player character]] untuk [[PlayerCharacterAction#Civilian task assignment|civilian task assignment]]

- [[Character#Player character|Player character]] bisa melakukan action tersebut begitu berinteraksi dengan civilian task board. Jadi player character tidak dianggap [[InteractivePropBehaviour#Occupiable|menempati]] civilian task board
  [[InteractivePropBehaviour#Occupiable|Occupiable]] HANYA oleh [[Character#Civilian|civilian]] yang statenya adalah [[CivilianState#Menunggu|menunggu]]
- Occupancy: civilian task board bisa [[InteractivePropBehaviour#Occupiable|ditempati]] oleh berapa pun banyaknya [[Character#Civilian|civilian]]

#### Dinning station

Dinning station adalah facility prop yang:
[[InteractivePropBehaviour#Containable|Containable]] untuk menyimpan [[Resource#Food|food]]

- Capacity: Dinning station bisa menyimpan minimal 0 food, maksimal 100 food
  [[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Ally character|ally character]] untuk melakukan action berikut:
- [[AllyCharacterAction#Memberi makan ally character|memberi makan ally character yang lapar]]
- [[AllyCharacterAction#Makan|makan]]
  - Agar ally character bisa melakukan action makan pada dinning station tersebut, dinning station harus memiliki [[Resource#Food|food]] > 0
  - Jika food <= 0, maka dinning station tersebut tidak akan bisa dipakai untuk makan
    [[InteractivePropBehaviour#Occupiable|Occupiable]] bagi [[Character#Ally character|ally character]] untuk melakukan [[AllyCharacterAction#Makan|makan]]
- Jadi ally character yang melakukan action makan di dinning station dihitung sebagai character yang menempati prop tersebut
- Occupancy: satu dinning station hanya bisa ditempati oleh satu ally character dalam satu waktu
- Suatu dinning station hanya bisa dipilih oleh ally character untuk ditempati jika, food > 0 DAN occupancy = 0

#### Stretcher

Stretcher adalah facility prop yang:
[[InteractivePropBehaviour#Containable|Containable]] untuk menyimpan [[Resource#Medicine|medicine]]

- Capacity: Stretcher bisa menyimpan minimal 0 medicine, maksimal 100 medicine
  [[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Ally character|ally character]] untuk melakukan action berikut:
- [[AllyCharacterAction#Menyimpan medicine|menyimpan medicine]]
- [[AllyCharacterAction#Mengobati civilian|mengobati civilian]]
  [[InteractivePropBehaviour#Occupiable|Occupiable]] bagi [[Character#Civilian|civilian]] yang sedang dalam state [[CivilianState#Sakit|sakit]]
- Occupancy: satu stretcher hanya bisa ditempati oleh satu civilian dalam satu waktu
- Walaupun stretcher tersebut memiliki medicine <= 0, civilian yang dalam state [[CivilianState#Sakit|sakit]] bisa menempati stretcher tersebut jika occupantnya = 0

### Processing prop

Processing prop adalah interactive prop yang:
[[InteractivePropBehaviour#Buildable|Buildable]]
[[InteractivePropBehaviour#Productive|Productive]] menghasilkan [[Resource#Processed Resource|processed resource]]
[[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Ally character|ally character]]
[[Upgradable]]

Tipe processing prop

#### Apotechary Table

Apotechary table adalah processing prop yang:
[[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Ally character|ally character]] untuk [[InteractivePropBehaviour#Productive|Productive]] menghasilkan [[Resource#Medicine|medicine]] dari [[Resource#Plant|plant]] dan [[Resource#Fluid|fluid]]

#### Electric Stove

Electric stove adalah processing prop yang:
[[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Ally character|ally character]] untuk [[InteractivePropBehaviour#Productive|Productive]] menghasilkan [[Resource#Food|food]] dari [[Resource#Plant|plant]] dan [[Resource#Meat|meat]]

#### Machinist bench

Machinist bench adalah processing prop yang:
[[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Ally character|ally character]] untuk [[InteractivePropBehaviour#Productive|Productive]] menghasilkan [[Resource#Sparepart|sparepart]] dari[[Resource#Mechanical scrap|mechanical scrap]] dan [[Resource#Electrical scrap|electrical scrap]]

#### Woodwork bench

Woodwork bench adalah processing prop yang:
[[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Ally character|ally character]] untuk [[InteractivePropBehaviour#Productive|Productive]] menghasilkan [[Resource#Component|component]] dari [[Resource#Mechanical scrap|mechanical scrap]] dan [[Resource#Natural scrap|natural scrap]]

### Tech prop

Tech prop adalah interactive prop yang:
[[InteractivePropBehaviour#Buildable|Buildable]]
[[InteractivePropBehaviour#Containable|Containable]] [[Resource#Component|component]] dan [[Resource#Sparepart|sparepart]]
[[InteractivePropBehaviour#Upgradive|Upgradive]]
[[InteractivePropBehaviour#Actioncapable|Action-capable]] oleh [[Character#Player character|player character]]

Tipe tech prop

#### Bookcase

Bookcase adalah tech prop yang:
[[InteractivePropBehaviour#Upgradive|Upgradive]] untuk mengupgrade:

- [[TipeInteractiveProp#Facility prop|Facility prop]]
- [[TipeInteractiveProp#Processing prop|Processing prop]]
- [[TipeInteractiveProp#Defense prop|Defense prop]]
  Satu bookcase mengupgrade satu interactive prop, bukan mengupgrade lebih dari satu interactive prop atau semua tipe dari subtipe interactive prop
  Visual: secara visual bookcase memiliki bentuk yang sama untuk semua bookcase. Yang membedakan adalah warna dari bookcase. Bookcase memiliki palet warna yang sama dengan interactive prop yang dia upgrade
  [[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Player character|player character]] untuk [[PlayerCharacterAction#Mengupgrade interactive prop|mengupgrade interactive prop]]

#### Tool rack

Tool rack adalah tech prop yang:
[[InteractivePropBehaviour#Upgradive|Upgradive]] untuk mengupgrade [[Axe]]
[[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Player character|player character]] untuk [[PlayerCharacterAction#Mengupgrade equipment|mengupgrade equipment]] milik semua character yang menggunakan axe

#### Weaponry

Weaponry adalah tech prop yang:
[[InteractivePropBehaviour#Upgradive|Upgradive]] untuk mengupgrade [[Pistol]]
[[InteractivePropBehaviour#Actioncapable|Action-capable]] bagi [[Character#Player character|player character]] untuk [[PlayerCharacterAction#Mengupgrade equipment|mengupgrade equipment]] milik semua character yang menggunakan pistol

### Defense prop

Defense prop adalah interactive prop yang:
[[InteractivePropBehaviour#Buildable|Buildable]]
[[InteractivePropBehaviour#Breakable|Breakable]] oleh [[Character#Enemy character|enemy character]]
[[InteractivePropBehaviour#Repairable|Repairable]] oleh [[Character#Ally character|ally character]]
Mungkin [[InteractivePropBehaviour#Aggroable|Aggroable]] terhadap [[Character#Enemy character|enemy character]]
[[Upgradable]]

Tipe defense prop

#### Turret

Turret adalah defense prop yang:
[[InteractivePropBehaviour#Breakable|Breakable]] oleh [[Character#Enemy character|enemy character]]
[[InteractivePropBehaviour#Repairable|Repairable]] oleh [[Character#Ally character|ally character]]
[[InteractivePropBehaviour#Aggroable|Aggroable]] terhadap [[Character#Enemy character|enemy character]]

#### Fence

Fence adalah defense prop yang:
[[InteractivePropBehaviour#Breakable|Breakable]] oleh [[Character#Enemy character|enemy character]]
[[InteractivePropBehaviour#Repairable|Repairable]] oleh [[Character#Ally character|ally character]]

### Gating prop

Gating prop adalah interactive prop yang:
[[InteractivePropBehaviour#Openable|Openable]] oleh [[Character#Player character|player character]]

Tipe gating prop

#### Locked door

Locked door adalah gating prop yang openable, yang memungkinkan character untuk mengakses suatu tempat saja

#### Locked fence gate

Locked fence gate adalah gating prop yang [[InteractivePropBehaviour#Spawncapable|spawncapable]] dalam memicu spawning [[Character#Zombie robot|zombie robot]]

### Interactive prop khusus

Terdapat sejumlah interactive prop khusus yang memiliki behaviour tidak tipikal dengan interactive prop lain.

Tipe interactive prop khusus

#### Generator

Generator adalah interactive prop yang:
[[InteractivePropBehaviour#Activeable|Activeable]] oleh [[Character#Player character|player character]]
Lalu setelah statenya aktif maka generator akan menjadi [[InteractivePropBehaviour#Routeable|Routeable]] bagi [[Character#Civilian|civilian]]
[[InteractivePropBehaviour#Spawnincrementor|Spawnincrementor]]
[[InteractivePropBehaviour#Spawncapable|Spawncapable]] dalam memicu spawning [[Character#Robber|robber]]

#### Tower radio

Tower radio adalah interactive prop yang:
[[InteractivePropBehaviour#Breakable|Breakable]] oleh [[Character#Zombie robot|zombie robot]]
[[InteractivePropBehaviour#Buildable|Buildable]] oleh [[Character#Player character|player character]]
[[Upgradable]]
[[InteractivePropBehaviour#Spawnincrementor|Spawnincrementor]]
[[InteractivePropBehaviour#Spawncapable|Spawncapable]] dalam memicu spawning [[Character#Zombie robot|zombie robot]] dan [[Character#Robber|robber]]
[[InteractivePropBehaviour#Endtriggerable|Endtriggerable]]
