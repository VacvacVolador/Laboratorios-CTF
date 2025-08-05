1- Ping y NMAP

<img width="634" height="534" alt="image" src="https://github.com/user-attachments/assets/1f2b8d18-607f-416a-81ca-8fecc232a84a" />

2- Buscar directorios :

<img width="760" height="412" alt="image" src="https://github.com/user-attachments/assets/c4871814-88ae-42c7-986c-e8595b190d88" />

3- enum4linux IP

<img width="553" height="254" alt="image" src="https://github.com/user-attachments/assets/121192c3-869c-41f9-8ef1-3203c0d2004f" />

4- crackmapexec smb IP ATACADA -u 'usuari' -p /usr/share/wordlists/rockyou.txt----pwd

<img width="713" height="115" alt="image" src="https://github.com/user-attachments/assets/79b9c2b1-9247-40d2-9ac2-ae475ca12e12" />

Ya tenemos usuario y contraseña:

<img width="770" height="568" alt="image" src="https://github.com/user-attachments/assets/4808a4e8-f23e-421a-b8a4-b8159595f310" />

Vemos donde tiene acceso y donde no.

<img width="380" height="72" alt="image" src="https://github.com/user-attachments/assets/d29a4d44-41f5-47c7-9c76-f6647eee7918" />

<img width="538" height="718" alt="image" src="https://github.com/user-attachments/assets/7653aa6d-53e6-4f36-ace9-2e8027855453" />

Vemos dos ficheros y los cojemos, los leemos y vemos unas contraseñas:

<img width="578" height="489" alt="image" src="https://github.com/user-attachments/assets/b9202641-c52c-4604-9989-14984c0f8e78" />

<img width="507" height="355" alt="image" src="https://github.com/user-attachments/assets/3c40f09b-8bd4-4204-9f7a-f9c177e3b119" />

Voy a su /home y subo un fichero que es una revshell. Me pongo en escucha y ejecuto.

<img width="625" height="110" alt="image" src="https://github.com/user-attachments/assets/917ea911-c63f-4000-97e8-3c73df4d191a" />

Una vez dentro:

<img width="639" height="199" alt="image" src="https://github.com/user-attachments/assets/2916101c-453e-4480-8187-01fd5d775886" />

Consultamos en GTFOBins y ya somos root.
