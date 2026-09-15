Upgrade materials adalah property tentang tipe dan kuantitas resource yang dimiliki oleh [[Upgradable]] object
Object yang [[Upgradable#Upgradable|upgradable]] memiliki property tentang apa saja resource yang diperlukan untuk mengupgrade suatu object, baik [[PlayerCharacterAction#Mengupgrade equipment|equipment]] maupun [[PlayerCharacterAction#Mengupgrade interactive prop|interactive prop]]
Karena action [[PlayerCharacterAction#Mengupgrade equipment|mengupgrade equipment]] maupun [[PlayerCharacterAction#Mengupgrade interactive prop|mengupgrade interactive prop]] tidak dilakukan dengan cara langsung berinteraksi dengan upgradable interactive prop yang bersangkutan, melainkan interaksi dengan [[InteractivePropBehaviour#Upgradive|upgradive]] interactive prop yang [[UpgradeTarget|upgrade target]]-nya adalah upgradable interactive prop tersebut, maka [[InteractivePropBehaviour#Upgradive|upgradive]] interactive prop tersebut bisa mengakses informasi tentang ini juga

### Build materials

Build materials adalah upgrade materials dari level 0 ke level 1
