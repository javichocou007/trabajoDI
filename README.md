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
Utilidad: Multiples conversaciones simultaneas.  
Socket: Es la combinación de IP y puerto origen e IP y puerto destino. Permite diferenciar procesos en una máquina y conexiones en un servidor.  
Rangos de puertos:  
Puertos bien conocidos: 0 - 1023. Para servicios y protocolos bien conocidos.  
Puertos registrados: 1024 - 49151. Puertos registrados en la IANA por empresas.  
Puertos privados y/o Dinámicos: del 49,152 al 65,535. El resto de puertos libres para uso privado.  
El comando netstat permite ver las conexiones actuales de TCP y UDP.  

### Sesiones TCP
En un servidor cada proceso ocupa un número de puerto ,no puede haber un puerto con dos servicios
Establecimiento de una conexión tcp:  
Una máquina manda a otra una solicitud SYN.  
La otra máquina manda una respuesta ACK y manda un SYN.  
La primera máquina manda una respuesta ACK.  
Para finalizar es lo mismo pero con una solicitud FIN.  
Esto se conoce como protocolo three way handshake.  
Los mensajes mandados TCP pueden ser: URG, ACK, PSH, RST, SYN, FIN.  

### Confiabilidad y control de flujo
TCP garantiza la entrega ordenada de los segmentos.  
TCP garantiza que ante una pérdida de datos estos serán retransmitidos.  
TCP proporciona herramientas de control de flujo para no mandar datos más rápido de lo que la otra máquina puede aguantar.  
MSS(Maximum Segment Size) en IPv4 suele ser 1460.  

### Comunicación UDP
UDP no establece conexión, tiene poca sobrecarga por el tamaño del encabezado, no reordena los paquetes recibidos.  

### Principios de la redes inalámbricas
### Tecnologías inalámbricas
Bluetooth: Estándar IEEE 802.15.1 WPAN utilizado para emparejar dispositivos a una distancia de hasta 100m.  
WiMAX: Proporciona enlaces alternativos a internet. Estándar IEEE 802.16 WMAN para distancias de hasta 50km.  
Banda ancha celular: 4G, 5G.  
Banda ancha satelital: Antena parabólica direccional.  
WLAN: 2.4 GHz (UHF) - 802.11 b/g/n/ax, 5 GHz (SHF) – 802.11 a/n/ac/ax.  

### Componentes de una WLAN
NICs inalámbricas.  
Routers de hogar inalámbricos.  
AP autonomo, AP basado en controlador o LAP. Los LAP usan LWAPP para comunicarse con un WLC. Un WLC sirve para configurar automáticamente los AP.  
Antenas: Omnidireccionales, direccionales, MIMO.  

### Funcionamiento de una WLAN
Topologías:  
Modo ad hoc: Dispositivo a dispositivo. IBSS.  
Modo infraestructura: Conexión a AP. BSS o ESS.  
Tethering: Un dispositivo comparte conexión haciendo de AP.  
Las WLAN son half-duplex y no pueden mandar y recibir a la vez por lo que no pueden detectar colisiones. Por esta razón se utiliza CSMA/CA.  

### CAPWAP
CAPWAP es el protocolo que utilizan los WLC para administrar varios AP, está basado en LWAPP y se cifra con DLTS.  
Los tuneles CAPWAP son las conexiones del WLC a los AP.  

### Gestión de canales
DSSS - Direct-Sequence Spread Spectrum.  
FHSS - Frequency-Hopping Spread Spectrum.  
OFDM - Orthogonal Frequency-Division Multiplexing.  
Sección de canales 2,4GHz:
La banda de 2,4 GHz se subdivide en múltiples canales, cada uno de los cuales tiene un ancho de banda de 22 MHz y se separa del siguiente canal en 5 MHz.  
Cuando se necesitan múltiples APs 802.11b/g en la misma zona se recomienda utilizar canales no superpuestos, como los números 1, 6 y 11.  
Sección de canales 5 GH:  
En los estándares de 5 GHz 802.11a/n/ac, hay 24 canales.  
Cada canal está separado del siguiente canal por 20MHz.  
Los canales no superpuestos son 36, 48 y 60 en el caso de canales de 20MHz.  

### Seguridad en las WLANs
Técnicas de seguridad básicas pero efectivas: Ocultación de SSID, filtrado de direcciones MAC.  
Autenticación abierta: No se requiere contraseña.  
Autenticación de clave compartida: WEP, WPA, WPA2 y WPA3.  

### Principios de virtualización
### Computación en la nube
La computación en la nube resuelve algunos problemas administrativos: Elimina o reduce equipos de TI, reduce el costo de equipamiento, energía y refrigeración.  
Servicios principales:   
Software como un Servicio (SaaS): Office 365, Wordpress.  
Plataforma como un Servicio (PaaS): Google App Engine.  
Infraestructura como un Servicio (IaaS): Azure, AWS.  
Tipos de nubes: públicas, privadas, híbridas, comunitarias.  
Centro de datos: Procesamiento y almacenamiento de datos.  
Computación en la nube: recursos de computación compartidos.  

### Vitualización
Con la virtualización en vez de tener un servidor para cada función, un servidor puede tener varios OSs. Con esto se evita tener un unto único de fallo, tener muchos servidores y malgastar recursos.  
El Hypervisor proporciona una capa de abstracción frente al hardware físico real y permiten tener varias instancias de OSs.  

### Hypervisores
Tipos: Tipo 1(Bare-metal), tipo 2(Hypervisor alojado).  
Las de tipo 1 se instalan directamente en el hardware, son más eficientes, necesita una consola de administración.  
Los de tipo 2 son programas como: VirtualBOX, VMWare Professional, VirtualPC, VMWare Fusion.  

### Virtualización de servicios de red
En una arquitectura virtualizada las VMs son trasladables y se usan switches virtualizados para simplificar el trabajo.  
Hay dos tipos de flujo en  una arquitectura virtualizada: Tráfico Este-Oeste, Tráfico Norte-Sur.  
Mediante técnicas de virtualización se puede implementar: Subinterfaces, Interfaces virtuales, VLAN, VRFs.  

### Conceptos de conmutación
### Estructura de una trama ethernet
Ethernet está definido en dos estándares de la IEEE:  
IEEE 802.2: implementa la subcapa LLC.  
IEEE 802.3: Implementa la subcapa MAC y la capa física.  
La subcapa MAC es responsable de: encapsulamiento de datos, trama de Ethernet, direccionamiento Ethernet, detección de errores Ethernet, acceso a los medios.  

### Direccionamiento MAC
Una dirección MAC tiene 48 bits o 12 dígitos hexadecimales, los 24 primeros son el OUI(Organizationally unique identifier), los 24 restantes los asigna el fabricante.  
Una dirección MAC tiene que ser única de una NIC.  
Tipos de direcciones MAC: unidifusión, multidifusión, difusión.  
Las de unidifusión se usan como unicast y para ARP(Address Resolution Protocol) y ND(Neighbor Discovery).  
Las de difusión se mandan a todos los dispositivo de una LAN, la dirección es FF:FF:FF:FF:FF:FF.  
Las de difusión se mandan a los dispositivos que pertenecen a un grupo de multidifusión.  

### Tabla MAC de un switch
Los switches tienen tablas de direccionamiento en las que guardan las direcciones MAC conectadas a cada puerto.  
Si una dirección MAC no está en la tabla se hace una busqueda y se añade. Las direcciones se van eliminando de la tabla con el tiempo.  

### Conmutación en un switch
Métodos de conmutación: almacenamiento y reenvío, de corte(avance rápido o sin fragmentos).  
Configuración de duplex:  
Full-duplex: La información puede mandarse y recibirse al mismo tiempo.  
Semiduplex: La información solo puede mandarse o recibirse en un instante.  
Autonegociación: Los dos dispositivos negocian la mejor opción.  
AUTO-MDIX(Medium Dependent Interface): Sirve para poder usar cables de par trenzado directos o cruzados indiscriminadamente.  


## Curso 2: Prácticas de Fundamentos de redes
### Introducción
Poner en práctica los conocimientos del curso anterior.  

### Práctica 1: Conectividad de la capa física
Usando el programa Packet Tracer:  
Identificar las características físicas de cada dispositivo de interconexión de redes.  
Seleccionar los módulos correctos para proporcionar conectividad.  
Conectar los dispositivos.  
Probar la conectividad entre los dispositivos.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/9486c6f1-01dc-4747-88b4-394c3159439f)

### Práctica 2: Subredes con IPv4
Con Packet Tracer:  
Diseñar un esquema de subredes IPv4.  
Configurar los dispositivos de acuerdo a las subredes generadas.  
Probar la conectividad en la red y solucionar los problemas encontrados.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/499a0a2e-6d8c-4c24-a2bf-28d2e015251d)

### Práctica 3: Diseño de subredes con VLSM
Con Packet Tracer:  
Realizar la división en subredes acorde a las especificaciones de número de redes y tamaño de cada red.  
Asignar direcciones a los equipos de cada subred.  
Probar la conectividad.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/7ccdce4d-bedc-4b1e-b273-6e29474e967b)

### Práctica 4: Diseño de subredes en papel
Teniendo las especificaciones de la red, en un archivo de texto:  
Calcular el esquema de direccionamiento más óptimo.  
Calcular las direcciones de red, broadcast y rango de direcciones útiles para cada subred.  
Dada una dirección calcular a qué subred pertenece y la dirección de red y broadcast de dicha subred.  

### Práctica 5: Subredes con IPv6
En Packet Tracer:  
Determine las subredes y el esquema de direccionamiento IPv6.  
Configure el direccionamiento IPv6 en los outers y los Hosts.  
Verificar la conectividad IPv6.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/647f83f5-38fd-4215-9f07-9fde872909b8)

### Práctica 6: Comunicaciones de capa de transporte
En Packet Tracer:  
Generar tráfico de red utilizando el modo simulación.  
Examinar el funcionamiento de los protocolos TCP y UDP.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/022c740e-ef44-47a6-85eb-93d317f89a99)


## Curso 3: Acceso a la red
### Introducción
Aspectos relacionados con VLANs, switches y capa 2.  

### Configurar y verificar VLANs
### ¿Qué es una VLAN?
Son segmentaciones lógicas en redes físicas de forma que no hacen falta varios dispositivos y conectan distintos dispositivos de la VLAN. Mejor organización y tráfico.  
Tipos de VLAN: VLAN de datos, VLAN nativa, VLAN de administración, VLAN de voz.  
Es necesario tener una VLAN separada para voz porque se necesita: retraso inferior a 150ms prioridad, (QoS)Quality of Service, ancho de banda, congestionamiento.  
Los switches de cisco tienen una VLAN creada de forma predeterminada, la VLAN1. Hay que tener cuidad al configurar las VLANs en el switch.   

### VLANs en entornor conmutados múltiples
Un enlace de trocal es un enlace entre dos dispositivos de una red que permite el trafico de VLANs.  
Para diferenciar el trafico de VLAN se añade a la trama un encabezado IEEE 802.1Q.  
Se debe configurar los dispositivos de forma que un enlace de troncal conecte la misma VLAN.  

### Configuración de VLANs
Comandos para crear una VLAN:  
vlan vlan-id  
name vlan-name  
end  
Una vez creada se asigna a una interfaz del switch. Comandos para asignar al puerto:  
interface interface-id  
switchport mode access  
switchport access vlan vlan-id  
end  
Para verificar la creación:  
show vlan [brief | id vlan-id | name vlan-name | summary]  
show interface vlan vlan_id  
Cambiar perteneciencia a un puerto:  
switchport access vlan vlan-id  
no switchport access vlan  

### Enlaces troncales
Comandos para configurar un enlace troncal:  
interface interface-id  
switchport mode trunk  
switchport trunk native vlan vlan-id  
switchport trunk allowed vlan vlan-list  
end  
Para verificar: show interfaces interface_id switchport  
Para restablecer enlace de troncal a modo predeterminado:  
no switchport trunk allowed vlan  
no switchport trunk native vlan  
Para restablecer a puerto de acceso: switchport mode access  

### Protocolo DTP
DTP(Dynamic Trunking Protocol) es un protocolo propietario de cisco que automatiza ciertas tareas de las VLAN en los switches cisco y determina si se usa un enlace troncal o de acceso.  
Esta activado por defecto, el valor predeterminado es dynamic-auto, puede desactivarse con switchport nonegotiate y activarse con switchport mode dynamic auto.  
Se configura con el comando switchport mode y uno de los siguientes modos: acceso, dinámico automático, dinámico deseable, troncal.  
Verificación: show dtp interface  

### Configurar y verificar conectividad entre switches
### Concepto del enrutamiento entre VLANs
Opciones de enrutamiento:  
Enrutamiento entre VLAN heredado: Un router con varias interfaces conecta cada puerto con el switch de una VLAN.  
Router-on-a-stick: Se crean subinterfaces en un router mediante la configuración. Es poco eficiente, raramente se usa.  
Uso de switches de capa 3 (MLS) con interfaces virtuales conmutadas (SVIs): Se crea una interfaz SVI para cada VLAN del switch.  

### Enrutamiento entre VLANs mediante 'Router on a stick'
Proceso de creación:  
Crear y nombrar las VLANs.  
Crear la interfaz de administración.  
Configurar puertos de acceso.  
Configurar puertos de enlace troncal.  
Para verificar se revisca con ICMP y los comandos:
show ip route  
show ip interface brief  
show interfaces  
show interfaces trunk  

### Enrutamiendo entre VLANs mediante 'MLS'
Hace falta un conmutador de capa 3, así se hace conmutación en hardware para mayor velocidad.  
Para la configuración:  
Crear las VLAN.  
Crear las interfaces VLAN SVI.  
Configurar los puertos de acceso.  
Habilitar el enrutamiento IP.  
Verificación:  
show ip route  
show ip interface brief  
show interfaces  
show interfaces trunk  

### Resolución de problemas de enrutamiento entre VLANs
Falta alguna VLAN: show interface interface-id switchport.  
Problemas con el puerto troncal del switch: show interface trunk y show running-config interface interface_id.  
Problemas en los puertos de acceso de switch: show vlan brief, show interface interface_id switchport o show running-config interface interface_id.  
Configuración incorrecta en el router: show ip interface brief y show interfaces.  

### Configurar y verificar protocolos de descubrimiento de capa 2
### CDP como protocolo de descubrimiento de capa 2
CDP(Cisco Discovery Protocol) es un protocolo propietario de cisco de capa 2 usado para recopilar información de los dispositivos del mismo enlace. Se ejecuta en todos los dispositivos cisco. Es un LLDP(Link Layer Discovery Protocol) de capa 2.  
Está habilitado de forma predeterminada. Para ver la información se usa show cdp. Para desactivarlo se usa no cdp enable, por motivos de seguridad se puede desactivar para no dar información a un atacante, además que un técnico ya sabría la topología de la red, el comando para ver la topología y diseño es show cdp neighbors.  

### LLDP como protocolo de descubrimiento de capa 2
Es como CDP pero no hace falta usar dispositivos cisco. Puede o no estar habilitado. Para habilitar globalmente lldp run. Para verificar show lldp. Para usarlo show lldp neighbors.  

### Configurar y verificar Etherchannel
### Conceptos generales de Etherchannel
Para aumentar el ancho de banda se pueden proporcionar varios enlaces. Para esto hace falta un protocolo que lo permita debido al STP(Spanning Tree Protocol) que bloquea bucles de conmutación.  
Para esto se usa Etherchannel.  

### PAGP y LACP
PAGP(Port Aggregation Protocol) sirve para crear enlaces Etherchannel. Modos: encendido, desirable, auto. Dependiendo de los dos dispositivos se establece enlace o no.  
LACP(Link Aggregation Control Protocol) agrupa varios puertos físicos para hacer uno solo lógico. Modos: encendido, activo, pasivo. Dependiendo de los dos dispositivos se establece el canal o no.  

### Configuración de Etherchannel
Cosas a tener en cuenta:  
Soporte de EtherChannel.  
Velocidad y duplex.  
Coincidencia de VLANs.  
Rango de VLANs.  

### Resolución de problemas de Etherchannel
Comandos para verificar:  
show interfaces port-channel  
show etherchannel summary  
show etherchannel port-channel  
show interfaces etherchannel  
Problemas típicos:  
Los puertos no son de la misma VLAN y no hay enlace troncal.  
Conexión troncal no configurada en todos los puertos.  
El rango permitido de VLAN no es el mismo.  
Opción de negociación dinámica es incompatible.  

### El protocolo STP y sus variantes
### Funciones de STP
El protocolo STP previene los bucles que proporcionan redundancia. Si STP no está habilitado se pueden formar bucles de capa 2 que haga que las tramas se progragen infinitamente en bucle por la red.  
Broadcast storm: Número anormalmente alto de tráfico broadcast que saturan la red.  

### Algoritmo STP
Crea una topología sin bucles y todos switch determinan una única ruta de menor costo.  
Método:  
Selección de un puente raíz.  
Bloquear de rutas redundantes.  
Creación de una una topología sin bucles mediante el bloqueo de puertos específicos.  
Vuelta a calcular en caso de falla de enlace.  

### Elección del puente raiz
Durante STP los switches utilizan BPDU(Bridge Protocol Data Units) para compartir su información.  
Así se determina el mejor puente raiz y rutas. El costo está definido por la IEEE.  

### Puertos raíz, designados y alternativos
Cada switch escogerá entonces un puerto raíz, el cual es el más cercano al enlace raíz.  
Entre dos switch habrá un puerto designado que tiene el costo de ruta raíz interna para el puente raíz.  
Si un puerto no es un puerto raíz o un puerto designado, se convierte en un puerto alternativo.  
Podemos ahora identificar puertos raíz, designados y alternativos.  

### Elegir un puerto raíz a partir de multiples rutas de igual costo
Criterios:  
Oferta de remitente más baja.  
Prioridad de puerto del remitente más baja.  
ID de puerto del remitente más bajo.  

### Temporizadores y estados de puerto
STP utiliza tres temporizadores:  
Temporizador de Hello.  
Temporizador de demora directa (Forward delay).  
Temporizador de edad máxima (Max Age).  

### Evolución de STP
Historia y novedades de STP.  

### PortFast y BPDUGuard
Cuando un dispositivo se conecta a un switch se espera cada vez que expira el temporizador de retardo de reenvío 15 segundos durante 30 segundos.  
Si el puerto esta configurado en PortFast se evita el retraso.  
Los switches de cisco mediante BPDUGuard pueden poner el switch en estado errdisabled al recibir BPDU para protegerse ante bucles. Aunque el administrador tiene que volver a poner manualmente la interfaz de servicio.  

### Arquitecturas inalámbricas de cisco
### Conceptos generales de tecnologías inalámbricas
Redes inalámbricas: WPAN, WLAN, WMAN, WWAN.  
Tecnologías inalámbricas: bluetooth, WIMAX, banda ancha celular, banda ancha satelital.  
Estandares varios de 802.11.  
Organizaciones: ITU(International Telecommunication Union), IEEE, Alianza Wifi.  

### Componentes de las WLAN
NIC inalámbrica, router inalámbrico, AP inalámbrico(autónomos, basados en controlador), antenas(Omnidireccional, direccional, MIMO).  

### Funcionamiento de las WLAN
Topologías: modo ad hoc, modo de infraestructura(BSS, ESS), tethering.  
Asociación: descubrir un AP inalámbrico, autenticarse con un AP, asociarse con el AP.  
Parametros de asociación: SSID, contraseña, modo de red, modo de seguridad, configuraciones de canal.  
Algoritmo CSMA/CA

### Administración de APs
CAPWAP permite configurar varios APs medianten un WLC. Usando IPv4 usa el protocolo IP 17 y usando IPv6 usa el protocolo IP 136.
DTLS es el protocolo de cifrado entre el AP y el WLC.  
FlexConnect permite la configuración y el control de APs a través de un enlace WAN.  

### Gestión de canales WLAN
La saturación de canales de radiofrecuencia se puede mitigar con las técnicas DSSS, FHSS, OFDM.  
Los canales de banda de 2,4GHz tienen 22MHz mientras que los de 5GHz tienen 20MHz de separacion

### Configuración de WLAN de ubicación remota
En oficinas pequeñas y hogar normalmente se usan routers SOHO que son como una mezcla de router switch y AP inalámbrico.
Configuración:  
Configurar el router desde el navegador web.  
Configurar más aspectos de la red.  
Si hace falta configurar una red de malla para aumentar el alacance.  
Configurar el NAT.  
Configurar QoS.  
Configurar el reenvio de puertos.  

### Configuración básica en WLC
Los puntos de acceso ligeros(LAP) no requieren configuración inicial y se usan para comunicarse con el WLC. Es parecido a conectarse a un router mediante el navegador web. Desde ahí hay varias opciones especificas para configurar los APs.  


## Curso 4: Prácticas de acceso a la red
### Intruducción
Poner en práctica los conocimientos del curso anterior.

### Práctica 1: Implementación de VLANs con Trunking
Configurar las VLAN.  
Asignar las VLAN a los puertos.  
Configurar troncales estáticos.  
Configurar enlace troncal dinámico.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/62ed79c4-566b-4379-a432-8147ec346f5f)

### Práctica 2: Enrutamiento entre VLANs con Router on a Stick
Agregar VLAN a un switch.  
Configurar subinterfaces.  
Probar la conectividad con entre VLANS.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/3f14d627-6ca4-44e4-aef5-9fc0b95bba97)

### Práctica 3: Enrutamiento entre VLANs con MLS
Configurar el switching de capa 3.  
Configurar el routing entre redes VLAN.  
Configurar el enrutamiento IPv6 entre VLAN.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/f4f910cf-1ecf-4deb-99be-b153b8034d54)

### Práctica 4: Reconocimiento de red con CDP
Obtener la topología de una red usando CDP y acceso remoto SSH
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/84e9389d-f5ef-4600-a4ae-e48e076a604d)

### Práctica 5: Implementación de Etherchannel
Configurar los parámetros básicos del switch.  
Configurar un EtherChannel con PAgP de Cisco.  
Configurar un EtherChannel LACP 802.3ad.  
Configurar un enlace EtherChannel redundante.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/61fefab3-f084-4e95-be22-b96ce889b7c6)

### Práctica 6: Verificación de funcionamiento de STP
Describir el protocolo del árbol de expansión rápida (STP).  
Explique cómo el protocolo de árbol de expansión evita los bucles de conmutación al tiempo que permite la redundancia en las redes conmutadas.  

### Práctica 7: Configuración de una red inalámbrica
Conectar a un router inalámbrico.  
Configurar el router inalámbrico.  
Conectar un dispositivo cableado al router inalámbrico.  
Conectar un dispositivo inalámbrico al router inalámbrico.  
Agregar un AP a la red para ampliar la cobertura inalámbrica.  
Actualizar la configuración predeterminada del router.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/2e6464fe-a9ca-40d4-878a-cf8f40325810)

### Práctica 8: Configuración de una WLAN básica con WLC
En este laboratorio estudiaremos algunas de las características de un controlador de la red Inalámbrica.  
Crearemos una nueva WLAN en el controlador e implementaremos ciertos aspectos de seguridad en esa LAN.  
Configuraremos un host inalámbrico para conectarse a la nueva.  
WLAN a través de un AP que esté bajo el control del WLC.  
Por último, verificaremos que exista conectividad.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/f0e06fde-63c7-4e43-ba83-4b782c5a19f9)


## Curso 5: Conectividad IP
### Introducción
Routers y enrutamiento.  

### Interpretar los componentes de la tabla de enrutamiento
### Función de un router
Un router tiene dos funciones: Enrutar, cuando recibe un paquete IP, determinar que interfaz usar para reenviar. Conmutar, reenviar el paquete a otra red para que llegue a su destino.  
Un router encuentra la mejor ruta por medio de la tabla de enrutamiento.  

### Determinación de la mejor ruta
La mejor ruta de la tabla de enrutamiento también se conoce como la coincidencia más larga. En las tablas de enrutamiento hay guardadas direcciones de red y una logitud del prefijo. Para encontrar la mejor ruta se busca que coincidan el mayor número de bits de entre las direcciones de red y la dirección destino del paquete.  

### Genereación de la tabla de rutas
Orígenes de la direcciones de red:  
Redes conectadas directamente: Se agregan cuando una interfaz local está configurada con una dirección IP.  
Redes remotas: Rutas estáticas o protocolos de enrutamiento dinámico(RIP, IGRP, EIGRP u OSPF).  
Rutas predeterminadas. Se usa cuando no tiene la dirección, puede ser una estática o dinámica.  

### Mecanismo de reenvío de paquetes en un router
Al reenviar paquetes, un router debe encapsularlos en el tipo de trama adecuado para el enlace de datos de salida de manera eficiente.  
Existen tres mecanismos:   
Switching de procesos: Antiguo. La CPU hace coincidir la dirección de destino con una entrada de la tabla de enrutamiento para determinar la salida.  
Switching rápido: Usa una memoria caché para almacenar la información de siguiente salto.  
CEF(Cisco Express Forwarding): CEF crea una Base de Información de Reenvío (FIB) y una tabla de adyacencias, la tabla se actualiza solo cuando cambia la estructura de la red, no al recibir paquetes como en los otros.  

### Estructura de la tabla de direccionamiento IPv4
Las rutas de la tabla tienen estos códigos:  
L: Dirección asignada a la interfaz del router.  
C: Red conectada directamente.  
S: Ruta estática.  
O, D, B...: Red que se descubre de forma dinámica de otro router con el protocolo de routing OSPF(Open Shortest Path First).  
Cada entrada de la tabla tiene: origen de ruta, red de destino, distancia administrativa, métrica, siguiente salto, marca horaria, interfaz de salida.  
Aunque obsoleto, se usa la arquitectura de direccionamiento por clase, hay entradas principales y secundarias.  

### Estructura de la tabla de direccionamiento IPv6
Comparte con la de IPv los origenes y fuentes de datos.  
Cada entrada de la tabla tiene: origen de ruta, red de destino, distancia administrativa, métrica, siguiente salto, interfaz de salida.  
No usa arquitectura de clases.  

### Distancia administrativa
Una entrada de una ruta puede venir de dos origenes distintos. En este caso, que ruta se escoge.  
En el IOS de cisco cada ruta tiene un valor de AD(Administrative Distance) que a menor valor mayor confianza.  

### Enrutamiento estático vs Enrutamiento dinámico
La mayoría de las redes utilizan una combinación de protocolos de enrutamiento dinámico y rutas estáticas.  
Estático: Ruta predeterminada del ISP, rutas no aprendidas por el protocolo dinamico, cosas del admin, redes internas.  
Dinámico: Redes escalables, escalabilidad.  
El enrutamiento estático es más eficiente pero requiere trabajo configurarlo por lo que se usa para tareas simples y redes simples.  

### Protocolos de enrutamiento dinámico
Un protocolo de enrutamiento sirve para llenar la tabla de enrutamiento.  
Objetivos del enrutamiento dinámico: Redes remotas, mantener información actualizada, mejor ruta, alternativas.  
Componentes: estructuras de datos, mensajes del protocolo de enrutamiento, algoritmo de enrutamiento.  

### Métricas de algunos protocolos de enrutamiento dinámico
La métrica es un valor que se usa para medir la distancia.  
RIP(Routing Information Protocol): Recuento de saltos a lo largo de la ruta.  
OSPF(Open Shortest Path First): Ancho de banda acumulado.  
EIGRP(Enhanced Interior Gateway Routing Protocol): Ancho de banda y retraso.  

### Configurar y verificar el enrutamiento estático IPv4 e IPv6
### Tipos de rutas estáticas
Tipos: estándar, predeterminada, flotante, resumida.  
Dependiendo del destino al que enviemos el paquete se denomina una de estas rutas: de siguiente salto, estática conectada directamente, estática totalmente especificada.  
Comando para configurar IPv4 estática: ip route network-address subnet-mask { ip-address | exit-intf [ip-address]} [distance]  
Y para IPv6: ipv6 route ipv6-prefix/prefix-length { ipv6-address | exit-intf [ ipv6-address]} [ distance]  

### Configuración de rutas estáticas
Cuando configuramos rutas estáticas en un router básicamente le indicamos como llegar a ciertas redes. Hay varias formas de hacerlo:  
Configurar la ruta estática de siguiente salto IPv4/IPv6: Especificamos la IP del siguiente salto para llegar a una red determinada.  
Configurar de ruta estática conectada directamente IPv4/IPv6: Especificamos la interfaz de salida para llegar a una red conectada directamente.  
Configurar de ruta estática totalmente especificada IPv4/IPv6: Especificamos tanto la interfaz de salida como la IP del siguiente salto
Para verificar: show ip route o show ipv6 route  

### Configuración de rutas predeterminadas
Una ruta predeterminada es una ruta estática que coincide con todos los paquetes por si no se encuentra la red.  
Comando de ruta estática predeterminada IPv4: ip route 0.0.0.0 0.0.0.0 {ip-address | exit-intf}  
De IPv6: ipv6 route ::/0 {ipv6-address | exit-intf}  
Para verificar usar el comando show ip route static y ver que sea 0 la máscara y buscar el * en IPv4.  

### Configuración de rutas flotantes
Las rutas estáticas flotantes proporcionan una ruta de respaldo a una ruta principal si falla el enlace.  
Las rutas flotantes tienen que tener más AD que las rutas principales y las rutas estáticas tienen de AD predeterminado 1, pero se puede cambiar.  
Para verificar: show ip route static  

### Configuración de rutas de host
Una ruta de host es una dirección IPv4 con una máscara de 32 bits o una dirección IPv6 con una máscara de 128 bits.  
Se instala una automaticamente al configurar una dirección de interfaz.  

### Cómo un router con rutas estáticas reenvía paquetes
Se explica un ejemplo de reenvío de paquetes en una topología.  

### Configurar y verficar OSPF monoárea
### Características de OSPF
OSPF(Open Shortest Path First) es un protocolo de enrutamiento dinámico de estado de enlace. Sus ventajas son velocidad y escalabilidad. No usa clases si no áreas.  
Mediante este protocolo los routers se mandan este tipo de paquetes: de saludo, de descripción de la base de datos, de solicitud de estado de enlace, de actualización de estado de enlace, de acuse de recibo de estado de enlace.  
Estos paquetes actualizan tres bases de datos: de adyacencia(vecinos), de enlace(topología), de reenvío(enrutamiento).  
Mediante el algoritmo STP se crea la tabla de topología en forma de árbol para calcular rutas.  
En OSPF un área es un conjunto de routers que comparten LSDB.  
OSPF monoárea: Solo tiene un área denominada área 0.  
OSPF multiárea: Se implementa de forma jerárquica, todas las áreas se conectan al área 0. Los routers que conectan areas se denominan ABR(routers fronterizos de área).  

### El router ID
OSPFv2 se habilita con el comando: global router ospf process-id  
Router ID es un valor de 32 bits y se utiliza para identificar de forma única un router en un dominio OSPF. Se puede establecer manual(router-id rid) o automático. Aparece en los paquetes OSPF. El router escoge su IPv4 más alta.  

### Redes OSPF punto a punto
Para configurar los interfaces p2p: network network-address wildcard-mask area area-id  
La máscara wildcard mask suele ser la inversa de la máscara de subred configurada en un interfaz. Restar a 255.255.255.255 la mascara.  
Se puede hacer configurando directamente la interfaz: ip ospf process—id area—id  

### Redes OSPF multiacceso (Elección de DR BDR)
En las redes OSPF multiacceso se escoge un DR(Designated Router) que controla los LSA y un BDR(Backup Designated Router) por si falla el DR, el resto de routers son DROTHER.  
Para ver las funciones de cada router: show ip ospf interface
Para ver las relaciones entre los otros routers: show ip ospf neighbor (posibilidades: FULL/DROTHER, FULL/DR, FULL/BDR, 2-WAY/DROTHER)  
El router con la prioridad de interfaz más alta es el DR y el segundo el BDR. Si las prioridades son iguales se escoge el que tenga la ID más alta.  
Para controlar la prioridad: ip ospf priority value  

### Configuración detallada de OSPF
En OSPF se usa el costo como métrica. Costo = ancho de banda de referencia / ancho de banda de la interfaz en bps. Ancho de banda predeterminado $10^8$.  
Cambiar el ancho de banda predeterminado: auto-cost reference-bandwidth  
Establecer manualmente el costo: ip ospf cost  
Para ver el coste: show ip route  
Intervalo Hello: Los paquetes Hello se transmiten a la dirección multicast 224.0.0.5 (todos los routers OSPF) cada 10 segundos.
Intervalo Dead: es el período que el router espera para recibir un paquete Hello antes de declarar al vecino como inactivo. Cisco utiliza un intervalo predeterminado de cuatro veces el intervalo Hello.
Los intervalos se pueden configurar pero deben coincidir.  
Comandos para intervalos:  
ip ospf hello-interval segundos  
ip ospf dead-interval segundos  
Para verificar adyacencias: show ip ospf neighbor  

### Verificación de funcionamiento de OSPF
show ip interface brief  
show ip route  
show ip ospf neighbor  
show ip protocols  
show ip ospf  
show ip ospf interface  
show ip ospf neighbor
Si no se establecen adyacencias comprobar: Máscara de subred, intervalos, tipos de redes, comando network.  
show ip protocols  
show ip ospf  
show ip ospf interface  
show ip ospf interface brief  

### Protocolos de redundancia de la puerta de enlace
### Conceptos de FHRP
FHRP(First-hop redundancy protocol) es un protocolo que proporciona puertas de enlace predeterminadas alternativas en redes conmutadas donde dos o más routers que están conectados a las mismas.  
Esto es necesario para cuando falle la interfaz del router gateway predeterminado.  
Para que el gateway no sea el único punto de fallo se implementa un router virtual.  

### El protocolo HSRP
HSRP(Hot Standby Router Protocol) es un protocolo propietario de cisco que permite evitar la pérdida de acceso externo a la red si falla el router predeterminado.  
HSRP configura un grupo de routers seleccionando uno de ellos como dispositivo activo y otros como dispositivos de reserva.  
Se escoge como activo el que tenga la prioridad más alta, en caso de ser iguales el que tenga la IPv4 más alta. Para configurar la prioridad , 0-255, se usa standby priority priority_number.  
Para forzar un nuevo proceso de elección: standby preempt  
Estados: inicial, aprender, escuchar, hablar, en espera.  

## Curso 6: Prácticas de conectividad IP
### Introducción
Poner en práctica los conocimientos del curso anterior.  

### Práctica 1: Conectividad IP entre dispositivos
Parte 1:  
Asignar direcciones IPv4 e IPv6 estáticas a las interfaces de los hosts.  
Configurar parámetros básicos del router.  
Configurar el router para el acceso por SSH.  
Verificar conectividad de red.  
Parte 2:  
Recuperar información del hardware y del software del router.  
Interpretar el resultado de la configuración de inicio.  
Interpretar el resultado de la tabla de enrutamiento.  
Verificar el estado de las interfaces.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/32f6425d-692a-464f-b6a3-221599bd9965)

### Práctica 2: Enrutamiento estático y por defecto
Configurar rutas predeterminadas estáticas flotantes y estáticas IPv4 e IPv6.  
Configurar rutas estáticas estáticas y flotantes IPv4 e IPv6 a las LAN internas.  
Configurar rutas de host IPv4 IPv6.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/4b081036-8a62-4832-909b-0337400f0d5e)

### Práctica 3: OSPF P2P y OSPF Multiacceso
OSPF P2P:  
Configurar los router IDs.  
Configurar las redes para el enrutamiento OSPF.  
Verificar la configuración OSPF. 
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/85a33cb8-bc1d-498f-b98f-be9bac404005)

OSPF Multiacceso:  
Examinar las funciones cambiantes del DR y el BDR.  
Modificar la prioridad OSPF y forzar las elecciones.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/29bfe561-fd9a-4708-8233-22844b539806)

### Práctica 4: Enrutamiento OSFP Monoárea
Implementar OSPFv2 de área única en redes difusión de acceso múltiple y punto a punto.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/15677705-f39d-4d42-a72c-e4a5ae8c1fb0)

### Práctica 5: Configuración de HSRP
Configurar un router activo HSRP.  
Configurar un router en espera HSRP.  
Verificar el funcionamiento de HSRP.  
![image](https://github.com/javichocou007/trabajoDI/assets/121022101/268d54fa-8d25-4e44-85f4-820655a92710)
