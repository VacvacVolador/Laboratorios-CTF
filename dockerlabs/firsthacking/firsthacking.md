1-Ping   

<img width="517" height="182" alt="image" src="https://github.com/user-attachments/assets/eabc8728-002f-4ce7-9d44-1de77d8b24b3" />   

2- Escaneo NMAP

<img width="766" height="256" alt="image" src="https://github.com/user-attachments/assets/3dffa2af-55fa-4827-8145-8c825e5e7d3e" />   

3- Vemos que solo tiene ftp y nos fijamos que tiene vsftpd 2.3.4, vamos a buscar un xploit ya que no hay mucho mas donde urgar.

<img width="606" height="214" alt="image" src="https://github.com/user-attachments/assets/5deff5ee-3d1f-4689-9c5b-4b3fc8131a14" />    

---abrimos la consola de xploits: msfconsole y buscamos: search vstfpd 2.3.4       

<img width="946" height="199" alt="image" src="https://github.com/user-attachments/assets/84e24f54-0284-418a-b3ef-894105641803" />    

4- Usamos el unico que hay. No tiene mucha perdida, es facil de usar, selecionamos use 0 y configuramos.

<img width="939" height="500" alt="image" src="https://github.com/user-attachments/assets/418ab2ec-a43d-4b71-8d23-0b97316b9055" />    

Configuramos en este caso solo el RHOSTS i ponemos la ip a atacar. RPORT ya esta correcto en este port.  
Y para ejecutar el xploit se usa run y ya vemos que somos directamente root.

<img width="841" height="197" alt="image" src="https://github.com/user-attachments/assets/d3a7b2e8-6632-468f-ae3c-36ec22e260c9" />





