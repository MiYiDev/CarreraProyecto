# CarreraProyecto

Dia 1: Realizado Análisis forense básico en sistemas Windows y Análisis forense avanzado en sistemas Windows (este último sin probar demasiado la herramienta Volatility porque no me lo permite mi PC (se crashea)).

Tras un parón por problemas en el PC de casa:

17/04/2023: Realizado forense básico en sistemas Linux.

01/05/2023: Realizado forense avanzado en sistemas Linux.

06/05/2023: Comiendo con el curso de OSINT. Comienza explicando los términos de "Inteligencia" y "Ciberinteligencia", las diferente disciplinas que hay (ej: OSINT(inteligencia en fuentes abiertas) o CYBINT (inteligencia en el ciberespacio)), el ciclo de la inteligencia y la problemática que hay por el exceso de información que tenemos hoy en día que hace dudar sobre la fiabilidad y credibilidad de la misma. Por último dentro del apartado de "OSINT", habla sobre el factor humano y de lo importante que es saber diferenciar entre el uso de herramientas para acompañar la tarea y la capacidad que tienen los analistas, ya que una herramienta no puede sustituir las capacidades de una persona analista en poder descartar ciertos casos o diferenciar.

En el apartado de "Hacking con buscadores", comienza explicando las diferentes herramientas que Google proporciona para poder hacer búsquedas avanzadas o personalizadas dependiendo de cual sea nuestro fin. Continúa mostrando los diferentes motores de búsqueda que podemos usar y las ventajas de cada uno y el hecho de poder usar motores de búsqueda específicos de cada lugar o país para poder tener resultados más específicos geograficamente hablando. También vemos la opción de búsqueda de imagenes para poder así encontrar suplantación de marca, fake news o simplemente imagenes visualmente similares a una que nosotros busquemos y buscadores tecnológicos para poder encontrar tecnologías vulnerables en diferentes sitios web que busquemos. Más adelante, explica lo que serían las diferentes "capas" de internet (surface, deep y dark web) y como poder acceder a estas últimas con navegadores que lo permitan como Tor. Por último en este apartado, propone un "reto" que trata de un tweet utilizando como fuente una imagen que, buscandola en Google Imagenes se encuentra que es de otra época totalmente anterior a la fecha del tweet.

Apartado de METADATOS:

Comienza explicando que son los metadatos, que no dejan de ser datos acerca de otros datos, por ejemplo, en el caso de una fotografía, datos acerca del fabricante del modelo de la lente, lugar, fecha...

08/05/2023: Muestra el programa "ExifTool" que sirve para ver los metadatos de diferentes ficheros. También muestra el programa "FOCA", de ElevenPaths, para poder ver los metadatos de páginas web (a mí particularmente no me deja ejecutarlo, captura adjunta). Lo que sí que pude hacer fue el reto que propuso, siendo este averiguar de que fecha es un documento de un exconsejal de la comunidad de Madrid que dice haberlo hecho público el día que se creó. (Captura adjunta).

El apartado de "Herramientas", se me hace imposible seguirla, pues el enlace de descarga del buscador que proporciona en el curso ya no está disponible y otros enlaces que encontre, algunos contienen Malware y otro se descarga a 300kb hasta que se para por completo, por lo que paso directamente al siguiente apartado de "Herramientas de Monitorización".

<b>"Herramientas de Monitorización"</b>

Vemos y analizamos el uso de herramientas como TweetDeck (captura adjunta) o Twitonomy para analizar desde perfiles de twitter hasta hashtags... etc.

La siguiente sección trata sobre las alertas de google (Google Alerts), con las que podemos programar alertas para que nos avise cada vez que aparece algo nuevo relacionado con la búsqueda que hayamos elegido como filtro.

<b>"Privacidad y Anonimato"</b>

Aquí vemos diferentes herramientas que podemos usar para poder hacernos identidades anónimas digitales, utilizando por ejemplo "FakeNameGenerator" para poder crear un perfil de una persona falso, así como la creación de E-Mails temporables o desechables con, por ejemplo, "ProtonMail".

También muestra como podemos enmascarar nuestra propia identidad, como realizando las investigaciones en máquinas virtuales para así poder borrar nuestras huellas fácilmente borrando la máquina o llevando nuestras herramientas en un USB propio, además de ocultar la IP de diferentes formas (proxy, vpn...), un gestor de contraseñas...

09/05/2023:

<b>"Herramientas avanzadas para búsqueda OSINT"</b>

Después de explicar por encima en que se basa el OSINT, muestra las fases del proceso que se debe llevar a cabo, como establecer objetivos.

Muestra los diferentes buscadores que podemos usar, distribuciones de linux preparados para OSINT, herramientas para obtener datos con emails, herramientas para geolocalizar tweets, ips...

En general, la primera parte del taller muestra herramientas para obtener información sobre diferentes plataformas o elementos, como Instagram, Twitter, Emails...

(Aquí me doy cuenta de que hay un gran problema (en esta carrera al menos) sobre informar del software que se va a utilizar en los talleres o cursos, ya que siempre que se utiliza alguna distribución diferente de Linux o algun software específico me entero en el momento que lo abre y tengo que parar todo para poder instalarmelo y entonces poder continuar...)

En este punto decido no continuar con este taller de forma práctica ya que hace uso de herramientas que piden previo registro con teléfono movil y, tras comentarlo con el profesor, decido no hacerlo.

De forma teorica, básicamente trata diferentes formas de buscar brechas de seguridad, información sobre personas, sus pertenencias digitales... En general datos sobre las personas para poder sacar algún beneficio con dicha información. Sería algo asi como ir tirando del hilo para sacar cada vez más sobre alguien. Desde su posible locaclización gracias a su correo electrónico, hasta si posee bitcoins o está presente en alguna asociación, entre otras muchas cosas.

10/05/2023:

<b>"HACKING WEB"</b>

Al inicio del curso, básicamente, explica que es el Hacking y sobre que plataformas se puede aplicar.

-SQL INJECTION: Primera vulnerabilidad que muestra. Esto es, mediante sentencias SQL, poder, por ejemplo, saltarnos inicios de sesión (poner en un inicio de sesión, de usuario "999" or "1" = "1" --   y de contraseña  "password1"), haciendo asi, que la posible consulta a la base de datos fuera "select * from users where user = "999" or "1" = "1" --" and password = "password1". De este modo, la parte derecha del --" quedaría comentada y, puesto que "1" = "1" es siempre true, podremos acceder. Otro posible objetivo del SQL INJECTION sería la obtención de datos que nos interesasen.

-XSS (Cross-Site Scripting): Otro tipo de inyección de código. Trata de ejecutar una parte de script para poder obtener, por ejemplo, datos sobre la tabla de la base de datos. De esta vulnerabilidad hay dos tipos: XSS almacenado, donde inyectas codigo que se almacena en la base de datos para que se cargue más adelante cuando se acceda a la base de datos, y XSS Reflejado, donde, a diferencia del almacenado, no se envía la inyección a la base de datos, sino que se queda en el código de la página web. Es una vulnerabilidad algo más potente ya que, utilizando, por ejemplo, window.location en el script, y consiguiendo la cookie, puedes llegar a conseguir hacer robos de sesiones, phishing...

-Unrestricted File Upload (vulnerabilidad sobre tratado de ficheros): Consiste en insertar un fichero a alguna página web que permitan la subida de ficheros (por ejemplo, una página que pida subir un pdf de tu CV). 

-Local File Inclusion: Cargar algún fichero interno de la aplicación web modificando la ruta del fichero al que debería acceder normalmente, pudiendo así acceder a ficheros que nos interesen como passwd en linux.


Robo de sesiones:

-Session Prediction: El session prediction trata de poder acceder a la sesión de otro usuario intentando adivinar su ID de sesión siguiendo la estructura de nuestro id. 

-Fuerza bruta: Intentar averiguar una contraseña según combinaciones, contraseñas comunes...  

Accesos ilegales:

-Parameter tampering: Trata de modificar el valor de un parámetro para poder obtener algún dato beneficioso para nosotros.

-Control inseguro de roles: Conseguir opciones que tienen usuarios con otros permisos que nosotros no, pudiendo acceder así a opciones de administración, por ejemplo.


<b>"CURSO DE HACKING TOOLS: BLUE TEAM"</b>

-LINUX 100%: 

Primer video de "Usuarios, grupos y permisos" me lo "salto", pues es algo de lo que ya adquirimos conocimientos en primero de DAM con David en Sistemas Informáticos. Paso directamente a "Accesos remotos".

En "Accesos remotos", explica el uso que vamos a hacer de SSH, que permite el acceso remoto, y las ventajas que tiene este sobre otros protocolos como "telnet". Además, tambien trata VNC, con el que también nos podremos conectar al equipo remotamente.

En "Squid", un servidor situado entre la máquina del usuario y otra red (proxy-caché), cuenta que sirve para poder permitir el acceso web a maquinas privadas, controlar el acceso web aplicando reglas, controlar el contenido web visitado y descargado, registrar logs de las peticiones, etc... Además, nombra sus ventajas, como servir de cortafuegos y cuenta su instalación, mediante apt-get.

"IpTables": Conocido como "el cortafuegos de kernel", permiten tener control total sobre sistemas linux. Pueden ser de IPv4 y de IPv6. Explica el Filter table, que sirve para filtrar los paquetes, el Nat table, que es la tabla de traducción de direcciones de red y el Mangle table, que ajusta las opciones de los paquetes. Muestra además, las reglas, los comandos y diferentes ejemplos de aceptar peticiones, abrir puerto para un servidor web, etc...

-METASPLOIT 100%:

Muestra la herramienta METASPLOIT, con la que podremos hacer uso de los diferentes xploits, payloads, etc... Una vez visto esto, pasamos a práctica de METASPLOIT guiada. (no cuento con entornos seguros para seguir esta práctica guiada, por lo que me limito a seguir el video).

Muestra las diferentes fases en las que usaremos Metasploit. Trata sobre el "fingerprinting", es decir, saber en que sistema operativo se está lanzando el host. Además, explica que es un "backdoor". Esto es, ejecutar un script remoto a la máquina de la victima.

Explica que, para atacar Windows (sistemas antiguos), usaremos Msfvenom, herramienta que permite crear un exploit para ejecutar una conexión reversa entre la victima y el atacante, y un multi-handler.

En el caso de atacar Linux, primeramente se debe de realizar un escaneo de los puertos para ver qué servicio está corriendo en la maquina a la que vamos a atacar, y después, ver las vulnerabilidades que tienen los puertos de la máquina.


-PYTHON PARA PENTESTING

Muestra diferentes librerias para la creación de scripts, como DNS Python, Python-Twitter, PyGeoIP, etc... y el uso de cada una de ellas.

Realizamos el primer script para obtener información del dominio de openwebinars. (captura)

<b>SCAPY</b>

Permite enviar, falsificar y diseccionar paquetes de red. 

<b>BEAUTIFULSOUP</b>

Biblioteca de Python para analizar documentos HTML. Util para web Scrapping.



"RED TEAM"

Empieza tratando un poco por encima inyección SQL, fuerza bruta, XSS, inyección de codigo, phishing... básicamente cosas que ya hemos visto anteriormente en la carrera, por ello no muestro gran cosa sobre esto.

<b>HACKING INFRAESTRUCTURAS</b>

"Buscando objetivos con Shodan y ZoomEye": Shodan y ZoomEye son motores de búsqueda. En el caso de Shodan, busca servicios para encontrar vulnerabilidades en ellos. En caos de ZoomEye, que es más potente que Shodan, indexa una vez por semana (shodan lo hace 1 vez por mes) y es capaz de buscar direcciones IP públicas que tengan en internet un servicio.

"Google Dorks": Como en la primera parte de Red Team, esto es algo que ya se ha visto anteriormente en la carrera por lo que, no voy a añadir gran parte de este apartado aquí. Basicamente explica y da ejemplos del uso de Google Dorks para encontrar información.

"Man in the Middle": Como atacante, entras en el trafico de datos de 2 partes, para recibir los datos en vez de que los reciba la otra parte, haciendote pasar por ella. Hay diferentes tipos de ataques MitM (ARP caché poisoning, basado en servidores DNS, simulación de punto de acceso inalámbrico...) pero, básicamente son diferentes formas de poder entrar en el medio de una comunicación para capturar los datos cuando se están enviando, ya sea haciendote pasar por una red WiFi, instalando malware en los navegadores de las victimas, etc...

"Cracking WIFI": Básicamente, conseguir la WiFi de alguna forma, por ejemplo, con fuerza bruta. 

"INFORMATICA FORENSE"

Básicamente, como en los primeros talleres de la carrera, vamos a ver como obtener evidencias, contrastarlas, etc.. para obtener información. 

<b>Fases de la metodología forense<b>

    1.- Asegurar la escena: Asegurarse de que la escena no ha sido modificada a la hora de obtener datos e información.
    2.- Recolección de evidencias: Debido a la volatilidad de los datos, se debe de recoletar de forma ordenada y rápida las pruebas más volátiles. Por ejemplo, como primeros datos, deberíamos de obtener los registros y contenidos de la memoria caché, y de último, los documentos. (por poner un ejemplo). El RFC 3227 es un documento que recoge las directrices para la recopilación de datos, es decir, establece como un "estandar".
    Por último, analizaríamos esas evidencias.

<b>Volcados de memoria<b>
    
    Esto es, una instantánea del estado interno de un programa. Una vez más, esto es algo que ya vimos a principios de la carrera, por lo que no incluiré mucha información sobre esto en este apartado.

<b>Heramientas<b>
    NMAP: Comenzamos con el uso de nmap. (capturas adjuntas)
    WIRESHARK: De nuevo, capturas adjuntas de su utilización.
    VOLATILITY: Herramienta usada a inicios de la carrera y, de nuevo, me es imposible usarlo.
    DUMPIT: Lo mismo que Volatility.
    AUTOPSY: Esta herramienta se trata de un conjunto de herramientas útiles para el análisis forense. Analiza el registro del S.O., saca datos EXIF de imágenes, etc...

"METASPLOIT PARA PENTESTING"

Inicialmente, explica que es Metasploit (algo que, de nuevo, ya hemos visto en dos ocasiones a lo largo de la carrera), como iniciarlo, actualizar la herramienta, el uso de filtros como RHOSTS, LHOST (localhost), cargar exploits, payloads...

Posteriormente, realiza un ejemplo práctico de realizar una taque con Metasploit, al igual que en otras ocasiones en la carrera, básicamente, sobre un entorno controlado, realiza un analisis con nmap de los puertos que está usando para encontrar vulnerabilidades y exploits potencialmente peligrosos. Una vez encontrado el exploit y rellenados los filtros necesarios (RHOST y LHOST), lo lanza y carga un payload para acceder. Una vez accede, navega por la consola de la máquina atacada para entrar en ficheros como Passwd.

"AUTOPSY: Recuperación de Datos"

Último taller de la carrera. De nuevo, herramienta que ya hemos visto anteriormente... Muestra como instalarlo y las funcionalidades que tiene, como por ejemplo, analizar el registro del S.O., sacar datos EXIF de imágenes... pero esto es algo que ya he explicado.

A mayores que lo visto anteriormente, enseña como hacer un hash lookup para hashear los ficheros que analicemos, explora archivos de ejemplo para ver metadatos que proporciona y la opción de recuperarlos.



Acabado el taller de Autopsy, queda finalizada la carrera de Hacking Ético. En mi opinión, considero que es una carrera muy útil e interesante pero, lo falla todo la forma en la que está hecha. Considero que las personas encargadas de llevar a cabo los diferentes cursos y talleres de esta carrera, aunque son muy profesionales y, evidentemente, tienen muchos conocimientos acerca de este tema, no creo que se desenvuelvan bien a la hora de explicar y enseñar a otra gente. Bajo mi punto de vista, no sólo es poco dinámica, sino que además se hace pesada y larga (a pesar de su corta duración), pues, salvandose un poco el profesor Francisco Carcaño, encargado de la parte de OSINT, tanto Carlos Lucena (encargado de la parte de testing) como Jordi Ubach (profesor que más "encargado" está en enseñar en esta carrera, pues es el que más aparece), hablan muy lento (he necesitado poner los videos en, como poco, x1.5 de velocidad), sino que además no explican muy bien o de forma clara los temas que se tratan. 

Dejando este tema a un lado, también considero que se da poca información con "valor". Utilizando la palabra "valor" me refiero a, información o aprendizaje realmente interesante que te puede dar un curso online y no tanto así tu propia búsqueda por internet. Yo, como persona que le gusta el tema de la ciberseguridad, en pocos días aprendiendo usando la plataforma HackTheBox hace un año, aprendí y utilicé más sobre, por ejemplo, nmap, Metasploit o SQL Injection, que las aproximadamente tres horas que se tratan esas herramientas en la carrera.

Otro tema que considero que no está bien pensado es, el previo aviso sobre las herramientas que se van a utilizar en los talleres o cursos. Cuando se toca Kali Linux, no sólo no explican previamente que debes de tener preparada una máquina con Kali (te enteras una vez la abren ellos...), sino que además no se paran a explicarte el por qué vas a utilizar una distribución como Kali ni explican la existencia de otras más potentes y avanzadas como Arch. Considero que, puestos a enseñar, enseñémos de verdad y expliquemos el por qué de las cosas y la utilidad que tienen.

Como algo más que añadir, también me gustaria comentar que en ciertas cosas que se dicen no estoy muy de acuerdo. En la parte de Hacking Web, empiezan explicando una "estructura(?)" de internet, donde, al parecer, hay como 3 segmentos bien diferenciados y marcados con porcentajes sobre las diferentes capas que hay. Da una explicación de Dark Web y Deep Web que, más que la realidad, parece que afirma los tópicos que se dicen sobre la Dark Weeb de que es la parte criminal irrastreable de internet y utilizada por grandes criminales y ni mucho menos, por no hablar de que lo de internet es un 3% lo que vemos y el resto información turbia y oscura lo recuerdo yo de cuando era un niño pequeño y me empezaba a informar sobre las capas que tiene internet... (porcentajes inventados por mi porque no recuerdo los dichos por el profesor... pero tanto no se alejaban.)

Repito, esto anteriormente dicho es bajo mi punto de vista y mi opinión completamente subjetiva. Dicho esto, mi conclusión para esta carrera es: un tema que puede ser muy interesante y muy útil pero, con grandes sombras en términos de explicación e información dada y, sobretodo, dinamismo.




