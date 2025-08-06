1- Ping y NMAP

<img width="761" height="477" alt="image" src="https://github.com/user-attachments/assets/98554d25-adf0-49ad-8f15-1cff23e7fee0" />

2-Gobuster:

<img width="758" height="498" alt="image" src="https://github.com/user-attachments/assets/31dba701-3985-4bdf-a9f1-c89f18d554ab" />

Entramos al directorio imagenes y vemos un txt:

<img width="708" height="116" alt="image" src="https://github.com/user-attachments/assets/b545c102-ba12-432a-92b5-42d33d731832" />

Entro al /secret y me encuentro unos usuarios: ya tengo una contraseña y 3 usuarios::

<img width="523" height="177" alt="image" src="https://github.com/user-attachments/assets/955a47a1-bbec-4438-b124-5cc097a50d41" />

3- Una vez dentro de mysql::

<img width="760" height="672" alt="image" src="https://github.com/user-attachments/assets/953b441f-2302-4357-9eab-9d066619d33e" />

Descubro otra ruta: unprivate/acces

<img width="1081" height="555" alt="image" src="https://github.com/user-attachments/assets/c215415c-c461-472a-b724-2554be8e310e" />

Aqui la verdad esque he visto el usuario de la pagina principal que se llama  grooti16 y he provado directamente numero 16 y cualquier cosa y se me ha descargado un zip:

Lo he descargado y he usado la contraseña que haviamos conseguido: 

<img width="714" height="658" alt="image" src="https://github.com/user-attachments/assets/b1d1a737-bdbc-4910-8034-5e67a70a5c18" />

4- Una vez con la lista de los nombres le pasamos a hydra esa lista::

<img width="753" height="258" alt="image" src="https://github.com/user-attachments/assets/4f71de2f-5dc9-432d-9f1a-118df46a3c39" />

5-Escalada::

<img width="751" height="468" alt="image" src="https://github.com/user-attachments/assets/470ed462-26f3-4941-86a9-d9c7242aa8ac" />

Me encuentro este fichero: malicious.sh--- lo modifico::

<img width="341" height="124" alt="image" src="https://github.com/user-attachments/assets/41f17654-3814-46ff-b08c-3329de707137" />

Me pongo en escucha con netcat y ya somos root.

<img width="512" height="131" alt="image" src="https://github.com/user-attachments/assets/24fc0e6a-dcfb-4410-a82b-10b0e0b56616" />
