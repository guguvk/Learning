# Comandos básicos
- `cd` Cambiar de directorio `cd Directorio_al_que_se_accedera` y si haces tal cual `cd` te lleva al PATH del usuario
- `cd..` Retroceder un directorio. Si estamos en `/home/gugu/a/b/c` y hacemos `cd ../..` cambiamos a `/home/gugu/a` (retrocedemos 2 directorios "`../`" hace referencia a que directorio)
- `mkdir` Crear un directorio `mkdir Directorio_a_crear`
- `rm` Eliminar directorio `rm Directorio_a_eliminar`
- `mv` Mover archivos o carpetas de lugar `mv archivo_que_se_movera lugar_a_donde_se_movera`
- `mv` Renombrar archivos o carpetas `mv carpeta_que_se_renombrara nuevo_nombre_de_carpeta`
- `cp` Copia archivos o carpetas `archivo_que_se_copiara lugar_donde_se_copiara` "lugar_donde_se_copiara" (es carpeta o ruta absoluta "`/esto/es/la/ruta/absoluta`")
- `clear` Limpiar la pantalla (quitar todo lo que se mostraba y lo anterior)
- `ls` Listar lo que hay en el directorio actual, `ls -l` Listar lo que hay y ver mas informacion (permisos, usuario propietario, grupo, tamaño y si es un enlace simbolico)
- `cat` Visualizar lo que tiene dentro de un archivo (sin necesidad de abrirlo)
- `touch` crea un archivo (sin necesidad de abrir y volver a guardar)
- `grep` Extraer texto de un archivo (puede estar dentro de un archivo directamente o un archivo dentro de una carpeta)
- `pwd` Te muestra la ruta actual donde estas ubicado
- `whoami` Te muestra el usuario actual (el que estas usando)
- `id` Muestra información sobre la identidad de un usuario y los grupos a los que pertenece
- `*` Se refiere a 0 o mas (basicamente, todo)
- `>` Redirige la salida de un comando a otro comando o a un archivo
- `<` Hace la entrada de una cadena a un comando

# Conceptos basicos
- **Que** es un **Rabbit Hole**?
- **Que** es **estar** en **escucha**?
- **Que** es el **fuzzing**?
- **Que** es un **exploit**?
- **Que** es **openvpn**?
- **En linux importan** las **extensiones**?
- **Que** es el **passwd**?
- **Que** es el **shadow**?
- **Que** es **PoC**?
- **Que** es **rustscan**?
- **Que** es **nmap**?
- **Cuantos puertos existen**?
- **Que** es **dirsearch**?
- **Al entrar** a una **pagina web** que debemos **buscar**?
- **Que** es **Netcat**?
- **Que** es una **tty**?
- **Por que** exportar las **variables SHELL** y **TERM**?
-  **Al** hacer **sudo -l** si no arroja **información** que **significa**?

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
- Se pueden representar con **numeros   4** -> **READ   2** -> **WRITE   1** -> **EXEC**
```
   400       777        536
r-------- rwxrwxrwx  r-x-wxrw-
```
# Puertos
- **21 ftp**
- **22 ssh**
- **23 telnet**
- **25 smtp**  #Servicio por el cual corren los puertos
- **8080 http**
- **443 ssl/tls -> https**
- **445 microsoft-ds**
- **3306 mysql**

# Escalada de privilegios
- **sudo -l** 
- **find / -perm -4000 2>/dev/null**
- **ss -tuln** 
- **ps- aux**
- **/home/ETSCTF/.ssh/id_rsa** 
- **/etc/cron.d**






