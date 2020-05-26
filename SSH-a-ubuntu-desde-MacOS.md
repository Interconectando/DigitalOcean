# Pasos para conección con una instancia de DigitalOcean con Sistema operativo Linux Ubuntu 18, mediante SSH desde la terminal de MacOS, y dejar configurado el servidor para administración remota segura.

### Abrir la terminal

Puedes abrir tú terminal haciendo una búsqueda como:
`terminal`

## 1 Creación de un usuario `Non-root` con privilegios de Super Usuario (SuperUser)


## 2 Configuración de enlace SSH

### Crear una llave en la ubicación -f, del tipo rsa, de tamaño 4096
`ssh-keygen -f ~/Users/ElChupa/id_rsa_miclave.pub -t rsa -b 4096`


## 3 Asegurar el servidor

### Prohibir el acceso remoto de `root`


### Deshabilitación de acceso al servidor por medio de contraseña
