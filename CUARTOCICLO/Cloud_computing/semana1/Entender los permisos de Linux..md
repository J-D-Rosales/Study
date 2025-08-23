UNIX(70's) -> LINUX (90's) <- Lenguaje C.
Linux es multiusuario.
Un usuario: Puede ser una persona o puede ser un usuario administrativo. 
UID: Es el user ID, por defecto vienen creados varios usuarios. El root, es el máximo usuario, el super de supers.  (Los creados en instalaxión tienen un UID < 1000)
En cambio creados por el root es UID.
Para saber quién soy escribo:
```bash
whoami
```

```bash
id
```
Para saber tu id.
En linux no es oblicatorio que un archivo tenga extensión.
___
Cómo creamos un usuario en linux.
Hay comandos administrativos que no todos pueden usarlos. Solamente el root puede crear usuarios.
___
Ejercicio:
Vamos a hacer que jperez pertenezca al grupo estudiante y tesistas. 
1.- Se crea primero los dos grupos.
Si lo haces solo con 
```bash
groupadd estudiantes
```
Esto no va a funcionar. Esto porque aws ha creado un usuario ubunto. En donde, el id de ubunto pertence al id 1000. Para que pueda ejecutar comandos como si fuera root, se debe agregar el usuario al grupo sudo. De esa manera será un usuario administrador. 
Entonces deberías hacer.
```bash
sudo groupadd estudiantes
```
De la misma manera creas tesistas. 
Ahora para visualizar tus grupos haces.
```bash
cat /etc/groups
```
Ahora como crear un usuario. Esto se hace así:
```bash
sudo useradd -m jperez -g estudiantes -G tesistas
```
Si quieres que pertenezca a más grupos adicionales, puedes hacer una , ye lresto de grupos. 
```bash
sudo useradd -m jperez -g estudiantes -G tesistas, sudo
```
De esta manera creas un usuario administrador.
Ahora tenemos que colocarle un password. Así:
```bash
sudo passwd jdaniel
```
Ahora cómo vamos a probar que funciona el jdaniel.
En este caso es con el comando 
```bash
su (switch user)
su jdaniel
```
Luego verifica con whoami y id, que realmente eres ese user, es decir que cambiaste el user.
Ahora vamos a crear el grupo d einvestigafores.
Y lo agregamos a investigadores con
```bash
sudo usermod jdaniel -a -G investigadores
```
___
# Permisos concepto de permisos y cosas así.
En la ppt está muy bien explicado.
Para cambiar los permisos se usa chmod 
AHora para saber como cambiar o que permisos cambiar, hay na tabla en la ppt.

También existes permisos sobre directorio. EN donde solo el dueño puede hacer o deshacer, pero el resto no. S i quieres cambiar lso permisos, debes mediante el admin de ese directorio darle los permisos a otro ususario.
___
# Espacio ocupado por directorios
Con el comando 
```bash
df -h
```
podrás ver tu espacio ocupado
Ahora con el comando 
```bash
top
```
Podrás ver cual de los programas están usando más gigas.
Aunque con 
```bash
htop
```
Dónde se puede ver los cpus, la barrita te dice que tanto estás usando.
Hay mucha inforamción y cosas.
