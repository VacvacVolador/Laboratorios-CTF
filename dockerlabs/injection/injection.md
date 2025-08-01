1-Comprovacion de ping.

<img width="560" height="228" alt="image" src="https://github.com/user-attachments/assets/5ed251a8-77ec-41b0-ab91-4d5f8aa86a3c" />

TTL de 64, seguramente estamos contra una maquina linux.

2-Escaneo de NMAP.

<img width="801" height="381" alt="image" src="https://github.com/user-attachments/assets/ff8b520f-a358-43ac-8a8b-d063d309b2d2" />

-sC = Incluye cosas como: leer banners, buscar vulnerabilidades simples, etc.  
-sV = detección de versiones.  
-T4 = Velocidad de escaneo. Va de T0 (muy lento) a T5 (muy agresivo).  
-Pn = No hace ping al host. 

3-Entramos via http i vemos un panel de login.  

Provamos con sqli i entramos a la primera con---  
user: lo que quieras  
pw: admin' or '1'='1  

<img width="988" height="141" alt="image" src="https://github.com/user-attachments/assets/8a3e02da-18d3-4e77-b141-059e3d8dd72e" />

4-Vemos que nos da un codigo, pienso que es una contraseña para usar via ssh.  

<img width="648" height="446" alt="image" src="https://github.com/user-attachments/assets/3d568e52-d069-424d-84bc-075ae1f017a8" />

5-Estamos dentro. Ahora toca buscar como escalar privilegios.

<img width="470" height="247" alt="image" src="https://github.com/user-attachments/assets/f8ff50fd-ae5d-423e-b018-0926249d9367" />   

Intentamos primero siempre con sudo -l, no funciona.    
Segundo intento con: find / -perm -4000 2>/dev/null    
Vemos que hay el /usr/bin/env y buscamos en GTFOBins y vemos que es vulnerable.  

<img width="379" height="66" alt="image" src="https://github.com/user-attachments/assets/f1663886-ed61-4574-8bce-544aa75d1bcc" />

