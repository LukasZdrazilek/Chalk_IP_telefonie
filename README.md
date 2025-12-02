============================ IP TELEFONIE =================================

### ⦁	ISDN = první integrace služeb do jedné (hlas+data)
### ⦁	ATM = optika, velmi kvalitní, implementace QoS, ale drahé
### ⦁	Nakonec nástup IP (DSL, Ethernet, Wifi, VoIP)

### ⦁	VoIP = technologie umožňující provozovat IP telefonii

### ⦁	IP telefonie = koncept telefonování přes datové sítě
 - žádné hybridní systémy, vše jede přes IP
 - **Gateway** = přenos mezi starými a novými technologiemi (překlad dat+sinalizace)

 - **Výhody**
   - levné (použití již vybudované infrastruktury, menší management, levné komponenty)
   - menší šířka pásma (použití komprese)
   - flexibilita (použití známých protokolů, number mobility)
   
 - **Nevýhody**
   - horší kvalita hlasu než klasika
   - zabezpečení sítě
   - spolehlivost, (99,999 % ve VoIP = 6 minut za rok) redundantní HW, linky a zálohy

### ⦁	Zpoždění
  - **očekávané** (paketizační): záleží na velikosti paketů a typu kodeků
  - **náhodné**: wrapping, access, node, buffer
      - Jitter = rozdíl mezi očekávaným a reálným příchodem paketu (v bufferu)
  - 300ms = hranice zpoždění pro kvalitní hovor

### ⦁	Řešení zpoždění
  - implementace priorit (QoS)
  - limitace maxima provozních jednotek
  - rezerva prostředků

### ⦁	Techniky imlementace QoS
  - VLAN a priority
  - MPLS
  - Integrated Services (IS)
    - téměř dokonalé
    - složité, zatěžující zařízení
    - jde až na úroveň datových toků
  - Differentiated Services (DS)
    - rozlišuje data a hlas
    - nutná SLA (service level agreement)
  - CoS (class of service) + rámec Ethernetu
