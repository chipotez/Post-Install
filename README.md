# Configuracion de Hostname

Para configurar el hostname en Red Hat Enterprise Linux (RHEL) 8, puedes utilizar el comando hostnamectl. A continuación, se muestran algunos ejemplos de cómo utilizar este comando con diferentes opciones y argumentos:

1. Para establecer el hostname del sistema:

`sudo hostnamectl set-hostname NOMBRE_DE_HOST`

Donde NOMBRE_DE_HOST es el nombre que deseas asignar al sistema. Este comando establece el hostname de forma temporal. Si deseas establecer el hostname de forma permanente, también debes editar el archivo /etc/hostname con el nombre del hostname.

2. Para establecer el hostname del sistema y asignar un nombre de dominio:

`sudo hostnamectl set-hostname NOMBRE_DE_HOST.NOMBRE_DE_DOMINIO`

Donde NOMBRE_DE_HOST es el nombre que deseas asignar al sistema y NOMBRE_DE_DOMINIO es el nombre de dominio que deseas asociar al sistema. Este comando establece el hostname de forma temporal y modifica el archivo /etc/hostname con el nuevo hostname.

3. Para establecer el hostname del sistema y modificar el archivo /etc/hosts para que coincida con el hostname:

`sudo hostnamectl set-hostname --static NOMBRE_DE_HOST`

Donde NOMBRE_DE_HOST es el nombre que deseas asignar al sistema. Este comando establece el hostname de forma temporal y modifica el archivo /etc/hostname y /etc/hosts para que coincidan con el nuevo hostname.

4. Para establecer el hostname del sistema y modificar el archivo /etc/machine-info con información adicional:

Para las opciones --icon-name y --chassis del comando hostnamectl, se pueden usar diferentes valores dependiendo de la distribución y la versión del sistema operativo. En general, estos valores están definidos por la especificación de freedesktop.org.

Para la opción --icon-name, algunos de los valores comunes que se pueden usar incluyen:
```
computer
laptop
tablet
smartphone
server
network-server
desktop
audio-card
video-display
```
Para la opción --chassis, algunos de los valores comunes que se pueden usar incluyen:
```
desktop
laptop
server
handset
tablet
convertible
all-in-one
mini-tower
tower
portable
netbook
sub-notebook
main-server-chassis
expansion-chassis
bus-expansion-chassis
peripheral-chassis
```
Ten en cuenta que la lista completa de valores para estas opciones puede variar según la distribución y la versión del sistema operativo. Además, algunas distribuciones también pueden proporcionar valores personalizados para estas opciones. En cualquier caso, puedes usar el comando hostnamectl --help para obtener una lista completa de las opciones y los valores disponibles en tu sistema operativo.

Configurando el nombre:
```
hostnamectl set-hostname --pretty "Servidor Ansible"
hostnamectl set-icon-name server
hostnamectl set-chassis server
```

Donde NOMBRE PRESENTABLE es un nombre que describes el sistema, ICONO es el nombre del icono asociado con el sistema y TIPO_CHASIS es el tipo de chasis del sistema (por ejemplo, laptop o desktop). Este comando establece el hostname de forma temporal y modifica el archivo /etc/hostname y /etc/machine-info con la información adicional.

5. Para mostrar la información actual del hostname:

`hostnamectl`

Este comando muestra la información actual del hostname, incluyendo el hostname actual, el nombre de dominio, la información presentable, el icono asociado y el tipo de chasis.

Estos son solo algunos ejemplos de cómo configurar el hostname en RHEL 8 utilizando hostnamectl. Es importante tener en cuenta que, para realizar cambios permanentes en el hostname, también debes editar los archivos correspondientes (por ejemplo, /etc/hostname, /etc/hosts o /etc/machine-info).
