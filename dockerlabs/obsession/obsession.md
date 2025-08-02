1- Ping.

<img width="523" height="154" alt="image" src="https://github.com/user-attachments/assets/c50fe17b-32db-4e47-9809-3fae9371c3cd" />

2- Escaneo NMAP

<img width="649" height="501" alt="image" src="https://github.com/user-attachments/assets/ad58437a-7565-4569-ae0f-73b82bf9e42a" />

Vemos que el escaneo tiene el ftp abierto a anonymous:anonymous

3- Logeamos en ftp

<img width="305" height="133" alt="image" src="https://github.com/user-attachments/assets/18ba9ecb-a1d8-4c27-8d54-b10019fecb23" />

Me encuentro unos ficheros los descargo y los leo, solo encuentro un par de usuarios y poco mas.

<img width="925" height="389" alt="image" src="https://github.com/user-attachments/assets/51f8e2f3-ab3f-4852-a3c6-5d04137f277a" />

<img width="956" height="338" alt="image" src="https://github.com/user-attachments/assets/00c3787b-38f3-4e63-897d-cdfa5c99b37c" />

4- Hydra , para obtener contraseña.

<img width="946" height="281" alt="image" src="https://github.com/user-attachments/assets/f1708e90-2403-4ead-ba51-c65a6dbf3ef5" />

5- Escalada de privilegios, como siempre siempre primero sudo -l.

<img width="585" height="202" alt="image" src="https://github.com/user-attachments/assets/96998cd3-13d3-48f0-a358-9a7a5241d538" />

Checkeamos GTFOBins y ya somos root.

