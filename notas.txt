# rh124
notas adicionales del curso
                _                      _   _      
  ___ _   _ ___| |_ ___ _ __ ___   ___| |_| |     
 / __| | | / __| __/ _ \ '_ ` _ \ / __| __| |     
 \__ \ |_| \__ \ ||  __/ | | | | | (__| |_| |     
 |___/\__, |___/\__\___|_| |_| |_|\___|\__|_|     
  ___ |___/  __ _ _ __  ___| |__   ___ | |_( )___ 
 / __| '_ \ / _` | '_ \/ __| '_ \ / _ \| __|// __|
 \__ \ | | | (_| | |_) \__ \ | | | (_) | |_  \__ \
 |___/_| |_|\__,_| .__/|___/_| |_|\___/ \__| |___/
                 |_|                              
Para ver el estado de 3 servicios:

# systemctl is-active httpd nfs-server libvirtd

Detener los 3 servicios:

# systemctl stop httpd nfs-server libvirtd

Crear un snapshot

# systemctl snapshot

Listar el snapshot

# systemctl --type=snapshot

Revertir snapshot

# systemctl isolate snapshot-1.snapshot

Revisar de nuevo el estado de los servicios:

# systemctl is-active httpd nfs-server libvirtd

Borrar el snapshot

# systemctl delete snapshot-1.snapshot

  _    _ _ _                    
 | | _(_) | |                   
 | |/ / | | |                   
 |   <| | | |                   
 |_|\_\_|_|_|             _     
  ___(_) __ _ _ __   __ _| |___ 
 / __| |/ _` | '_ \ / _` | / __|
 \__ \ | (_| | | | | (_| | \__ \
 |___/_|\__, |_| |_|\__,_|_|___/
        |___/                   

Configurar core file size
=========================

Ver el tamaño de "core file size"
$ ulimit -c 

Configurar "core file size ilimitado"

$ ulimit -c unlimited

Abrir firefox

$ firefox &

Determinar el PID de firefox

$ ps -elf | grep firefox

Detener el proceso y generar el core dump

$ kill -3 PID


Reiniciar PID
=============

Iniciar el proceso http

# systemctl start httpd

Determinar el PID de httpd

# systemctl status httpd

Enviar kill signal 1

# kill -1 $PID

Simultaneamente en otra consola revisar el archivo de log 

# tail -f /var/log/error_log

      _ _               _             _           
   __| (_)_ __ ___  ___| |_ ___  _ __(_) ___  ___ 
  / _` | | '__/ _ \/ __| __/ _ \| '__| |/ _ \/ __|
 | (_| | | | |  __/ (__| || (_) | |  | |  __/\__ \
  \__,_|_|_|  \___|\___|\__\___/|_|  |_|\___||___/
  ___| |_ __ _  ___| | __                         
 / __| __/ _` |/ __| |/ /                         
 \__ \ || (_| | (__|   <                          
 |___/\__\__,_|\___|_|\_\                         
                                                  
# pushd /var/tmp/
# pushd /etc/sysconfig/network-scripts/
# pushd /var/cache/
# pushd /usr/share/doc

# dirs -l

# popd
# popd
# popd
# popd
