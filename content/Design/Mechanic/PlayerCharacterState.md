Player character memiliki state yang tidak dimiliki character lain:

### Terang

- Character terang jika [[LightPoint|light point]] > 0
- Jika [[LightPoint|light point]] > 0, maka light point akan berkurang seiring waktu
- Kecepatan pengurangan light point adalah 5% dari total light point per detik

### Gelap

- Character gelap jika [[LightPoint|light point]] <= 0
- Jika character mengalami gelap, maka player character otomatis dipindahkan ke lokasi [[TipeInteractiveProp#Generator|Generator]] terakhir yang dia nyalakan

#### Pinalti

- Jika character mengalami gelap, maka sebagian [[Resource]] yang dimiliki [[Character#Ally character|Ally character]] akan dikurangi sebanyak 10% dari total resource yang dimiliki
- Resource yang dikurangi:
  - [[Resource#Plant|Plant]]
  - [[Resource#Meat|Meat]]
  - [[Resource#Fluid|Fluid]]

### Pingsan

- Player character akan pingsan jika [[HealthPoint|health point]] <= 0
- Jika player character mengalami pingsan, maka player character akan otomatis dipindahkan ke sebelah [[TipeInteractiveProp#Tower radio|Tower radio]]

#### Pinalti

- Jika character mengalami pingsan, maka sebagian [[Resource]] yang dimiliki [[Character#Ally character|Ally character]] akan dikurangi sebanyak 10% dari total resource yang dimiliki
- Resource yang dikurangi:
  - [[Resource#Mechanical scrap|Mechanical scrap]]
  - [[Resource#Natural scrap|Natural scrap]]
  - [[Resource#Electrical scrap|Electrical scrap]]
