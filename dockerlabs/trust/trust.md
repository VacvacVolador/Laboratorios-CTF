1-Realizamos ping.   

<img width="523" height="179" alt="image" src="https://github.com/user-attachments/assets/42901c9c-92f6-4e61-af3c-99c198c40ee2" />   


2-Escaneo de NMAP   

<img width="784" height="326" alt="image" src="https://github.com/user-attachments/assets/a5ff7b47-995f-47c8-9de0-3c4bcf540fb5" />   

-sC = Incluye cosas como: leer banners, buscar vulnerabilidades simples, etc.   
-sV = detección de versiones.   
-T4 = Velocidad de escaneo. Va de T0 (muy lento) a T5 (muy agresivo).   
-Pn = No hace ping al host.   

3- Entramos via http i vemos que no hay mucho que ver. Provaremos con gobuster a ver si hay algun directorio.    
gobuster dir -u http://172.18.0.2 -w /usr/share/seclists/Discovery/Web-Content/directory-list-lowercase-2.3-medium.txt -x html,php,sh,py,txt   

<img width="954" height="464" alt="image" src="https://github.com/user-attachments/assets/f53a7308-c78b-4230-8f70-892cdf1ba27d" />   

4- Entramos a la /secret.php que nos ha arrojado el escaneo, i vemos un nombre:    
<img width="969" height="578" alt="image" src="https://github.com/user-attachments/assets/47d222d6-c48c-4cc4-a40c-e9f0877aca70" />   

5- Como vimos con el scaneo que tenia abierto el puerto ssh, provaremos de encontrar la password de este nombre con hydra:   
hydra -l mario -P /usr/share/wordlists/rockyou.txt  ssh://172.18.0.2 -t 64   

<img width="957" height="333" alt="image" src="https://github.com/user-attachments/assets/76d7a049-a30a-4c8c-993d-0c65ca6aee09" />   

5- Entramos via ssh:   

<img width="835" height="194" alt="image" src="https://github.com/user-attachments/assets/cbd077c4-afcc-4e82-b2c2-0f7457c79ece" />   
Ya estoy dentro!   

6- Escalada de privilegios:   
Provamos sudo -l y funciona a la primera y ademas sale en GTFOBins, vemos que es vulnerable a vim.  

<img width="939" height="110" alt="image" src="https://github.com/user-attachments/assets/0a65196c-e0e9-47f4-8858-dd58e9bfc3d1" />   
Buscamos en GTFOBins y copiamos comando y listo! ya somos root   
<img width="382" height="93" alt="image" src="https://github.com/user-attachments/assets/0b8289eb-6685-4048-8457-0fa26f4f5eff" />




