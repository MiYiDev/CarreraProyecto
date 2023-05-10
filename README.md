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

Muestra la herramienta METASPLOIT, con la que podremos hacer uso de los diferentes xploits, payloads, etc... Una vez visto esto, pasamos a práctica de METASPLOIT (capturas adjuntas).

Muestra las diferentes fases en las que usaremos Metasploit. Trata sobre el "fingerprinting", es decir, saber en que sistema operativo se está lanzando el host. Además, explica que es un "backdoor". Esto es, ejecutar un script remoto a la máquina de la victima.

Explica que, para atacar Windows (sistemas antiguos), usaremos Msfvenom, herramienta que permite crear un exploit para ejecutar una conexión reversa entre la victima y el atacante, y un multi-handler.

En el caso de atacar Linux, primeramente se debe de realizar un escaneo de los puertos para ver qué servicio está corriendo en la maquina a la que vamos a atacar, y después, ver las vulnerabilidades que tienen los puertos de la máquina.


-PYTHON PARA PENTESTING

Muestra diferentes librerias para la creación de scripts, como DNS Python, Python-Twitter, PyGeoIP, etc... y el uso de cada una de ellas.