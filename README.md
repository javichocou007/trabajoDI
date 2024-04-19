# trabajoDI

## Curso 1: Fundamentos de redes
### Introduccion
Objetivo del curso: adquirir conocimientos minimos generales sobre redes

### Rol y funciones de componentes de red:
### Componentes de red
Dispositivos finales(Host): clientes y servidores  
P2P: Un host es cliente y servidor. Emule, Azureus, KazaA. Más simples y baratas, menos escalables.  
Dispositivos intermedios: Conectan dispositivos finales. Router, switch, firewall, AP(Access Point).  
AP inalámbrico: Como wifi.  
Categorias AP: autonomos, lo puedes configurar desde interfaz; basados en controlador, necesitas controlador(WLA)  
Medios de red: Cableados, inalámbricos.  

### Dispositivos de seguridad
Pueden ser tanto hardware como software. Deep defense, seguridad en muchas capas o niveles.    
Componentes enfocados a seguridad: VPN(Virtual Private Network) confidencialidad,  ASA Firewall(Algoritmo de Seguridad Sdaptable) filtrado,  
IDS(Intrusion Detection System) reactivo / IPS(Intrusion Prevencion System) proactivo,  
ESA(Email Security Appliance) / WSA(Web Security Appliance) filtrado de trafico de email y web,  
AAA(Autentificación Autorización Accounting) server.  
Firewall: Políticas de control de acceso.  
IDS/IPS: Identifican patrones de actividad maliciosa.  
Dispositivos de seguridad de contenido: ESA/WSA herramientas cisco. TALOS, TACACS.  

### Arquitecturas de topologías de red:
### Redes jerárquicas
Redes conmutadas sin bordes(Cisco Borderless Networks): Permite conectarse desde cualquier dispositivo en cualquier momento de forma segura.  
Redes jerarquizadas: Varias capas(acceso, distribución, núcleo), Modelos de dos o tres capas(tier 2 o 3).  
Tier 2 tiene las capas distribución y núcle combinadas y la tier 3 es más compleja, más dinero.  
Casos de uso: Tier 2, un edificio; tier 3, varios edificios, modelo estrella.  

### Clasificación de las redes según el tamaño
Formas de clasificar redes: area geográfica, cantidad de usuarios, cantidad de servicios, area de responsabilidad.  
Aquí las clasificaremos en función del área geográfica:(primera W siempre Wireless en los de la derecha)  
WPAN(Wireless Personal Area Network): Bluetooth ,Zigbee, RFID.  
LAN / WLAN(Local Area Network): Ethernet, Token Ring, WiFi(IEEE 802.11).  
MAN /WMAN(Metropolitan Area Network): SMDS(Switched Multi-megabit Data Service) cableado, WIMAX(Worldwide Interoperability for Microwave Access).  
WAN /WWAN: Internet, redes celulares 4G, 5G, redes satelitales.  
Internet: Conecta redes LAN, MAN y WAN; Gestionado por distintas entidades(No centralizado).  
IETF(Internet Engineering Task Force) ingeniería.  
IANA(Internet Assigned Numbers Authority) DNS.  
ICANN(Internet Corporation for Assigned Names and Numbers) DNS.  
IAB(Internet Architecture Board) Innovación.  
LAN vs WAN  
LAN: Conecta dispositivos finales, administrado por organización o individuo, elevado ancho de banda.  
WAN: Interconecta LANs, administrado por ISPs, menos ancho de banda.  

### Tipos de cableados e interfaces:
### La capa física
Conectividad: Cada dispositivo tiene una o varias NIC(Network Interface Card) para conectarse a una red, cableadas o inalámbricas con distinto rendimiento.  
Funciones: Mandar y recibir bits asi como codificación, último paso de la encapsulación.  
Estándares: Componentes físicos, codificación, señalización; entidades(EIA(Electronic Industries Alliance)/TIA(Telecommunications Industry Association), ISO(International Organization for Standardization), ITU(International Telecommunication Union), IEEE(Institute of Electrical and Electronics Engineers)).  
Codificación: Convierte bits lógicos a señales reconocibles, ejs. lan(Manchester, NRZ(NORETURN TO ZERO), 4B/5B y 8B/10B.).  
Parámetros físicos: Lantencia, rendimiento(mb/s), capacidad de transferencia útil(paquetes sin cabeceras).  

### Medios de cobre
Cables de cobre. Baratos y fácil de instalar.
Desventajas y soluciones. Atenuación, por larga distancia - longitud correcta; EMI y RFI(interferencias electromagneticas y de radiofrecuencia) - blindaje y toma de tierra; Diafonía, interferencias por cables cercanos - Trenzado de clables.  
Tipos de cables:  
Coaxial, antenas principalmente.  
De par trenzado: (TP - Twisted Pair, U - Unshielded, S - Shielded, F - Foiled) UTP, FTP, STP, SFTP, SSTP.  
Categorías de cables.  

### Cableado UTP
Estandares por EIA/TIA en concreto EIA/TIA-568, este tipo de cable con el pinout rj45 tiene 3 tipos que son directo, cruzado y de consola. El cruzado está en desuso debido a que los dispositivos detectan el tipo de cable y hacen un cruce electrónico.

### Médios de fibra
Utiliza led o laser como pulosos de luz, el costo es mayor que utp y la instalación más compleja, inmune a interferencias y menos atenuación. FO(Fibra Óptica). Más ancho de banda.  
Canal en al que se le disparan fotones y por la refracción y reflexion de la luz en el silicio sigue el camino.  
Tipos: SM(Single Mode) un laser potente, llega más lejos, se atenúa menos, MM(Multi Mode) varios caminos disparados por led con longitudes de onda distintos.  
Tipos de conectores.  

### Medios inalámbricos
Limitaciones: Área de cobertura, seguridad, interferencias, funcionamiento half-duplex en algunas WLAN que lleva a menos ancho de banda.  
Estandares de capa física: WIFI, WIMAX, etc...  

### Direccionamiento de la capa de red
### Direcciones Ipv4



