README Obligatorio Taller 2025.

Uso de playbooks:

Para utilizar el playbook nfs_setup.yml:

Correr comando:

ansible-playbook nfs_setup.yml

El playbook realizara las tareas siguientes, en este orden:

- Chequea que el servidor NFS este instalado
- Se asegura que NFS este iniciado y habilitado
- Si no existe, crea el directorio /var/nfs_shared, y le proporciona permisos 77 y pertenencia al usuario y grupo nobody/nobody
- Comparte el directorio /var/nfs_shared, agregandolo al archivo /etc/exports
- Reinicia el servicio NFS si el archivo /etc/exports es modificado.

Este playbook solo corre en servidores de la familia RedHat

Para utilizar el playbook hardening.yml

correr comando:

ansible-playbook hardening.yml

El playbook realizara las tareas siguientes, en este orden:

- Actualiza los paquetes del servidor
- Habilita firewall si no lo está, y bloquea el trafico entrante permitiendo solo acceso por ssh.
- Modifica el archivo /etc/ssh/sshd_config, reescribiendo lineas para hacer que solo se pueda acceder con clave ssh, y que root no pueda realizar login.
- Instala Fail2ban
- Habilita fail2ban y lo deja habilitado cuando reinicia.
- Configura el archivo /etc/fail2ban/jail.local para que bloquee el acceso ssh si se intenta acceder con usuario/contraseña incorrecto mas de 3 veces, por 600 segundos.
- Reinicia SSH si el archivo /etc/ssh/sshd_config fue modificado
- Reinicia el servidor, si este encontró paquetes a actualizar
- Reinicia fail2ban si el archivo /etc/fail2ban/jail.local tuvo modificaciones
