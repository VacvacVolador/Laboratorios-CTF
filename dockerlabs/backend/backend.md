1- Ping y NMAP

<img width="618" height="252" alt="image" src="https://github.com/user-attachments/assets/f4825cf0-360a-4d49-ac5f-e3fffe012a89" />

2- Gobuster para ver directorios ocultos

<img width="755" height="447" alt="image" src="https://github.com/user-attachments/assets/874d5b88-e7a4-4887-ac1c-d4a62bd36099" />

3- VAmos via http y vemos un panel de login.

<img width="678" height="693" alt="image" src="https://github.com/user-attachments/assets/b78d23fd-7dc5-4cdf-a215-1b52366d3c0e" />

<img width="563" height="193" alt="image" src="https://github.com/user-attachments/assets/189eee4e-2d15-441e-963d-c77a56acd295" />

<img width="601" height="179" alt="image" src="https://github.com/user-attachments/assets/76d0bda7-970a-4ec0-b5c0-55839fdf47e5" />

Logramos ver las tablas con los usuarios y sus passwords. Intentaremos entrar via ssh.

4- Ssh

<img width="648" height="162" alt="image" src="https://github.com/user-attachments/assets/c74b5eda-caee-44c6-8bcd-81f51ca088f2" />

El unico usuario que ha funcionado via ssh

haciendo ls veo un fichero en la carpeta de root. Lo intento ver mediante grep, que esta en el panel de SUID vulnerables.

<img width="298" height="54" alt="image" src="https://github.com/user-attachments/assets/3039089f-f25a-4208-be36-17603eb53df9" />

Descifro ese hash md5.

<img width="591" height="238" alt="image" src="https://github.com/user-attachments/assets/f2845dcd-63b4-4425-8677-2eb566aca6fc" />

Y ya tenemos la passw de root.

<img width="187" height="76" alt="image" src="https://github.com/user-attachments/assets/74eb2ddc-e878-4f36-9a44-c5610dbb7a3f" />
