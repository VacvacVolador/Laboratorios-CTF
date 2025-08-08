1-Nmap

<img width="631" height="271" alt="image" src="https://github.com/user-attachments/assets/5f46dc6e-5249-4784-ac20-c7933659b5ec" />

2- Vemos que es un wordpress y hacemos gobuster sobre wordpress:

<img width="756" height="504" alt="image" src="https://github.com/user-attachments/assets/839991e7-813f-48d4-9748-9a00004f3ac4" />

3- VEmos un apartado con usuarios y vemos que este es admin de wordpress

<img width="390" height="283" alt="image" src="https://github.com/user-attachments/assets/411957ba-1145-4652-9642-b60c3b964780" />

4- Nos descargamos el cupp, es un .py que sirve para generar contraseñas a partir de parametros que nosotros le indicamos:

<img width="186" height="91" alt="image" src="https://github.com/user-attachments/assets/ae520e16-53c5-4213-9a95-a0e57fb743e8" />

-

<img width="631" height="650" alt="image" src="https://github.com/user-attachments/assets/180c9672-9c1e-4724-8756-dd5d4cb824bf" />

5- Pasamos wpscan con el usuario luisillo y la lista que nos ha generado:

<img width="758" height="234" alt="image" src="https://github.com/user-attachments/assets/72c36c50-d746-4ec0-81ab-ccde5b2a6471" />

6-Tenemos la passw y nos logeamos en wp, y vamos directo al apartado de pluggins:

<img width="665" height="498" alt="image" src="https://github.com/user-attachments/assets/ebd86e02-0f4b-47c5-a457-c7f5a26fecdd" />

7- Una vez subido el pluggin creado por nosotros con una revershell lo ejecutamos y nos ponemos en escucha:

<img width="951" height="88" alt="image" src="https://github.com/user-attachments/assets/233e0ae6-fcd8-4d30-a558-2dc44bac5bfe" />


-

<img width="433" height="88" alt="image" src="https://github.com/user-attachments/assets/8125b552-19a1-4208-b4de-34067c68df4b" />

Vemos que hay una contraseña en una carpeta:

<img width="738" height="115" alt="image" src="https://github.com/user-attachments/assets/be16e2eb-41a0-4997-b6b8-4dd608ecb320" />

Una vez somos luisillo escalamos con gtfobins y ya somos root.

<img width="752" height="168" alt="image" src="https://github.com/user-attachments/assets/e234ca88-5c41-44d4-bc4b-d76445e28a01" />
