#Sarbide sareak
## Broadband forum notation:
	**Sarbide sarea:** V eta T artean
## ITU notation:
	**Sarbide sarea:** UNI eta SNI artean
	
	
## xDSL Laburpena

Kobre pareekin egindako azpiegitura bere osotasunean. DSLAM hornitzaile aldean, MODEM erabiltzaile aldean.

**Abantailak**
 - Telefonia eta internet zerbitzuak aldi berean
 - Kobre pareen banda zabalera maximora aprobetxatu
 - Hedatutako telefonia tradizionalaren azpiegitura erabili daiteke
 - Azpiegitura egoera onean egonda, abiadura "*dezenteak*"
 
**Desabantailak**
 - Puntu-puntu topologia (Telefoniarekin ezarritakoa)
 - Abiadura maximoa oso baxua (Mbps batzuk)
 - Eskalagarritasun gutxi, ekipoak bezero bakoitzeko erosi behar
 - DSL bertsioen arteko bateragarritasuna ez da beti ematen
 - Multizerbitzua: Ahotsa eta datuak soilik ematen ditu
 - DSL motaren arabera instalakuntza konplexua izan dezakete
 
## HFC Laburpena

Zuntz optikoa eta kable koaxialarekin eratutako sare hibridoak. Cable TV-rako jaiotakoa (Lehen bertsioek zuntza ez zuten sarbide sarean).

Service Flow/QoS bermatzen da MAC mailan. Mota bereko edo antzekoetako fluxuak bateratuz eta baliabideak erreserbatuz.

DOCSIS hasieratzea:
 - 1: Maila fisikoa: Maiztasunak eskaneatu eta egokiena aukeratu
 - 2: CableModem autentikazioa (Ziurtagiri digitala)
 - 3: Cable Modem-aren IP modua hasieratu (Ezarpenak TFTP bidez, IP helbidea lortu DHCP-z)
 - 4: Negoziazioa (Konfigurazio zehatzagoa, baliabideen erreserbak)

**Abantailak**
 - Zuhaitz topologia - Azpiegitura partekatzeko gaitasuna, eskalagarritasuna errazago
 - CMTS (Cable Modem Termination System) partekatu daiteke ISP aldean
 - Norantza bakarrekoak (Telebista bakarrik, hasierakoak) edo bi norantzatakoak
 - Zuntzezko garraio sarea hobeto erabilita (Abiadura altuagoak)
 - Eraztunetako topologia zuntzean (erredundantzia
 
**Desabantailak**
 - Bi norantzetarako NT gailuak behar
 - Coaxialeko atalean anplifikadoreak, splitterrak... behar. Zarata eta ohiartzunak
 - Abiadura kobreak limitatua
 - Optiko-Elektriko konbertsiorako gailuak behar
 - Erabiltzailearen aldean NT(+TFC) + Splitter instalatu behar
 - NT: Set-Top Box (CATV), CableMode
 
## Zuntz optikoa (FTTx): Laburpena

**AON** (Active Optical Networks)
 - Ptu-Ptu topologiak
 - NT: Harpidedunaren trafikoa soilik jaso
 - Segurtasun eta QoS hobeak
 - Garestiagoa
 
**PON** (Passive Optical Networks)
 - Zuntz optikoko loop-ak + Zuhaitza azken pausuetan
 - NT: Harpidedun talde baten trafikoa jaso, honek harpidedunarena filtratu eta desenkriptatuko du
 - Segurtasuna kriptografian oinarritua
 - Merkeagoa
 
**Elementu nagusiak**
OLT: Optical Line Terminator
 - Elementu aktiboa
 - Hornitzailetik-harpidedunetara doazen zuntzen hasiera
ONT: Optical Network Terminator
 - Elementu aktiboa
 - Harpidedunaren aldean zuntzen amaiera
 - Zuntzera sartzeko mekanismoak inplementatzen dituzte (Elektriko-Optiko)
 - OMCI: ONT Management and Control Interface
ODN: Optical Distribution Network
 - Elementu pasiboak
 - Zuntzak, Splitter optikoak, WDM iragazkiak
 
**GPON TRAMAK**
 - GEM tramak
 Datuen garraioa egiten duten tramak dira:
 [Payload Length, Port ID, Payload Tsype, HEC (Error Control)] + [GEM payload]
 
 - GTC tramak
 Kontrolerako eta kudeaketarako tramak. GEM trafikorik ez dagoenean GTC trama hutsak bidaltzen dira sinkronismoa mantentzeko.
  - Downstream: Denbora txanda ezberdinak trafiko ezberdinetarako. ONU bakoitzak bere txandakoa hartuko du. Txanden informazioa: Trafikoa baino lehen.
  - Upstream: Denbora txandetan egiten da ere. Txanden erreserbarako DBA (Bandwidth Report eskaera, OLT-ak Badnwidth Map-arekin erantzun)
  
**Abantailak**
 - Abiadura altuak bi norantzatan
 - Zerbitzu ezberdin ugari, guzitak batera eta kalitate onez
 - Teknologia mota ezberdin askoren lotura
 - Eskalagarritasuna
**Desabantailak**
 - Kostua: Zuntza garestia da, kostua konpentsatzeko azpiegitura partekatzen dute
 - Segurtasuna: Kriptografiaren propietateen esku geratzen da
 - OLT partekatua, banda zabalera partekatua
 
## Kablerik gabeko teknologiak

 - Finkoetarako sarbidea: Wireless Local Loop: Terminalfinkoak
 - Mugikorretarako sarbidea: Terminal mugikorretarako sarbidea
 - Luzera laburreko komunikazioak: Eremu txikietan eta terminalen artean (WiFi, Bluetooth)
 - LOS Sistemak: Maiztasun altuak, antenekin kontuz
 - NLOS Sistemak: Maiztasun baxuak, antenak ia edonola
 
 **Abantailak**
  - Hedapen merkea, azpiegitura berririk ez erabiltzaile berrietarako
  - Hedapena leku urrun eta zailetara
  - Enpresentzako sare pribatuak sortzeko gaitasuna, azpiegitura dedikatu gutxirekin
  - Topologia ugari onartu
 
 **Desabantailak**
  - Garestia
  - RF banden lizentzien beharra
  - Sistemaren arabera LOS ezarri behar
  - Interferentzia ugari
