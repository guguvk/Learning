# Comandos básicos
- `cd` **Cambiar** de **directorio** `cd Directorio_al_que_se_accedera` y si haces tal cual `cd` **te lleva** al **PATH** del **usuario**
- `cd..` **Retroceder** un **directorio**. **Si estamos** en `/home/gugu/a/b/c` y **hacemos** `cd ../..` **cambiamos** a `/home/gugu/a` (retrocedemos 2 directorios "`../`" hace **referencia** a **1 directorio**)
- `mkdir` **Crear** un **directorio** `mkdir Directorio_a_crear`
- `rm` **Eliminar directorio** `rm Directorio_a_eliminar`
- `mv` **Mover archivos** o **carpetas** de **lugar** `mv archivo_que_se_movera lugar_a_donde_se_movera`
- `mv` **Renombrar archivos** o **carpetas** `mv carpeta_que_se_renombrara nuevo_nombre_de_carpeta`
- `cp` **Copia archivos** o **carpetas** `archivo_que_se_copiara lugar_donde_se_copiara` "lugar_donde_se_copiara" (es **carpeta** o **ruta absoluta** "`/esto/es/la/ruta/absoluta`")
- `clear` **Limpiar** la **pantalla** (**quitar todo** lo que se **mostraba** y lo **anterior**)
- `ls` **Listar** lo que **hay** en el **directorio actual**, `ls -l` **Listar** lo que **hay** y ver mas **informacion** (permisos, usuario propietario, grupo, tamaño y si es un enlace simbolico)**
- `cat` **Visualizar** lo que **tiene dentro** de un **archivo** (**sin necesidad de abrirlo**)
- `touch` **crea** un **archivo** (**sin necesidad** de **abrir** y **volver** a **guardar**)
- `grep` **Extraer texto** de un **archivo** (**puede** estar **dentro** de un **archivo directamente** o en un **archivo dentro** de una **carpeta**)
- `pwd` **Te muestra** la **ruta actual** donde estas **ubicado**
- `whoami` **Te muestra** el **usuario actual** (**el** que estas **usando**)
- `id` **Muestra información** sobre la **identidad** de un **usuario** y los **grupos** a los que **pertenece**
- `*` **Se** refiere a **0** o **mas** (**basicamente**, **todo**)
- `>` **Redirige** la **salida** de un **comando** a otro **comando** o a un **archivo**
- `<` **Hace** la **entrada** de una **cadena** a un **comando**

# Conceptos basicos
- **Que** es un **HoneyPot**?  R= **Estado** o **situación** complejamente **extraño** o **difícil**
- **Que** es **estar** en **escucha**?  R= **Estar esperando** una **conexión**
- **Que** es el **fuzzing**?  R= **Buscar directorios ocultos** mediante **Fuerza Bruta**
- **Que** es un **exploit**?  R= **código** o **programa malicioso diseñado** para **aprovechar vulnerabilidades** en un **sistema**
- **Que** es **openvpn**?  R= **Programa** con el cual **enlazaremos** nuestra **ip** para poder tener **conexion** con las **maquinas**
- **En linux importan** las **extensiones**?  R= **Realmente NO**
- **Que** es el **passwd**?  R= **El archivo** donde se **encuentran** los **usuario** del **sistema**
- **Que** es el **shadow**?  R= **El archivo** donde se **guardan** las **contraseñas** del los **usuarios**
- **Que** es **PoC**?  R= **validación preliminar** de que un **método** es **viable**
- **Que** es **rustscan**?  R= **Herramienta** que **escanea puertos** (corre por detras **Nmap**)
- **Que** es **nmap**?  R= **Herramienta** que **escanea puertos**
- **Cuantos puertos existen**?  R= **65,535**
- **Que** es **dirsearch**?  R= **Herramienta** que realiza **búsquedas** de **fuerza bruta** en **directorios web**
- **Al entrar** a una **pagina web** que debemos **buscar**?  R= **Formularios**, **Directorios ocultos**, **HTML (Credenciales)**, **Servicio**, **Version**, **Base de datos**
- **Que** es **Netcat**?  R= **Herramienta** de **administracion remota**
- **Que** es una **tty**?  R= **La comunicación** entre los **dispositivos** de **terminal** y los **programas** que los **leen**
- **Por que** exportar las **variables SHELL** y **TERM**?  R= **Porque** si no se **exportan**, **no** seria una **terminal 100% funcional** y **podria** dar **problemas** con algunos **comandos**
-  **Al** hacer **sudo -l** si arroja **información** que **significa** "**(ALL : ALL) NOPASSWD: "Binario/script"**" **ALL** -> **Cualquier usuario**  **ALL** -> **Cualquier grupo**  **NOPASSWD** -> **No** te **pedira contraseña**  **"Binario/script"** -> **El** que **puedes ejecutar** con **sudo**

# Permisos
- Se dividen en **3**
- Se veran de la siguiente manera
```
-rwxrwxrwx    r -> READABLE (Lectura)  w -> WRITABLE (Escritura)  x -> EXECUTABLE (Ejecutable)
^
|_ El guión que sale a un lado de los permisos se refiere a:
- "Guion solo" # Es un archivo "normal"
d "Letra D" # Hace referencia a que es un directorio
l "Letra l" # Hace referencia a que es un enlace simbolico

    rwx        rwx    rwx
propiertario  grupo  otros
```
- Se pueden representar con **numeros**
- **READ (r)** -> **4**
- **WRITE (w)** -> **2**
- **EXEC (x)** -> **1**
```
   400       777        536
r-------- rwxrwxrwx  r-x-wxrw-
```
# Puertos
- **21 ftp**:  **Protocolo** de **red** estándar que se utiliza para **transferir archivos**
- **22 ssh**:  **Protocolo** de **red** que permite **conexiones seguras** y **cifradas** entre **dos sistemas**
- **23 telnet**:  **Protocolo** de **red** que permite la **comunicación bidireccional interactiva basada** en **texto entre dos computadoras** o **dispositivos**
- **25 smtp**:  **Protocolo** estándar utilizado para **enviar correos electrónicos** a través de **internet**
- **8080 http**:  **Protocolo** de **comunicación** que se utiliza para **transferir información entre un cliente (como un navegador web)** y **un servidor web**
- **443 ssl/tls -> https**:  **Versión segura** del **protocolo HTTP**
- **3306 mysql**:  **Sistema** de **gestión** de **base de datos relacional**

# Escalada de privilegios
- **sudo -l**  R= **Listar** los **privilegios** de **sudo** que tiene el **usuario actual**
- **find / -perm -4000 2>/dev/null**  R= **Buscar archivos** con el **bit SUID activado** en **todo** el **sistema**
- **ss -tuln**  R= **Mostrar puertos abiertos** y **servicios escuchando**
- **ps- aux**  R= **Muestra** una **lista** de **todos** los **procesos** que se están **ejecutando** en el **sistema**
- **/home/ETSCTF/.ssh/id_rsa**  R= **Corresponde** a una **clave privada** **SSH** para el **usuario ETSCTF**
- **/etc/cron.d**  R= **Tareas** que se **ejecuta** cada **cierto tiempo** (se usa **pspy** y es casi lo mismo que **ps -aux**)






