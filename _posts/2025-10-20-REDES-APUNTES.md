ÍNDICE



Definiciones	3
TEMA 1 REDES LOCALES	3
1.0 RED LOCAL	3
VENTAJAS	3
1.1 CARACTERÍSTICAS CPDS Y SERVIDORES	5
SERVIDOR	5
CLOUD	5
2.0 ELEMENTOS RED LOCAL	5
3.0 CLASIFICACIONES DE REDES Y CRITERIOS	7
SEGÚN SU TAMAÑO O EXTENSIÓN	7
SEGÚN LOS MEDIOS DE TRANSMISIÓN	8
GUIADOS	8
NO GUIADOS	9
SEGÚN LA TOPOLOGÍAS DE RED	9
SEGÚN LA TECNOLOGÍA DE TRANSMISIÓN	10
SEGÚN EL MODO DE TRANSMISIÓN	10
4.0 TIPOS DE SERVIDORES	10
TEMA 2 PROTOCOLO TCP/IP	12
EJERCICIOS	14
ESTÁTICAS/DINÁMICAS	15
RESERVAR/EXCLUIR IPS DHCP	16
RANGO DIRECCIONES PRIVADAS	16
EJERCICIOS	17
ENRUTAMIENTO	18
INTRODUCCIÓN AL PROTOCOLO TCP/IP	20
PROTOCOLO DHCP	22
PROTOCOLO ARP	23
PROTOCOLO DNS	23
DNAT	24
SNAT	24
COMO FUNCIONA TCP/IP EN LA REALIDAD	25
ICMP	28
TEMA 3 NIVELES FÍSICO Y ENLACE	29
NIVELES FÍSICOS	29
HERRAMIENTAS	29
DEFINICIONES	29
EJERCICIO	30
FIBRA ÓPTICA	31
EJERCICIO	31
VELOCIDADES MEDIOS	32
NIVEL ENLACES	32
CARACTERÍSTICAS AL COMPRAR SWITCH	35
REDES VIRTUAL (VLANS)	37
VLANS	37
ESPECIFICACIONES DE CISCO	38
NAT	38
SNAT	38
DNAT	39
SNAT CISCO	39
CORTAFUEGOS	39
NODO	40
PERIMETRAL	40
MODULOS IPTABLES	41
COMANDOS	42
ENCAMINAMIENTO DINÁMICO	42
PROTOCOLOS DE VECTOR DE DISTANCIA	42
PROTOCOLO DE ESTADO DE ENLACE	43
VPN (VIRTUAL PRIVATE NETWORK)	43


Definiciones



Help Desk: Técnicos encargados de la resolución de problemas, hay varios niveles [1-3], y estos son escalables en función del problema.
Servidores: Máquinas con gran hardware, estas normalmente no tienen teclado ratón ni pantalla ya que a estas se accede a través de red normalmente por ssh, normalmente solo acceden a ellas los administradores
INTRANET: Conjunto de hardware y software que tiene la empresa para los trabajadores de esta, la información se tiene en un servidor de datos y se accede a través de un servidor web, es una manera de organizar el trabajo de una empresa, a través de la web directamente realiza todo lo que necesite: EJ: SÉNECA; Siempre te tienes que identificar para acceder a esta
EXTRANET: Obsoletas ya que todas las intranet permiten ya el acceso remoto
DNS SOBRE HTTPS(DOH): 
Protocolo: Conjunto de normas 
RFC: Request for comments
TORMENTA DE BROADCAST: Principalmente creadas por un bucle en algun switch de la rede local lo que genera un colapso de la red por completo 
TTL: Tiempo de vida de los paquetes, cada vez que salta se reduce a uno evitando para evitar paquetes perdido sin la red




TEMA 1 REDES LOCALES
1.0 RED LOCAL
Una red local es el conjunto de ordenadores y/o dispositivos (nodos) conectados entré sí que comparten información recursos o servicios, para que esto ocurra se necesita transmision
VENTAJAS 
Compartir recursos: Esto reduce el número de periféricos evitando comprar uno por cada equipo (Consecuencia: Más espacio y menos gastos)
Compartir información: Los dispositivos pueden compartir información, a través de carpetas compartidas, servidores de datos o servidor web si se utiliza una Intranet
Fiabilidad: Se mejora la fiabilidad pudiendo realizar copias de seguridad almacenadas en un servidor de datos, redundancia de los servidores más importantes y las actualizaciones se podrán hacer desde la red evitando hacerlas manualmente
Rendimiento: Se puede mejorar el rendimiento montando y utilizando clusters de ordenadores
Alta disponibilidad: Conjunto de ordenadores con redundancia entre si o de un servicio específico
Alto rendimiento: Conjunto de ordenadores haciendo tareas cooperativas para obtener mayor rendimiento. Antes del cluster suele haber un balanceo de carga para dividir las peticiones, procesos…

Medio de comunicación: Al montar la red, los miembros de esta pueden estar comunicados entre sí, a demás está comunicación se puede regular por ejemplo en distintos departamentos u otorgar más privilegios a algunos usuario que otros

1.1 CARACTERÍSTICAS CPDS Y SERVIDORES



Mantener estable la temperatura y buscar una temperatura fría sin que se condense la humedad para evitar mojar los servidores. En función del precio de la luz se pone a una temperatura u otra dependiendo si sale más rentable o no (antes 16ºC/17ºC ahora 20ºC/23ºC)



Los servidores se almacenan en armarios en forma de rack normalmente estos armarios tienen medidas estándares y se mide por unidades de armarios (rack) por ejemplo 42U.



SERVIDOR
En comparación con un cliente, más CPU, RAM, Discos más rápidos, mayor calidad, Redundancia(Métodos para seguir con el funcionamiento de este), 95% linux
CLOUD
Escalabilidad de recursos y pago por lo que uso



2.0 ELEMENTOS RED LOCAL



SERVIDOR: Equipo o dispositivo que provee de uno o varios servicio




CLIENTES: Equipo o dispositivo que solicita servicios al servidor




Suelo técnico: Un suelo que se pone por encima del suelo verdadero para ocultar los cables
Ventajas: No hay que tirar canaletas, si hay cambios en la oficina no hay problemas a diferencia de las canaletas que si estorban 
Desventajas: Caros





OTROS DISPOSITIVOS: Además de servidores y clientes se pueden encontrar impresoras Plotter…




TARJETAS DE RED: Permite la conexión de dos ordenadores entre sí, puede estar integrada en la Placa Base, en un slot de expansión o a un puerto USB… (Conector hembra)




CABLES Y CONECTORES
Cables RJ45: Ambos extremos conectores machos, encargados de la conexión de una tarjeta de red con otra u otro elemento de la red





PATCH PANNEL: Conjunto de conectores hembras (4,8,16,24) al que se conectan los cables de red de las canaletas y de ahí otros cables hacia el switch




cable pc-roseta: Latiguillo




cable roseta-patch pannel: Canal permanente




cable patch panel-switch: Latiguillo de armario




Canaletas, torres y paneles: 
Las canaletas son estructuras las cuales protegen y cubren los latiguillos, hay de suelo y techo
Torres de suelo: Puntos de corrientes
Paneles: Puntos de corrientes





Hub: Precursores de los switch y tontos, son pura electrónica, toda señal que le llega por una boca la reenviar por el resto, cosa que no sucede con el switch. No tenía seguridad a la hora de transmitir los datos




Switch: Dispositivo que sirve para crear una red local, lo que permite la conexión de diferentes dispositivos, similar al hub, pero reenvía los datos según una dirección MAC especificada en los datos a transmitir




Router: Dispositivo que conecta dos o más redes distintas




Router doméstico: Actúan como un pequeño switch punto de acceso e interconectan las redes del proveedor de internet y la red local





*REGLA PARA LAS CANALETAS: SOLO SE PUEDEN USAR ⅔  DEL ÁREA DE LA CANALETA EJ: CANALETA CON ÁREA DE 1000 CM 2 SOLO SE PUEDE UTILIZAR 666 CM 2 ESO DIVIDIRLO ENTRE EL ÁREA DEL CABLE (60 CM 2) 660/60 = 11 CABLES POR CANALETAS*



AP/WAP: Dispositivo similar al hub pero el medio de transmisión de datos es el aire, estos dispositivos normalmente van conectados a otro dispositivo como un switch o un router, en otros casos se conectan directamente con la línea telefónica, a este tipo se le conoce como router inalámbrico




Las redes inalámbricas son como las redes conectadas por hubs, el medio del aire es el mismo para todos por lo que los paquetes chocan de no ser porque hay métodos para controlar la emisión de paquetes y hay métodos de encriptación para garantizar la integridad de los datos que transmite los dispositivos (WPA2/3)



Armarios: Pueden tener varias entradas además de la puerta, entradas superior e inferior y paneles laterales desplegables. Hay armarios con una bisagra que permiten extraer todo el contenido para poder abrirlo y reparar en cualquier momento de forma muy cómoda




CUADRO ELÉCTRICO
INTERRUPTORES DIFERENCIALES: Protegen a las personas, si la electricidad se está fugando por algún lado, corta la serie de circuitos necesarios
INTERRUPTORES MAGNETO TÉCNICO: Protegen la propia instalación: Genera un circuito y a ese circuito se conectan dispositivos eléctricos. Hay varios interruptores magnetotérmicos, para diferentes circuitos de diferentes amperajes


	10A—------1,5mm2 alumbrado
	16A—------2,5mm2 fuerza
	20A—-------Frigorifico lavavajillas
	25A—-------Horno



10A*220V==2200W



por cada 3 magnetotérmicos 1 diferencial en instalaciones de red
cables negativo positivo y masa
conectores
mesas electrificadas



PLANIFICAR REDES



Saber material a utilizar y calcular los costos
Saber plasmar gráficamente la estructura de la red (planos)
Saber las tareas que se van a necesitar, personal necesario para llevar a cabo las tareas, el orden para hacerlas y saber cuales se pueden hacer a la vez y cuales no



armariorack.es




3.0 CLASIFICACIONES DE REDES Y CRITERIOS
SEGÚN SU TAMAÑO O EXTENSIÓN



PAN: Personal area network, en estás redes normalmente el método de comunicación es bluetooth.(Mobile-wearables)
Acceso muy sencillo
Radio de alcance muy limitado
Inalámbrica
Costes de instalación bajos o nulos.

LAN: Local area network, el tamaño de estás son de edificios, oficinas o casa. En ámbito doméstico lo normal es inalámbrica, suele ir a un tercio de la red cableada y esa velocidad dividirla entre los dispositivos conectados a esta en ámbito profesional cableada.
Velocidad de transmisión de 1Gbps
Toda la red pertenece a una misma organización (privada)
Tamaño de edificio oficina o casa 

MAN: Metropolitan area network, cubren una ciudad pueblo o una ciudad y los pueblos de alrededores
Suelen trabajar con fibra óptica
Suelen ofrecer servicios integrados como datos, voz y video

WAN: Wide area network, redes que cubren países o continentes








SEGÚN LOS MEDIOS DE TRANSMISIÓN
GUIADOS 
Es el medio por el que viajan los datos, medios guiados(cables) o medios no guiados (inalámbricas) o mixtas
Hay varios tipos de cables para los medios guiados



Par paralelo: Dos hilos de cobre paralelos con una funda de plástico, es muy vulnerable a las interferencias
Par trenzado: Contiene 8 cables en 4 parejas de 2, al estar trenzado es mucho más resistente a las interferencias electromagnéticas
Fibra óptica: Contienen un hilo de un porómetro para que circule y rebote la luz. Alcance mucho más ampliado, depende de la calidad









Coaxial: Se utilizan para los enlaces exteriores desde el punto de acceso hasta las antenas, compuesto de una parte interna después funda de plástico,maya de cobre y otra funda de plástico. Cuesta mucho conectorizar un cable coaxial




NO GUIADOS
Utilizan el aire como transmisor dependen mucho de la frecuencia si distancia aumenta y la facilidad de atravesar obstáculos
Ondas de radio:
Microondas:
Infrarrojos: Poco alcance y necesita visión directa
Ondas de luz: Antiguo método,
Lifi: Utilizando los leds, se envía información, similar a los infrarrojos se necesita visión directa

 SEGÚN LA TOPOLOGÍAS DE RED



Se refiere a la estructura de los dispositivos de la red



Topología en bus: Contaba con un único cable al que se iban conectando los ordenadores, no había un nodo central de la red. Compuesto por un cable coaxial y en los extremos 2 terminadores para evitar que la señal rematará. Red muy barata, desventaja al haber una avería la red entera se caía. Para averiguar la avería se quitaba el terminador del final y se iba poniendo en diferentes alturas para averiguar dónde estaba el fallo. El ancho de banda se dividía por el número de máquinas.




Redes en anillo: Se utilizan para redes con gran volumen de tráfico, tiene el mismo error que las redes en bus a la hora de sufrir una avería y se suele utilizar 2 anillos, para evitar los problemas y tener una a modo de soporte (redundancia), se suelen poner por diferentes lugares un anillo de otro, cada nodo que se conecta a este actúa de repetidor, se suele utilizar en redes MAN




Redes en estrella: Utilizan un nodo central normalmente un switch o un conjunto de estos. Normalmente cuando dos elementos de la red se quieren conectar el switch hace de intermediario, el tráfico siempre pasa por el. Cuando se estropea una parte de la red solo se estropea esa parte y el resto de la red sigue funcionando y el ancho de banda no se comparte siempre que las comunicaciones entres los nodos sean diferentes entre sí (PC1-PC2  PC3-PC4), la desventaja el la cantidad de cable que se necesita




Redes mixtas: En la realidad las redes se forman juntando las topologías anteriores por ejemplo estrella-estrella anillo-estrella anillo-estrella-estrella





VPN: lÍNEA DE TRÁFICO CIFRADO PERO SE UTILIZA LAS LÍNEAS DE INTERNET, ESTA LÍNEA VIAJA POR INTERNET ENCRIPTADAS



BEST EFFORT: Mejor esfuerzo
SEGÚN LA TECNOLOGÍA DE TRANSMISIÓN



Punto a punto: La comunicación se hace solo entre 2 nodos. Se puede dar de dos maneras
Conmutación de circuitos: Primero se establece la conexión antes de la conexión, en los repetidores por los que se va a realizar la conexión se debe de reservar un slot(hueco en los repetidores), si no hay slots libres no se puede realizar la comunicación . Cuando se finaliza la comunicación se liberan los slots
Conmutación de paquetes: Se divide la información y se envía por un camino que no tiene porque ser el mismo siempre





Difusión: Los mensajes interesa que lleguen a todo el mundo, no tiene ningún receptor específico.

SEGÚN EL MODO DE TRANSMISIÓN



Simplex: La comunicación es unidireccional, El transmisor es capaz de transmitir pero no recibir o el receptor es capaz de recibir pero no de responder




Semi-dúplex: Puede ser bidireccional pero no simultánea, se puede recibir y escuchar pero no a la vez EJ: Walkie Talkie o tarjetas de red




Full-duplex: Transmitir y recibir simultáneamente




4.0 TIPOS DE SERVIDORES



Los de BASE DE DATOS: Almacena la información de forma relevante sobre la empresa guardando esta en forma de tablas, esta información se consulta con aplicaciones o programas de la empresa. Compuesto de discos duros con mucha capacidad. Un cliente utiliza la aplicación o navegador que lleva a una página web (servidor web), en función de lo que solicite en la web, este servidor web se conecta al servidor de base de datos y este ya devuelve la información de las tablas 





LOS SERVIDORES WEB: Un cliente realiza peticiones a través de navegadores web en un lenguaje http o https. Para que un ordenador funcione como un servidor se necesita un software específico para que este ofrezca servicios y ser un servidor, en caso de un servidor de base de datos utilizo oracle en uno web apache. Estos software permiten al servidor entender el lenguaje con el que se realiza la petición de las otras máquinas. Estas máquinas son las que guardan las páginas webs de las empresas




	PROPIO: Libertad total sobre el servidor desventaja



SERVIDOR PROXY: Su función es compartir la conexión a internet con otras páginas. Es importante ya que permite cachear las páginas, es decir almacenar las webs que se solicitan. Cuando se realiza una consulta a una web, el proxy almacena temporalmente una copia de esta para cuando se vuelva a solicitar no navegar por internet. Las paginas con https con login no se cachean. Con el incremento del https esta parte del proxy está siendo obsoleta. Cuenta con 2 funciones más importantes




Centralizar la navegación: Es importante para monitorizar el tráfico de la red, los proveedores de internet registran los tráficos de los clientes, en caso de utilizar VPN se sabrá que se ha utilizado una vpn pero no donde ni que se transmite por esta. 




Filtrado de tráfico: Se puede configurar como una especie de firewall de lista negra o blanca para limitar la navegación incluso bloquear búsquedas de palabras concretas o webs que contenga en su url palabras concretas





SERVIDOR APT-PROXY: Caché paquetes de linux, si se tiene montado, en vez de guardar copias de las webs guarda los paquetes




SERVIDOR PROXY-INVERSO: Si en una red hay varios servidores webs guarda la lista de los servidores que devuelve




SERVIDORES DE MÁQUINAS VIRTUALES: Los clientes a través de una interfaz gráfica se accede al servidor de las máquinas virtuales, esta interfaz suele ser alojada en un servidor web que en estos casos se suelen alojar en la misma máquina que actúa de servidor de máquinas virtuales



 TEMA 2 PROTOCOLO TCP/IP









BINARIOS



2⁷	2⁶	2⁵	2⁴	2³	2²	2¹	2⁰
0	1	0	1	1	1	1	0



0	64




Hexadecimal base de numeración de base 16 (16 dígitos posibles), son:
1-9 A,B,C,D,E,F 



A=10
B=11
C=12
D=13
E=14
F=15



El numero más grande con 2 digitos en hexadecimal es FF



FF
F¹	+ F⁰



15*15	+15*1





PARA PASAR DE BINARIO A HEXADECIMAL
0	1	0	1	1	1	1	0
—----------------------------	—-----------------------------
	5				E



5*16¹ +E


EL NÚMERO 123



2⁷
2⁶
2⁵
2⁴
2³
2²
2¹
2⁰
128
64
32
16
8
4
2
1
1
0
1
0
0
1
0
0







DEC-BIN		BIN-DEC
123			00110011
18			10101000
200			11101110
220			01011110
115			10111110	




01111011		51
00010010		168
11001000		238
11011100		94
01110011		190




Comando ip a devuelve información de la tarjeta de red, en esta información podemos ver



El estado: State UP/DOWN
Dirección de enlace (link) y el tipo (ether): 4c:cc:6a:e5:ec:ce esta es la direccion MAC, cuenta con 48 bits en bloques de 8 bits 
4c: este es un bloque de 8bits



Los primeros 24 bits indican el fabricante y modelo




inet(direccion a nivel de red): Es la dirección ip y se usa en el nivel de red, escrita en decimal separadas por punto con 4 numeros 112.22.34.1 llamada notación decimal puntuada
Cada número es un conjunto de 8 bit en siendo un total de 32 bits
1011010101010101010101010101010





El uso de binarios se utiliza en las direcciones IP



ENLACE: Dirección MAC de 48bits 00:00:74:32:A7:B1
RED: Dirección de IP (32 bits, representada en notación decimal puntuada) + Máscara de red (32 bits)




En una dirección IP hay 2 partes, una parte que se refiere a la red en la que estoy y otra parte al host concreto de esta red.



Es importante saber que parte es necesaria para la red y otra para el host ya que si hay varios host en la misma red, se pueden comunicar sin un ruter. 



Para saber que parte pertenece a la red dentro de una ip se utiliza una mascara de red, la máscara de red indica la cantidad de bits que se utilizan EJ: 192.168.x.x = 1111111.1111111.00000000.00000000
Los bits a 1 son los utilizados por la red los 0 al host



Se utilizan 2 notacions, la decimal puntuada 255.255.255.255 o /32



192.168.0.1 /16: Utiliza los primeros 16 para la red, el resto host
192.168.0.1 255.255.0.0: Utiliza los primeros 16 para la red, el resto host



EJERCICIOS
Di si estas parejas de ordenadores están en la misma red



192.168.1.1 /16

192.168.0.1 /16 	SI



192.168.1.1 /24

192.168.0.1 /24	NO



80.59.1.152 /28

80.59.1.201 /28	Los bits del 25 al 28 son diferentes por lo que NO estan en la misma red



01010000.00111011.00000001.10011000
01010000.00111011.00000001.11001001 



12.11.13.14 /12

12.14.12.13 /12	Los 12 primeros bits SI coinciden



12.00001011.13.14
12.00001110.12.13




120.140.160.180 /18

120.140.180.200 /18		SI



120.140.10100000.180
120.140.10110100.200



200.200.200.200 /5

160.0.0.0	/5		NO, a demás la segunda IP es la dirección de una red



11001000
10100000



ESTÁTICAS/DINÁMICAS
Dos ordenadores no pueden tener una misma IP en la red, porque no se identifican, en una red pequeña se pueden poner las IP estáticas pero en redes grandes no es factible por lo que se configura la máquina para que estas tengan ip dinámica



Puerta de enlace: Nodo de mi red, al que voy a enviar los mensajes con destino fuera de la red local (router, máquinas cortafuegos y configuradas como router, proxy …)



Estáticas: Se configuran a mano.
Dinámicas: Aplica el modelo cliente servidor, las máquinas clientes solicitan una configuración IP al servidor DHCP dentro de está configuración se encuentra la IP a utilizar (IP, máscara de red, puerta de enlace, servidor DNS …)




Cuando se configura un servidor DHCP se puede configurar para reservar una IP para nodos específicos evitando así que siempre cambie, esto puede aplicarse a servidores o nodos como routers si estos cambian la IP los clientes no saben encontrarlos para ello en la configuración DHCP se puede reservar para esos dispositivos 



RESERVAR/EXCLUIR IPS DHCP
Se puede configurar un rango de direcciones IPs 172.22.0.0 /16
exlused.address 172.22.0.1 - 172.22.0.6



Tambien se pueden por reservas 



Reserves



MAC
IP
Mac_servidor
Ip_para_maquina_con_esa_mac
A1:B1:B1:A1:C2:C3
172.22.0.3/16



default-lease-time 86400; Esta configuración indica el tiempo válido de asignación de la ip de la máquina



fixed-address 192.168.1.3: Esto es para una reserva



ISP: Proveedores de servicio de internet



Un router doméstico de nuestra casa tiene 2 caras una red local que actúa de DHCP para los dispositivos de nuestra casa y otra cara en la que actúa de cliente y solicita la configuración IP del servidor DHCP el cual es un router o máquina de nuestro ISP



Las IPV6 están compuesta por 128 bits, fue una solución ante la futura falta de IPV4 en el mundo, la implantación de IPV6 es muy lenta a hoy dia no está implementado al completo, después de eso crearon las IPs públicas e IPs privadas



IPs públicas: Estas IPsV4 si son únicas en el mundo 
IPs privadas: Con estas IPsV4 no son únicas se repiten en millones de redes pero si es única en una red local, con estás IPs no se puede navegar por internet.



Para navegar por internet se utiliza la IP pública asignada al router que es asignada por el ISP, en las redes locales cuando algún equipo necesita navegar, se realiza un proceso llamado NAT por el cuál se utiliza la IP publica del router en vez de las privadas de las máquinas
RANGO DIRECCIONES PRIVADAS



	10.X.X.X
	172.16.X.X-172.31.X.X
	192.168.0.X-192.168.255.X


NAT: Normalmente se configura en los router, proceso por el que se traduce las IPs de públicas a privadas, también se puede configurar en otros dispositivos



Mascara de red: Numero de 32 bits que me dice que parte es dirección de red y que parte es el numero de host dentro de esa red



Hay una dirección que es la primera es decir en en una /24 la ip 192.168.0.0 es la primera y representa a toda la red, no se puede asignar a ninguna maquina



Hay una dirección llamada dirección de difusión que es la ultima, es la dirección para enviar un mensaje a toda la red esta representa a todos los ordenadores, con la misma red de arriba la difusión seria 192.168.0.255



EJERCICIOS 
Tengo un ordenador con la IP 130.120.240.12 y máscara de red /20



Indica:
La máscara de red en notación decimal puntuada
La Dirección de la red.
La dirección de difusión de esa red
El número de ordenadores que puede tener esa reed
De qué dirección a qué dirección podemos usar para identificar los ordenadores de esa red
Si el ordenador con IP 130.120.250.2 pertenece a esa red




a)255.255.240 .0
b)Es la primera dirección de esa red, es decir aquella que tiene todos los bits de host a 0 
130.120.240.12
100000010.01111000.11110000.00001100
100000010.01111000.11110000.00000000
130.120.240.0




c)130.120.240.12
100000010.01111000.11110000.00001100
100000010.01111000.11111111.11111111
130.120.255.255



d) Necesitamos saber cuantos bits tenemos para enumerar los ordenadores



Cuento los bits de host y realizamos la siguiente operación 
2^n host - 2
2¹² - 2 = 4096 -2 = 4094 ordenadores



C) Necesito utiliza la primera que es posible asignar a los equipos por lo que la .0 no es validad y lo mismo con la de broadcas .255 no vale



130.120.240.1 hasta 130.120.255.254



f) Comprarlo los primeros bits 20 bits o miro si está entre el rango de las IPs validad





ENRUTAMIENTO
En un router cuando llega un mensaje se mira el destino de este y se empieza a leer la tabla de enrutamiento de este para saber por dónde enviarlo



Si quiero llegar a algun servidor, no se sabe cómo llegar al servidor sino que se sabe utilizando el gateway iré saltando de router en router hasta llegar a mi destino, estos routers no saben el camino completo pero saben cual es la mejor opción posible para llegar al destino, estas mejores opciones se basan la cantidad de saltos de router en router, ver la cantidad de tráfico si está muy saturado se descarta, que esté operativo o la cuota que impone el ISP.



En internet hay miles de routers pero normalmente para llegar al destino lo normal es dar entre 8-15 saltos a otros router, si un paquete llega a dar 65 saltos este se elimina ya que se considera perdido.



Una tabla de enrutamiento va a contar con las siguientes columna



DESTINO 	SIG_ROUTER		INTERFAZ_SALIDA	COSTE
IP_DESTINO   IP_sig_router + interf	mi_interfaz_salida





En redes locales se utiliza enrutamiento estático donde se rellenan las tablas manualmente y en internet se utiliza el enrutamiento dinámico que utilizan un algoritmo (OSPF,RIP…)
estos algoritmos preguntan constantemente a sus vecinos cuanto tardan y a donde saben llegar con esto ya saben por donde enviar los paquetes



En las tablas de enrutamiento primero se busca las IPs de las máquinas en caso de que no exista se busca la IP de la red que tambien es valida, las tablas se leen verticalmente



Si queremos evitar las conexiones con una red o máquina específica, normalmente se utiliza cortafuegos pero con tablas de enrutamiento también se puede utilizar modificando la ip de destino por una que no existe tambien puede funcionar modificando la interfaz de salida pero a veces los routers no te deja esta opción



En la vida real debemos de optimizar las rutas, analizarlas para saber la cantidad de trafico que tienen para saber cual es la mejor ruta


En una red tenemos un ordenador configurado con la IP 192.168.1.239 CON LA MÁSCAR /29



Indica la máscara de red en notación decimal puntuada
La dirección de la red en la que está dicha máquina
La dirección de broadcast o difusión de la red en la que está dicha máquina
El número máximos de dispositivos que porá tener esa red
Como prodrá comunicarse el ordenador anterior con la máquina 192.168.1.250




255.255.255.248
192.168.1.111011111 -> Ip maquina 

	192.168.1.111011000
	192.168.1.232
192.168.1.111011111 -> Ip maquina 

	192.168.1.111011111 -> 192.168.1.239
2³-2 = 8 -2 = 6
Esta máquina no puede comunicarse ya que tiene asignada la dirección e broadcast de la red /29, además la ip X.X.X.250 estaría fuera de la red ya que supera la 239 o al ser otra red a través de un router 





En una red tenemos un ordenador configurado con la IP 172.22.68.12 CON LA MÁSCAR /20



Indica la máscara de red en notación decimal puntuada
La dirección de la red en la que está dicha máquina
La dirección de broadcast o difusión de la red en la que está dicha máquina
El número máximos de dispositivos que porá tener esa red
Como prodrá comunicarse el ordenador anterior con la máquina 172.22.90.1




	f) 255.255.240.0
	g) 172.22.01000100.00001100 -> IP maquina
	     172.22.01000000.0000000 -> 172.22.64.0
	h)172.22.01001111.11111111 -> 172.22.79.255
	i)2¹²-2 = 4096-2 = 4094 host disponibles
	j)La ip X.X.90.1 es de otra red por lo que se necesitarán conectarse a través de un router 




TRUCO PARA CALCULAR LAS POTENCIAS
2¹⁰ = 1024
2²⁰ = 1048576



2¹² = 2¹⁰ * 2²



2¹⁶ = 2¹⁰ * 2⁶



2²⁹ = 2¹⁰ * 2¹⁰ * 2⁹ = 2²⁰ * 2⁹
INTRODUCCIÓN AL PROTOCOLO TCP/IP 
Hay otros protocolos aparte de TCP/	IP hace años las empresas como IBM tienen sus propios protocolos por lo que solo las maquinas de esas marcas podían comunicarse entre si y no con otras de otras marcas
Se decidió crear un protocolo que no fuera propiedad de nadie, esté fue TCP/IP que durante años estuvo compitiendo con los protocolos de las empresas como IBM, MICROSOFT… hasta los 90 donde TCP/IP ya se usaba en internet.
En TCP/IP divide sus normas en diferentes capas o niveles (físico, enlace,red,transporte y nivel de aplicación)
Físicos: Garantiza que un PC puede transmitir y recibir información.

Normas como pueden ser el tamaño de los conectores, el orden de los cables RJ45, la potencia de señal de transmisión etc. Aspectos eléctricos y electrónicos principalmente nos centraremos en redes de cobre donde si hay voltio representan 1 si hay ausencia de voltios es 0, en redes inalámbricas se utiliza un cambio de fase de ondas y en fibra óptica es similar al cobre pero con pulsos de luz



Enlace: Dos nodos que están en la misma red local se puedan comunicar, cómo saber cuando un ordenador puede transmitir o no (control de acceso al medio), también casi todo lo relacionado con los switch, en resumen la relación de cómo funcionan las redes locales. También se encarga de la forma de acceder al medio y saber si es capaz de transmitir viendo si el medio de transmisión está libre para evitar colisiones de los paquetes




Detección de colisiones: Se usa en redes de cobre e inalámbricas. Los nodos que quieren transmitir se ponen en escucha para saber si el canal está ocupado, en caso de estar ocupado se espera X tiempo si no empieza a transmitir. Hay un periodo de tiempo en el que un equipo empieza a transmitir pero el equipo no le ha dado tiempo de escuchar por lo que también empieza a transmitir y se producen las colisiones. La encargada de esto es la tarjeta de red.




Paso de testigo: Se usa en redes de fibra óptica. Al ser normalmente redes en anillos con mucho tráfico la detección de colisiones no funciona muy bien por lo que se utiliza este método. Consiste en asignar X tiempo por segundo para transmitir a los equipos.




	En el nivel de enlace también se divide la información en paquetes o tramas, dependiendo del tipo de medio de transmisión el tamaño de los paquetes varían.



MTU (Max Transfer Unit): Tamaño máximo de un paquete en función del medio porque sino el rendimiento de la red baja y la probabilidad de fallo aumenta, en redes inalámbricas el MTU es bajo por lo que se envían paquetes más pequeños, en fibra óptica se dividen en paquetes grandes y en cobre es un término medio. Se puede configurar el tamaño de estos




	También se añaden mecanismos para saber sin un mensaje a llegado correctamente para comprobar la integridad de los datos transmitidos, utilizando un CRC (Código redundante cíclico), antiguamente se usaba el bit de paridad, si se iban a transmitir 8 bits el emisor añadía otro donde antes de comunicar se llegaba a un acuerdo el emisor y el receptor si se decidía par o impar el bit del final que se complementa para comprobar si el mensaje llega íntegro, pero esto solo funciona cuando falla 1 solo bit en la transmisión ya que si fallan 2 estos pueden camuflarse entre sí y no permite saber en qué posición ha fallado. Más adelante se complementa con 3 bits de paridad en vez de 1 teniendo que transmitir un 30% más por lo que satura mucho la red y esto solo se puede permitir en transmisiones que no pueda perder la información.
Una tarjeta de red coje los 1500bytes del mensaje este mensaje se somete a una división por un polinomio y nos quedamos con el resto (circuito integrado) y se obtiene del resto un número de 32 bits que es el CRC finalmente el receptor recopila los bytes del paquete y realiza la misma operación y compara el resultado con el número de 32bits. Es decir por cada 1500 bytes se transmiten 15004 bytes.



Control de flujo: Si el buffer (pequeño espacio de almacenamientos), está lleno de la información recibida, para evitar que se pierda la información, activa el mecanismo de control de flujo, al ejecutarlo la tarjeta de red envía una señal al emisor para indicar que pare de transmitir y evitar la pérdida, después de que el buffer baje de x umbral le indica que vuelva a transmitir.




Red: Dos ordenadores de diferentes redes puedan comunicarse, en general todo lo que tiene que ver con conectar 2 redes diferentes y el dispositivo encargado de esto es el router. Las máquinas se identifican por IP y no por mac y es el encargado del que los ordenadores de diferentes red se puedan comunicar.
Enrutamiento de trama: como hacer que un mensaje llegue hasta su destino aunque tenga que atravesar distintas redes.
También se regula la congestión de la red, en caso de que los routers tengan enrutamiento dinámico, estos son capaces de modificar las sus tablas de enrutamiento para escoger la mejor ruta
El router se encarga de reestructurar los tamaños de los paquetes de diferentes niveles de enlaces de distintas redes es decir los paquetes en una red wifi tienen X tamaño y se utiliza detección de colisiones, si para llegar al destino hay una red de cobre o fibra … el router hará la reestructuración de los paquetes para que pasen a tener Y tamaño y utilizar otro método de evitar colisiones como puede ser el paso de testigo





Transporte: Se encarga de que 2 programas/procesos se comuniquen entre sí, identificar qué programas deben comunicarse. Hay 2 protocolos principales que son TCP protocolo confiable que procura que la información llegue al destino o UDP no se garantiza que la información no llegue al destino, pero más rápido que TCP. En este nivel los procesos se identifican por la IP + Nº puerto, el UDP solo aporta los puertos de origen y de destino, siendo este protocolo más rapido que TCP pero menos fiable. TCP es más seguro debido a que enumera las tramas que se transmiten, añade un campo al paquete con la enumeración, el receptor al notar la falta de un paquete lo vuelve a solicitar. Los paquetes no tienen porque llegar al mismo orden por lo que si al receptor le llegan desordenados este es capaz de ordenarlos. Estos procesos es por lo que lo hace lento a diferencia de UDP. El puerto de origen identifica al programa que ha iniciado la conversación y el destino el puerto del programa destino. En un mismo ordenador no se pueden utilizar el mismo puerto para dos programas a no ser que uno sea TCP y otro UDP ya que hay 65.000 para TCP y otros 65.000 para TCP




Aplicación: Define la manera en la que un cliente se comunica con un servidor, conjunto de protocolos como HTTP o HTTPS que tienen diferentes comandos/ordener que se envían al servidor. Regula que información se va a mandar y que formato se va a  enviar está. Se define como va a ser la consulta (protocolo-comando), y como se va a transmitir la información




En muchos casos el nivel Físico/enlace se consideran uno solo.
Dentro de cada nivel no hay un único protocolo, por ejemplo en el nivel de enlace no es el mismo si se trabaja en una red cableada o inalambrica




Físico/enlace
ethernet, 802.11(wifi), 5G(telefonía), Token-Ring(fibra, normalmente redes en anillo…)
Red
IPV4, IPV6
Transporte
TCP, UDP
Aplicación
HTTPS, HTTP, FTP(transferencia de ficheros), RTSP(streaming), SMTP(correo)




TCP/IP es un protocolo abierto que se construyó por la comunidad, se utilizó un request for comment(RFC), donde la comunidad realizó sus propuestas, estas se estudiaron, se creó el boceto y se volvió a realizar otro RFC hasta que se hizo aceptable





PROTOCOLO DHCP
Protocolo que se encarga de asignar las configuraciones TCP/IP a los clientes con la configuración de IP dinámica.
Los clientes nada más encender el ordenador realizan peticiones al servidor, la conexión comienza de la siguiente manera



CLIENTE DHCP DISCOVER: Mensaje de broadcast a la rede que vva en busca de un servidor DHCP suponiendo varias opciones que haya un servidor, que no haya ninguno o que haya varios.
Un solo servidor: En este caso procedimiento normal (discover, offer, request, ack)
Ningún servidor: Se intentan varios discover, normalmente has 4 en caso de no recibir ningún OFFER los propios clientes se ponen una ellos mismo utilizando dependiendo del SO se utiliza APIPA o AVAHI. Las direcciones son 169.254.0.0/16 antes de colocarse la IP pregunta a la red 169.254.X.X si está libre en caso de que no pues pasa a la siguiente así hasta que esté libre. Esta solución permite comunicar los ordenadores que hayan tenido el mismo problema, lo que no van a poder salir a internet
Varios servidores: Pueden dar direcciones de la misma red o de diferentes redes. De ser el primer caso pueden dar direcciones repetidas. Lo normal al tener varios servidores es que falle media red aproximadamente y una mitad no tenga conexión con la otra

SERVIDOR OFFER: Le envía un paquete mostrándole la configuración TCP/IP siendo un mensaje de punto a punto y no de broadcast
CLIENTE DHCP REQUEST: El cliente le indica que acepta la configuración y le reserve esa ip
SERVIDOR ACK: El servidor le envía la configuración de la oferta y le reserva la IP a esa maquina (ACK=ACKNOWLEDGEMENT=CONFIRMACIÓN)




Te prestan la configuración por un tiempo concreto (Lease Time)
Se pueden establecer reservas de IP en el servidor DHCP (Ips fijas para máquinas concretas)
Se usan los puertos 67(servidor) y 68(cliente)
Controla las IP que quedan libres




PROTOCOLO ARP
Address protocol resolution, traduce direcciones IP a MAC.
El switch no entiende de IPS solo entiende de nivel de enlace es decir hasta MAC, entonces cuando quiero enviar un mensaje a un ordenador de mi red, el switch cuenta con una tabla con todas las macs de las bocas



ARP Request: Mensaje de difusión que indica “El que tenga esta IP que me diga su MAC”
ARP Reply: Mensaje que responde a la petición anterior

PROTOCOLO DNS
DNS(Domain Name Service) almacena los nombres de dominios que son la manera de llamar a un ordenador o conjuntos de estos, los nombres de dominios son visibles normalmente en las URL de las webs a las que navegamos.
Las url estan formadas por 2 partes www	.	gonzalonazareno.org
					PC			DOMINIO
Los DNS traducen direcciones de dominio(URLs) a direcciones IPS. Antes de la creación de estos se almacenaban en un ficheros las webs a las que tú navegabas con las ips correspondientes a estas. Este fichero se llamaba hosts.txt y lo tenias que descargar por ftp
Este fichero se actualizaba bastante rápido por lo que había que descargar nuevas versiones y cada vez pesaba más y se llegaba a tardar mucho en descargar. A partir de aquí se decidió mostrar los servidores DNS que son bases de datos jerárquicas donde la información no esta en el mismo servidor sino distribuida en diferentes servidores en todo el mundo y con espejos de todos estos.
Los principales servidores DNS son los raiz / y lo que contiene son enlaces con los dominios con las urls principales (.com .org .es .uk) que contiene las IPS de los DNS de primer nivel y estos almacena los dominios de primer nivel 



Las URLs se estructuran de la siguiente forma dit.gonzalo.org
La primera parte hasta el primer punto identifica la máquina y el resto los niveles DNS 



Los DNS no dan la IP del servidor web o el que sea debido a que estos estan en una red local por lo que solo devuelve la ip publica del router, las peticiones son enviadas a este y el propio router es el que se encarga de devolver las consultas



También sirve para identificar las máquinas de dentro de la red ej: servidor de bbdd = 192.168.1.9	o también como caché DNS evitando tener que realizar las resoluciones



Softwares de servidores DNS pueden ser bind9 y trabaja en el puerto 53



Los mensajes del protocolo DNS son 2
DNS Request: La petición de la ip de la URL que se solicita (la petición se realiza a los DNS configurados en mi maquina)
DNS Reply: Se responde con la IP publica del router del dominó que se solicitó




Los DNS están configurados en el fichero (/etc/resolv.conf)
Cuando el primer DNS no tiene la resolución de la URL este pasa a actuar como cliente y cuando recibe la respuesta esté la añade
DNAT
Proceso inverso a SNAT es decir de IP publica a privada, cuenta con una tabla donde se almacena el numero de puertos y las maquinas que tienen un servicio con esos puertos por ejemplo
3306	192.168.0.2
5432	192.168.0.2
Es una tabla muy parecida a la de SNAT pero no similar
SNAT
Proceso de traducción de ip privada a pública necesario para poder navegar con IPV4, este proceso se lleva a cabo en el router y almacena la IP de la petición en una tabla llamada snat con el número de puerto y la ip de la máquina



Este proceso se realiza en la petición del router cliente y en la respuesta del router del servidor y al volver simplemente se deshace el SNAT pero no es un proceso de DNAT



PAT(TRADUCCIÓN DE DIRECCIÓN DE RESPUESTA) se basa en modificar el puerto de la petición del cliente debido a que el puerto ya está ocupado y repetido por otro programa de otro dispositivo.




COMO FUNCIONA TCP/IP EN LA REALIDAD
En cada nivel se va añadiendo información a los paquetes



MENSAJE CLIENTE
APLICACIÓN








Comando de protocolo
(GET WWW.MARCA.COM)
TRANSPORTE







P.ORIGEN Y P.DESTINO
(*|80)
Comando de protocolo
(GET WWW.MARCA.COM)
RED
(Para saber la IP destino, parar y realizar petición DNS)






IP.ORG Y IP.DEST
(192.168.1.10 | )
P.ORIGEN Y P.DESTINO
(2000|80)
Comando de protocolo
(GET WWW.MARCA.COM)








P.ORIGEN Y P.DESTINO
(2000|80)
Comando de protocolo
(GET WWW.MARCA.COM)








P.ORIGEN Y P.DESTINO
(2000|80)
Comando de protocolo
(GET WWW.MARCA.COM)




PETICIÓN DNS



APLICACIÓN






DNS Request
TRANSPORTE





43258 | 53



RED




192.168.1.10 | 8.8.8.8




ENLACE
(COMIENZA PETICIÓN ARP PARA AVERIGUAR MAC GATEWAY)



MAC_ORG Y MAC_DEST
(MI_PC | MAC_GATEWAY)





FÍSICO









PETICIÓN ARG
MAC_BROADCAST = ff:ff:ff:ff:ff:ff



APLICACIÓN




ARP REQUEST
ENLACE



MAC_PC | MAC_BROADCAST



FÍSICO






*ROUTERS CISCOS CUENTAN CON UN PROTOCOLO SIMILAR A ARP QUE ESTÁ SIEMPRE PREGUNTANDO A LOS VECINOS CDP*



*Puerto, identificador que asigna el SO a los programas que se ejecutan para comunicarse con otro fuera de mi red local hay 65535
PRIMER PUNTO EJERCICIO SIMULACRO EXAMEN



Se solicita una petición web a un servidor (A-C)

Comenzamos con la creación del paquete de petición web
PET web							(5º mensaje por cable)
APLICACIÓN 








get URL
TRASNPORTE






S.D=4000*
P.D=80
get URL
RED




IP.S=172.22.1.35
IP.D=pet.DNS
S.D=4000*
P.D=80
get URL
ENLACE
MAC.S = cliente
MAC.D = gateway
IP.S=172.22.1.35
IP.D=pet.DNS
S.D=4000*
P.D=80
get URL



PET DNS		(3º Mensaje por cable)
APLICACIÓN








DNS.REQUEST
TRANSPORTE






P.S=2502*(llama a otro programa diferente que el que hace la petición web)
P.D=53
DNS.REQUEST
RED




IP.S=172.22.1.35
IP.D=8.8.8.8(primario)
P.S=2502*
P.D=53
DNS.REQUEST
ENLACE
MAC.S=(cliente)
PET.ARP
(cuando tiene la mac ya se envia)
IP.S=172.22.1.35
IP.D=8.8.8.8
P.S=2502*
P.D=53
DNS.REQUEST




PETICIÓN ARP	(1º Mensaje por cable)				MSG:ARP request
APLICACIÓN




¿quien tiene la ip 192.168.1.1? Díselo a la maquina x.x.x.x
ENLACE
MAC.S=mac_cliente
MAC.D=ff:ff:ff:ff:ff:ff
(broadcast)




RESPUESTA ARP	(2º Mensaje por cable)				MSG: ARP reply
APLICACIÓN




la ip pertenece a X mac
ENLACE
MAC.S=equipo_solicitada_anteriormente
(gateway en este caso)
MAC.D=mac_cliente




RESPUESTA DNS 	(4º Mensaje por el cable)				DNS REPLY
APLICACIÓN








URL is ip_router
TRANSPORTE






P.S=53
P.D=2502
URL is ip_router
red




IP.S=8.8.8.8
IP.D= maquina_cliente
P.S=53
P.D=2502
URL is ip_router
enlace
MAC.S= gateway
MAC.S= mac cliente
IP.S=8.8.8.8
IP.D= maquina_cliente
P.S=53
P.D=2502
URL is ip_router



RESPUESTA WEB		(6º PAQUETE DEL CABLE)		
APLICACIÓN








HTML WEB
TRANSPORTE






P.O=80
P.D = 4000*
HTML WEB
RED




IP.O=IP ROUTER
IP.D=172.22.1.35
P.O=80
P.D = 4000*
HTML WEB
ENLACE
MAC_ROUTER
CLIENTE
IP.O=IP ROUTER
IP.D=172.22.1.35
P.O=80
P.D = 4000*
HTML WEB



ICMP
ICMP no utiliza nivel de transporte


TEMA 3 NIVELES FÍSICO Y ENLACE
NIVELES FÍSICOS
¿Que nos podemos encontrar en una instalación física/infraestructura física, tipos de cable, y como se trabaja con ellas desde el punto de vista teórico?
Muchas veces vamos a tener que decidir con qué tipo de medio realizar una instalación ya sea medio guiado o no guiado, donde se compra o comercializa
Vamos a tratar mucho con switches tanto física o virtualmente en gns3



HERRAMIENTAS
Benchmark: Sirve para comprobar la velocidad real de trasmisión
iperf / iperf3: Indica la el ancho de banda de una conexion
DEFINICIONES
Velocidad de transmisión: Cantidad de información que se transmite por unidad de tiempo, se mide en bits por segundo (bps) o en multiplos (Kbps, Mbps, Gbps)
1Kb	—	1024 b
1Mb	—	1024 Kb
1Gb	—	1024 Mb



Ancho de banda: Máxima velocidad de transmisión de la información que ofrece el medio en condiciones ideales (máximo teórico)



Latencia/retardo de propagación: El tiempo que tarda el primer bit transmitido por el origen  en llegar al destino



La latencia y la velocidad de transmisión no están correlacionadas similarmente es decir tener más velocidad de transmisión no es tener menor latencia, no tienen relación



Atenuación: Es una pérdida de potencia gradual de la señal transmitida por el medio, aumenta proporcionalmente con la distancia recorrida y se mide en decibelios o en porcentajes. Normalmente la atenuación en muchos cables suele ser debida por el rozamiento pasando gran parte de la potencia de la señal por calor hasta llegar a un punto en que la señal sea indistinguible



Ruido: Perturbación electromagnética que sufre la señal en una comunicación, se puede producir por muchos motivos. Una señal electromagnética siempre puede tener ruido, debido a elementos naturales como el propio campo magnético de la tierra, tormentas solares o componentes electrónicos (amplificadores, circuitos etc) y no todos los componentes tienen una señal igual de tenue que otras. También por elementos externos como motores y tubos fluorescentes … para evitar estos problemas o disminuirlos ha normativas específicas



Para evitar el ruido podemos dejar de trabajar con electricidad y trabajar con pulsos de luz ya que la fibra óptica no se ve para nada afectada a los campos eléctricos 



Ancho de banda garantizado: El mínimo de ancho de banda en el peor de los casos

EJERCICIO
Un amigo me ha pedido que le pase una película que ocupa 4GB. Su casa está a 5 minutos de la mía andando. Mi conexión a Internet tiene un ancho de banda de 300Mbps, aunque la velocidad de transmisión real es de aproximadamente 30% del ancho de banda



¿Será más rápido llevarle el pendrive con la peli o mandarla por internet?



¿Cuál será la latencia en cada caso?



Andando: Velocidad de transmisión (Vtx) = 4GB /300 seg
1GB son 8Gb
4GB pasan a ser 32Gb



32Gb (*1024)-> 32768Mb / 300 segundos -> 109.23 Mbps




Por Internet: 300Mbps * 30 / 100 = 90 Mbps



En primer bits andando tarda los 5 minutos del camino a la casa 





Normalmente a la hora de transmitir gran cantidad de datos como puede ser copias de seguridad no me va a importar la latencia mientras la velocidad de transmisión sea mayor, sin embargo a la hora de realizar alguna actividad interactiva si nos interesa tener una latencia muy pequeña



Por ejemplo en algunos medios como puede ser el aire en tarjetas inalambricas es posible que en el momento en el que comienza a transmisión no escucha por lo el destinatario es el unico que se da cuenta de que se han chocados paquetes por lo que los vuelve a pedir sin embargo en otros medios como algun medio guiado en caso de que haya una colision estos si pueden ser capaz de darse cuenta y para volver a transmitir se espera un tiempo aleatorio








TRANSMISIONES ANALÓGICAS Y DIGITALES



Las señales analígicas representan funciones continues es decir en el rango que se transmiten por ejemplo 0V y 5V puede representar cualquier valor entre ese rango esto con el ruido y la atenuación la señal original cambia y el destinatario no es capaz de saber el valor de la señal original



Las señales digitales representan funciones discretas es decir no puede coger cualquier valor sino unos limitados por lo que el destinatario es capaz de reconstruir la señal original. En estos casos por ejemplo un cable UTP a los 100 metros incluso estas señales no son reconocibles ya que no se puede distinguir si la señal a esa distancia es un 5V con atenuación o un 0V con ruido







FIBRA ÓPTICA
Monomodo: El núcleo es tan pequeño que la luz no puede desviarse teniendo un alcance muy grande
Multimodo: Permite que la luz se propague en diferentes direcciones, el núcleo tiene un índice de refracción diferente al del revestimiento por lo que la onda de luz se propaga rebotando en las paredes del revestimiento
Salto de índice: El cambio de refracción entre el revestimiento  el núcleo es muy grande
Salto de gradiente de índice: El cambio de refracción se realiza poco a poco 





EJERCICIO
Un fichero de 4.7GB ha tardado en transmitirse 12 minutos ¿Cuál ha sido la velocidad de transmisión?



Datos: Cantidad de Información y Tiempo
Incógnita: Vtx



Segundos 12 * 60 = 720 segundos 
Cantidad de información 4.7GB 4.7 * 8 = 37,6Gb * 1024 = 38502,4Mb
720	38502,4
1	x
Velocidad de transmisión por segundo=38502,4/720=53,47Mbps



Cuanto tarda en transmitirse por una red wifi 802.11ac un fichero de 12GB si la velocidad de transmisión ha sido de un 40% del ancho de banda



Datos: Vtx y Cantidad de información
Incógnita: Tiempo
Cantidad de información= 12GB *8 = 96Gb * 1024 = 98304Mb
Velocidad de transmisión (40% de ) 1.300 Mbps. * 40 = 5200 / 100 = 520 Mbps
520	1
98304	x
Tiempo= 98304 / 520 =  189 segundos / 60 = 3,15 segundos



¿Qué cantidad de información puede transmitirse en una hora por un dispositivo móvil usando bluetooth 3.0?



Datos: Tiempo y Vtx
Incógnita: Cantidad de Información



Ancho de banda 24Mbps
Velocidad = 60 min = 3600 segundos
24Mb	1 segundo
X	3600 segundos
Cantidad de información transmitida en una hora: 24 * 3600 = 86400 Mbps / 1024 = 84,375Gbps / 8 =10,54 GBps
VELOCIDADES MEDIOS
Redes cableadas
FastEthernet: 100Mbps
Gigabit Ethernet: 1Gbps
10GB Ethernet: 10Gbps

Redes inalambrica
802.11 a/b/g/h/ac/ax
Bluetooth 3.0 4.0 5.0






Par paralelo: Categoría 1 conector rj-11 con 4 cuchillas pero solo se utilizan 2



El cableado vertical  o backbone es el cableado que conecta las plantas




NIVEL ENLACES
Los switches se pueden componer de de 24, 48 bocas y estos tienen precios muy parejos casi siempre, con ellos se pueden crear una red local pequeña de no más de 48 nodos por switch, de forma que si quiero más nodos necesito varios switches, por ejemplo



Crear una red de 90 ordenadores, para ello conecto 45 ordenadores a cada switch y +1 boca para interconectar los switches 




En el caso anterior si los switches y el los cables trabajan en 1Gb, todas las maquinas de un mismo switch si se pueden comunicar a 1Gb por segundo pero si varias maquinas de un switch se quieren comunicar con otras del otro switch el cable que conecta ambos switch debe de repartir el ancho de vanda en caso de dos maquinas de switch a para 2 maquinas de switch b el ancho de banda será de 512 Mbps y en disminución en caso de que haya más conexiones



Ahora queremos salir a internet y conectamos un router al switch a




Después de este cambio los ordenadores del switch a tendrán más ancho de banda que los del switch b




En vez de 90 ordenadores 200 ordenadores




Necesito 5 switches y los voy a conectar en cascada, 40 ordenadores en cada switch y un switch conectado a otro, esto no esta permitido ya que como máximo se pueden tener 2 niveles en cascada y no 5 ya que en el peor de los casos es decir los 200 ordenadores queriendo salir a internet
swich a (41 bocas usadas): Hay que dividir el ando de banda entre las bocas 1024 / 41 = 25Mbps
switch b (41 bocas para 25 Mbps disponible): Hay que dividir 25Mbsp entre otras 41 bocas 25/41= 0,6Mbps
switch c (41 bocas para 0,6Mbps disponible): Hay que dividir 600Kbps/41=15Kbps
switch d (41 bocas para 15Kbps): 15/41=400bps
switch e (41 bocas pra 400bps): 400/41=10bps




Por estos casos no se pueden poner más de 2 niveles ya que con 10 bps no se puede hacer prácticamente nada





También podemos tener más problemas debido a tener más swiches, si estos están en un lugar inadecuado al alcance de personas no autorizadas, estos pueden llegar a crear una tormenta de broadcast conectadon un switch a otro switch en ambos extremos por ejemplo switch_a_boca_1 con switch_b_boca_1 y lo mismo con la poca 2 de ambos este caso puede crear un bucle y saturar el ancho de banda hasta tirar la red





Lo normal para evitar los altos niveles en cascadas, se recomiendan switches de cabeceras, este switch no va a tener ninguna máquina conectada a este más que los servidores, routers, AP y los demás switches.
Con este método se evita la jerarquía y todos los switches conectados al de cabecera tienen la misma capacidad de ancho de banda.



 
Si queremos la red de 200 máquinas en la imagen anterior para hacerlo bien necesitaremos un switch de segundo nivel más, para hacer bien



Port Bonding(general)/Trunking(CISCO)/Link Aggregation: Procesos por el que se utilizan para utilizar 2 conexiones como si fueran uno doblando el ancho de banda de las conexiones (no es el doble ya que surge tráfico para vincular los cables pero casi el doble). En la imagen anterior puedo hacer un bonding de 2 bocas en cada switch ya que el de cabecera tiene libre muchas bocas, con esto la conexion parasará de 1Gbps a 2Gbps practicamente
Ventajas: Más ancho de banda, normalmente bonding de 2,4,8
Desventajas: Menos bocas





En un servidor se pueden agregar tarjetas de red y hacer tambien bonding



***IMPORTANTE NO TENER CUELLOS DE BOTELLAS YA QUE TODA LA INFRAESTRUCTURA SE ADAPTA A LA VELOCIDAD MÍNIMA***



Otra opción es utilizar switch que cuentan con bocas de fibra por lo que no haria falta poner bonding por las bocas normales de switch utilizando estas bocas ya se podría utilizar 10Gbps estos switches se identifican (48 + 2 / 48+4)





Otras opciones son los switches apilables, estos switches se caracterizan por tener en la parte trasera dos puertos denominados stack in /stack out ó stack up / stack down. Estos puertos en función del fabricante tienen un formato u otro, la cantidad de switches que se pueden apilar también dependen del fabricante normalmente 8 
Se conectan cada in en el out del siguiente y el último in en el out del primero



Estos cables suelen ser de fibra o llamados fiberchannel que pueden ir entre 40-80 Gbps



A efectos practicos es como tener un unico switch




Otra opción es utilizar un Blade switch o switch modular este switch se le van añadiendo las ranuras de las bocas o modulos, parecido a un rack o los discos duros de los servidores, estos dispositivos tambien traen un software para configurarlo
Ventajas: Los switches estan conectados todos a una placa base por lo que será el mismo
Desventajas: Muy caros





*BARGAIN HARDWARE web con maquinas reacondicionadas *





CARACTERÍSTICAS AL COMPRAR SWITCH
PoE: Power over Ethernet: alimentación por ethernet, utilizando un cable utp se puede alimentar al switch por 2 hilos 
2x1100W: Indica 2 fuentes de alimentación 
Managed switch: Switch gestionable para poder realizar ciertas configuraciones





El protocolo de spanning tree Algorithm o Planning tree protocol es un protocolo encargado de anular los bucles para evitar las tormentas de broadcast (SPA/SPN/STP)


REDES VIRTUAL (VLANS)
Solo en switches gestionados (managed switch/ smart switch), en estos switches se pueden hacer port bonding, port mirroring, quality of service (qos).
Algunos switches tienen características de nivel 3 es decir de nivel de red
	VLANS
Permiten dividir la red local en redes virtuales, es decir puertos a-b primera red virtual y de c-d otra. Con esto se separan las máquinas y estas no tienen conexión
VLANS asimétricas: Estas VLANS son las que cuentan con puertos que pertenecen a varias VLANS




Tengo 4 switches, cada switch en un aula, menos uno de cabezera. El de cabezera tiene tres bocas para 3 servidores y una boca para el router. Los switches estan conectados al de cabecera con un bonding de 2 bocas.



Primer switch las trentan máquinas (3-32) de 1º grado medio y 15 de 2º SMR
Segundo de switch (3-12) 2º SNR  15 1º de asir y las ultimas 4 bocas 2º asir
Tercer switch (3-7), 2º asir y el resto de bocas libres




 
Tapped/Untapped ports: Un puerto etiquetado es aquel que añade una cabecera a los mensajes para indicar a qué vlan pertenece (802.1q), con esto se distinguen las vlans independientemente si la información va a otro switch. Todas las bocas que conectan otros switches hay que etiquetarlos.



Puerto de monitorización/espejo/port mirroring: Puerto que reenvía todo el tráfico que va por todas las bocas,  a una boca concreta a la que se conecta una máquina que analiza el tráfico. Normalmente se miran las estadísticas de switch antes que poner una máquina con wireshark ya que se ven las estadísticas del tráfico. A Veces las estadísticas de tráfico no muestran algo concluyente y entonces si conectamos la máquina con wireshark.



Hay switches que son capaces de decirte la velocidad de las conexiones, y la distancia del fallo 



Para saber a que boca de switch está conectada una máquina, normalmente se mira las etiquetas que se asigna a la roseta que te indica el patch panel armario y puerto.



En el diseño de la infraestructura, la cantidad de armarios y switches se debe de ampliar un 30% mas del uso total que se tiene previsto



QoS: Se centra en priorizar una cosa u otra a nivel general de informatica, en el caso de redes con los switch, le puedo dar prioridad a una boca sobre otra de forma que primero atiende el trafico de las bocas prioritarias antes que las de los demás, tambien sobre un tipo de trafico por ejemplo el trafico http o el trafico con destino dropbox tiene menos prioridad que otro 




ESPECIFICACIONES DE CISCO
Puertos access: Puertos en el que se espera conectar una maquina corriente
Puertos trunk: Puertos que se espera conectorizar otros switches
Port channel: Utilizar varias bocas para conectorizar similar a los port bonding de otros routers como los D-Link



 NAT



SNAT: Se cambia la ip de origen con la ip publica del router u otra IP. En caso de que los puertos de ambas maquinas coinciden, se realiza PAT que es la sustitución de los puertos en el trafico por parte del router
DNAT: Se cambia la ip de destino, nos permite que en un equipo externo a nuestra red pueda acceder a los servidores de mi red local.





El cliente al salir hace SNAT al recibirlo el router del servidor se hace DNAT, la respuesta generada por el servidor debe de hacer SNAT ya que la respuesta parte con la ip privada de la maquina y no la publica del router y finalmente se deshace el SNAT original porque que la petición contaba con la IP de origen publica y la respuesta tiene como destino la IP publica tambien por lo que el router deshace el SNAT



SNAT
REGLAS
up …….. Cuando se levante la interfaz se ejecutan las regla de iptables 
up iptables -t nat -A POSTROUTING -s IP_RED_LOCAL -o INTERFAZ_IP_PUBLICA -j SNAT –to IP_PUBLICA



down ……. Cuando se va a bajar la interfaz
down iptables -t nat -D POSTROUTING -s IP_RED_LOCAL -o INTERFAZ_IP_PUBLICA -j SNAT –to IP_PUBLICA
-t: Tabla
-A: Añadir cadena
-D: Eliminar cadena
-o: Interfaz de salida (output)
-j: Acción que vamos a hacer (SNAT, DNAT, MASQUERADE)
- -to: A que IP se va a traducir (solo en snat y dnat)





En la tabla NAT hay 2 cadenas
POSTROUTING: Después de haber tomado una decisión de enrutamiento, SNAT es siempre o casi siempre POSTROUTING ya que no es posible hacerlo hasta que no sepa que interfaz de salida va a utilizar por lo que primero se mira/realiza el enrutamiento y despues se aplica la regla
PREROUTING




En caso de tener una IP publica dinamica se utiliza la orden MASQUERADE



down iptables -t nat -D POSTROUTING -s IP_RED_LOCAL -o INTERFAZ_IP_PUBLICA -j MASQUERADE



DNAT
–p: Protocolo
- -dport:
-i: interfaz(input)

up iptables -t nat -A PREROUTING -p tcp –dport 80 -i eth0 -j DNAT - -to IP_privada




SNAT CISCO
En cisco hay que permitir con una ACL con las IPs que tienen permitidas realizar SNAT



(config)access-list nºacl permit ip wildcard
(config)ip nat pool IP_PUBLICA 









CORTAFUEGOS
Con un cortafuegos podemos permitir analizar el trafico de red al atravesar un dispositivo y tomar decisiones acerca del mismos
permitir el paso
denegar el paso silenciosamente o no
modificar el trafico
seleccionar determinado trafico para otra aplicación

Se usa por seguridad para controlar o modificar el trafico de la red




Los cortafuegos se pueden poner de 2 formas



NODO
Un cortafuego de nodo protege un solo equipo, normalmente un servidor, es muy laborioso cuando se tiene muchos servidores, pero cuenta con ventajas de protección tanto para ataques externos e internos



PERIMETRAL
Un cortafuegos que se coloca entre el router y el switch o en caso de ser software el propio router lo tiene integrado, los cortafuegos hardwares son más veloces a la hora de procesar el tráfico



DMZ
una zona desmilitarizada es una zona de mi red que permite cierto acceso a internet, para esto se utiliza un cortafuegos de 3 patas donde el cortafuego dependiendo de que a que maquina se dirige el trafico se aplica ciertas reglas u otras
 






Dentro de la tabla filter hat 3 cadenas
INPUT
OUTPUT
FORWARD




Para establecer una politica por defecto
iptables [-t tabla] -P cadena ACCEPT | DROP
-P: Policy, politica




Por cada cadena hay que establecer una política por defecto



iptables [-t tabla] -L [cadena] -n -v
Lista las reglas



iptables -A [cadena] -p protocolo -s ip_origen/red -d ip destino -i interfaz interda -o interfaz salida -j accept|drop



-j: Accion a realizar si acepta o dropear 
-p: Indicamos el protocolo, si se especifica tcp se permite utilizar
- -dport: puerto de destino
- -sport puerto de origen

-s: ip origen
-d: ip destino
-i: interfaz entrada
-o: interfaz de salida




- - state 




Los parametros con un - son basicas mientras -- indica parametros avanzados por lo que hay que cargar el modulo -m



-j REJECT rechazo confirmado similar a DROP pero este no confirma



iptables cuentas con muchos modulos y casi siempre hay que cargarlos -p protocolo -m protocolo --parametro_modulo en el caso de el modulo TCPy UDP ES DE LOS POCOS QUE SE CARGAN POR DEFECTO



MODULOS IPTABLES
addrtype: Sirve para cargar el tipo de dirección IP especifica como puede ser unicast multicast broadcast
-m addrtype -- {dst|src}-type broadcast
comment: Sirve para poner comentarios en el propio comando de ejecucion
-m comment –comment “Primero cargamos el modulo y utilizamos el parametro comment”
connlimit: Limita el numero de conexiones paralelas desde un mismo cliente
-m connlimit --connlimitº-above 3 
icmp: Utilizamos el protocolo ICMP
-m icmp –icmp-type echo -request
conntrack
–state 
iprange: indicamos un rango de ips
-m iprange
mac: Modulo para trabajar con macs
-m mac --mac-source || --mac-destination
multipor: Permite establecer un rango de puertos
time: Definimos un tiempo
-m time –timestart 13:30 --timestop 14:30 --weekdays




COMANDOS
hping3: Sirve para generar tramas personalizadas
telnet: sirve para comprobar si un puerto esta activo 
nmap: Siver para hacer un “mapa de la red” y conocer los servicios disponibles a demás de realizar ciertos ataques 





ENCAMINAMIENTO DINÁMICO
Se le asigna un valor de “coste”  a las rutas escogiendo la de costes mas “baratos”, sin importar el tiempo o la optimización de saltos de routers, este metodo es normal para las compañías de teleco que miran por los costes más baratos



Cada router pregunta a sus vecinos a donde saben llegar y qué coste tienen, a partir de aqui realiza las tablas de enrutamiento 



Utilización de algoritmo de DISTRAC 



Hay varios protocolos de encaminamiento dinámico pero ambos cuentan las siguientes características comunes
Minimizar el tamaño de las tablas de encaminamiento
Minimizar el número de mensajes de control a intercambiar
Generar rutas correctas, optimas en coste y uso del ancho de banda disponible sin discriminar a ningún nodo
Modificar las rutas en rapidamente en caso de fallos en alguna ruta o de cambios en las condiciones del tráfico 
Ser escalable, es decir que no se vuelva inviable cuando la red crezca, dicho de otra forma 




Los costes se pueden calcular en función de algo, como puede ser el ancho de banda, latencia, coste económico, número de saltos…



PROTOCOLOS DE VECTOR DE DISTANCIA
Son muy ligeros en el consumo de recursos, pero en las averías tardan en comunicarse y es posible que ciertos routers se queden sin saber que hay una averia (PROTOCOLO RIP) 





Usa UDP 

PROTOCOLO DE ESTADO DE ENLACE
Las averias se propagan rapido, se pueden combinar varios parametros para calcular el coste y a tiempo real
Permiten obtener rutas alternativas para un mismo destino
Cada nodo tiene información de toda la estructura del resto de la red y calcula por si mismo su tabla de enrutamiento

Desventajas
Algoritmos complejos
Requiere almacenar en cada nodo una gra cantidad de información
Los mensajes que intercambia los routers pueden 

OSPF – IS-IS
