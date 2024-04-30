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
Es un número de 32 bits separados en 4 octetos con una parte de red y otra de host determinados por la máscara de subred.  
Dirección de red: La del dispositivo que conecta los dispositivos.  
Dirección de host: Un dispositivo normal conectado a la red.  
Dirección de broadcast: Una dirección usada para transmitir a todos los dispositivos conectados a una red.  

### Tipos de direcciones IPv4 según el destinatario
Unicast: De un dispositivo a otro.  
Multicast: Rango de dispositivos subscritos a una ip.  
Broadcast: Todos los dispositivos de la red.  

### Direccionamiento privado
Hay direcciones públicas y privadas. Las privadas, definidas por la RFC 1918, solo se puede usar en LAN, no son enrutables globalmente.  
10.0.0.0/8  
172.16.0.0/12  
192.168.0.0/16  
El NAT permite traducir IPs privadas a públicas
Loopback 127.0.0.0/8  
APIPA 169.254.0.0/16 se ponen automaticamente si no esta configurada la ip y no se puede adquirir una.  

### Clases de direccionamiento en IPv4
Segun la RFC 790 hay 5 clases:   
Clase A (0.0.0.0/8 a 127.0.0.0/8)  
Clase B (128.0.0.0 /16 — 191.255.0.0 /16)  
Clase C (192.0.0.0 /24 — 223.255.255.0 /24)  
Clase D (224.0.0.0 a 239.0.0.0)  
Clase E (240.0.0.0 — 255.0.0.0)  
El direccionamiento de IPv4 lo llevan varias entidades: La IANA es la principal y ella le otorga permiso a otras como RIPENCC(europa, rusia, mediterraneo), AFRINIC(áfrica), LANCNIC(latinoamérica).  

### Segmentación de redes
El tráfico broadcast no viaja más allá de un router, lo que es el dominio de broadcast. También existe el dominio de colisiones, en el que los mensaje de dos dispositivos pueden colisionar al transmitir a la vez, estos dominios son entre los dispositivos conectados a un mismo switch, hub...  
Un dominio de broadcast grande puede generar tráfico excesivo y ser perjudicial para la red, por lo que se puede hacer subredes.  

### Planteamiento del problema de la división de subredes
Para dividir una red hay que robar bits a la parte de host de modo que habrá mas redes pero menos hosts por red. La primera y última direccion no se puede usar para host.  
El número de redes y de host es 2 elevado al número de bits que tenga la parte de red o de host.  

### Ejemplo de división de subredes
Ejemplos del proceso para determinar cuantos bits robar de la parte de host.  

### VLSM
VLSM(Variable Length Subnet Mask) sirve para poder dividir una subred en más subredes sin afectar a otras subredes creadas, se utilizaría una máscara de subred distinta a partir de la de la subred creada para hacer otras subredes en esa subred.  
Esto se hace debido a que al tener que hacer todas las subredes del mismo tamaño algunas terminan desperdiciando muchas direcciones host, como se vio en los ejemplos anteriores.  
Se empieza por la red que más direcciones necesita.  

### Agotamiento de direccionamiento IPv4
Las direcciones IPv4 son de 32 bits por lo que hay una posibilidad de 2^32 direcciones posibles y estas se están agotando. La IETF ha creado ya IPv6, estamos en una era de transición y para usar las dos al mismo tiempo se usan las siguientes técnicas.  
Dual stack: Soportar las dos versiones.  
Tunnerling: Encapsular los paquetes de una versión a otra.  
Translation: En la comunicación entre dos maquinas que soportan únicamente versiones distintas.  

### Estructura de una dirección IPv6
Las direcciones IPv6 son de 128 bits separados en 8 hextetos(16) separados por :. Para simplificarlas se omiten los ceros no significativos y cuando hay grupos de ceros contiguos se pone ::, solo se puede poner un ::. Aun no simplificando son válidas.  

### Tipos de direcciones
Categorías:  
Unicast: Una máquina a otra.  
Multicast: Una máquina a varias. Empiezan por FF. FF02::1 all nodes. FF02::2 all routers.  
Anycast: La tienen varias máquina que ofrecen un mismo servicio, se busca la más cercana.  
Las IPv6 tienen dos partes, prefijo de red e identificador de interfaz. Es recomendable y usual que cada parte tenga 64 bits, aunque puede cambiar.  
Tipos de direcciones:  
GUA(Global Unicast Address): Son como las IPs públicas de IPv4, enrutables globalmente. Rango 2000::/3.  
LLA(Link-Local Address): Direcciones que solo se ven dentro del mismo enlace. Rango FE80::/10.  
Menos usadas:  
Loopback: ::1/128.  
Dirección sin especificar: ::/128  
ULA(Unique Local Address): Son como las IPs privadas de IPv4. Rango FC00::/7 a FDFF::/7  
IPv4 integrada.  

### Configuración estática de direcciones GUA y LLA
Para configurar la IPv6 GUA estática en un router se usa: ipv6 address ipv6-address/prefix-length  
Para configurar la IPv6 LLA estática en un router se usa: ipv6 address ipv6-link-locall-address link-local  
Se puede poner la misma LLA en distintos enlace de un router siempre que sean únicas.  

### Configuración dinámica de direcciones GUA
Los dispositivos obtienen GUAs dinámicamente utilizando ICMPv6(Internet Control Message Protocol).  
El dispositivo manda RS(Router Solicitation) y un router responde con RA(Router Advertisement) para saber como obtener la GUA.  
La respuesta puede decir uno de estos tres métodos: SLAAC(Stateless Address Auto-configuration), SLAAC con servidor DHCPv6 stateless(no guarda la información de que asignó esa GUA), Stateful DHCPv6 (no SLAAC)(guarda la información).  
Los primeros 64 bits los da el RA mientras que los restantes son generados por el dispositivo.  
Antes de Windows Vista la parte del dispositivo se generaba mediante EUI-64 a partir de la dirección MAC, , pero ahora se hace aleatoriamente.  

### Configuración dinámica de direcciones LLA  
En windows las LLA se generan aleatoriamente. Esto se puede desactivar mediante el comando netsh interface ipv6 set global
randomizeidentifiers=disabled para que se generen mediante EUI-64  
Los routers de Cisco asignan la LLA cuando se asigna la GUA, generalmente con EUI-64.  

### Multicast en IPv6
Las direcciones multicast de IPv6 tienen el prefijo FF00::/8. Existen dos tipos: Dirección de red multicast conocida, dirección multicast de nodo solicitado.  
Red conocida: FF02::1, FF02::2.  
Un router comienza a formar parte de este grupo cuando se lo habilita como router IPv6 con el comando de configuración global ipv6 unicast-routing  
Nodo solicitado: Una dirección multicast de nodo solicitado se asigna a una dirección especial de multicast de Ethernet.  

### Subredes en IPv6
IPv6 se diseñó teniendo en cuenta las subredes. De los 64 primeros bit los 48 primeros son para direccionamiento global y los 16 restantes son el Subnet ID.

### Protocolos de capa de transporte
### Funciones de la capa de transporte
Resposabilidades: Comunicación entre aplicaciones, comunicaciones extremo a extremo, enlace entre capasa superiores e inferiores.  
Tareas: Seguimiento de conversaciones individuales, segmentación de datos y rearmado de segmentos, construcción de las cabeceras de las PDU de capa de
transporte, identificar, separar y administrar múltiples comunicaciones.  
La capa de transporte utiliza la segmentación y la multiplexación para permitir que diferentes comunicaciones se intercalen en la misma red.  
Protocolos fundamentales de la capa de transporte:  
TCP(Transmission Control Protocol): Confiabilidad, control de flujo.  
UDP(User Datagram Protocol): Baja sobrecarga, protocolo no orientado a conexión, entrega de mejor esfuerzo.  

### TCP
Características: Orientado a conexión, garantiza entrega confiable, reordenación de segmentos en destino, admite control de flujo.  
Cabecera de 20 bytes con distintas partes para tener confiabilidad.  
La mayoría de servicios y aplicaciones usan tpc debido a la confiabilidad. Ej. HTTP, SMTP, SSH, IMAP.

### UDP
Caracteristicas:  
Los datos se reconstruyen en el orden en que se recibieron.  
Los segmentos perdidos o con error no se vuelven a enviar.  
No está orientado a la conexión y no hay establecimiento de sesión.  
La cabecera es de 8 bytes para ser más ligero. Aun así tiene un checksum.  

### Números de puerto








