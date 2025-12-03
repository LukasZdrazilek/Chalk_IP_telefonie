============================ IP TELEFONIE =================================

### =>	ISDN = první integrace služeb do jedné (hlas+data)
### =>	ATM = optika, velmi kvalitní, implementace QoS, ale drahé
### =>	Nakonec nástup IP (DSL, Ethernet, Wifi, VoIP)

### =>	VoIP = technologie umožňující provozovat IP telefonii

### =>	IP telefonie = koncept telefonování přes datové sítě
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

### =>	Zpoždění

  - **očekávané** (paketizační): záleží na velikosti paketů a typu kodeků
    
  - **náhodné**: wrapping, access, node, buffer
      - Jitter = rozdíl mezi očekávaným a reálným příchodem paketu (v bufferu)
        
  - **300ms** = hranice zpoždění pro kvalitní hovor

  - **Řešení zpoždění**
    - implementace priorit (QoS)
    - limitace maxima provozních jednotek
    - rezerva prostředků

### =>	Techniky imlementace QoS
  - **VLAN a priority**
  - **MPLS**
    
  - **Integrated Services (IS)**
    - téměř dokonalé
    - složité, zatěžující zařízení
    - jde až na úroveň datových toků
      
  - **Differentiated Services (DS)**
    - rozlišuje data a hlas
    - nutná SLA (service level agreement)
      
  - **Class of Service (CoS)** + rámec Ethernetu
    - priority bitově zapsány v rámci Ethernetu (na liknové vrstvě)
  
  - **Asynchronous Transfer Mode (ATM)**
    - každých 125 mikrosekund se odesílají pakety
    - asynchroně se rezervují prostředky v paketech
    - pokud se nezaplní, přidají se prázdné bloky

### =>  Metody spolehlivosti ve VoIP
  - **Spanning tree protokol (STP)**
    - dělá z redundantně fyzicky zasmyčkované sítě logicky nezasmyčkovanou
    - postupy a designated router umět na zkoušku
    
  - **Power over Etherner (PoE)**
    - ušetříme kabely
    - méně konektorů
    - při výpadku proudu možný síťový spike při hromadném bootu zařízení
    
### => Kodeky
  - **Kodek**
    - převádí analogový signál na digitální 
  - **Waveform coders** - sbírají každých 125 mikrosekund vzorek (G.711)
  - **Vocoders** - komprimují, sbírají a zpracovávají základní parametry pro hlas (G.729)
  - **Hybrid coders**

  - **Parametry**
    - komplexita: MIPS (Million Instructions per Second)
    - voice bandwidth (bit/s)
    - packet size (payload)
    - kvalita - MOS (body 5-1 naopak jako ve škole)
    - R-factor - hodnocení dle algoritmu (body 0-100)
    - zpoždění
   
  - **Kodek G.722**
    - 50-7000 Hz (13,900 vzorkovací frekvence)
    - moderní, HD hlas, standard pro wired a wireless
    - sám přelaďuje a šetří tak šířku pásma
    - když je ticho, neposílá pakety ale pošle malý šum
