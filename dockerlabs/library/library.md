1- Ping y NMAP

<img width="773" height="478" alt="image" src="https://github.com/user-attachments/assets/d71bbdf5-0a59-43e7-9516-7d4e289fd80a" />

2- Gobuster para ver directorios ocultos

<img width="937" height="495" alt="image" src="https://github.com/user-attachments/assets/19b4bb75-fbbf-40b0-9a9c-a1a80c656a2a" />

3- Vemos que hay un directorio llamado /index.php.

<img width="704" height="209" alt="image" src="https://github.com/user-attachments/assets/9eb16a7f-b5ff-4ba7-b74c-aa2c8f25ce55" />

4- Tenemos una contraseña parece, falta el usuario:

<img width="941" height="243" alt="image" src="https://github.com/user-attachments/assets/b5a63282-6b18-4cda-a001-688fba08174b" />

5- Una vez tenemos usuario y passw, accedemos y hacemos como siempre de primeras sudo -l

<img width="815" height="421" alt="image" src="https://github.com/user-attachments/assets/8d56249f-d1dc-4298-ae83-041dbf99e2a2" />

Vemos que hay un script, y que tenemos permisos para ejecutar y leer.

<img width="435" height="55" alt="image" src="https://github.com/user-attachments/assets/6ed07d0d-3385-455d-80bd-278126af409d" />

6- Lo eliminamos y creamos uno con el mismo nombre con nuestro codigo.

<img width="541" height="169" alt="image" src="https://github.com/user-attachments/assets/83ce39b7-cf12-4058-8121-c7709beaf647" />
