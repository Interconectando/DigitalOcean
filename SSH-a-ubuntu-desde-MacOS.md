# Pasos para conección con una instancia de DigitalOcean con Sistema operativo Linux Ubuntu 18, mediante SSH desde la terminal de MacOS, y dejar configurado el servidor para administración remota segura.

Obten USD100 usando mi clave de promoción al registrarte en Digital Ocean
## [Código de promoción de 100 USD en Digital Ocean] (https://m.do.co/c/173db4c4fe04)

### Abrir la terminal

Puedes abrir tú terminal haciendo una búsqueda como:

Cmd + Space `terminal`

### Ingresa a tu droplet de Digital Ocean 



---
## 1 Creación de un usuario `Non-root` con privilegios de Super Usuario (SuperUser)
Creación de usuario

`adduser Usuario`

Ingresa dos veces la contraseña del nuevo usuario `Usuario`

Te preguntará que ingreses otra información general del usurio, puedes dejar en blanco todas las opciones.

Ahora que el usuario ha sido creado, agrega privilegios para que pueda ejecutar tareas como Super Usuario





---
## 2 Configuración de enlace SSH

### Crear una llave en la ubicación -f, del tipo rsa, de tamaño en bits 4096
`ssh-keygen -f ~/Users/ElChupa/id_rsa_miclave.pub -t rsa -b 4096`

---
## 3 Asegurar el servidor

### Prohibir el acceso remoto de `root`

Modifica `sshd_config` en el servidor Ubuntu remoto

`nano /etc/ssh/sshd_config` 

La linea a modificar es:

```bash
# Authentcation:
PermitRootLogin no
```
Ahora, para que los cambios tomen efecto

`service ssh restart`


### Deshabilitación de acceso al servidor por medio de contraseña
