1- Ping y NMAP

<img width="610" height="372" alt="image" src="https://github.com/user-attachments/assets/f4f4cf6e-993a-416c-b028-3be7a0e58999" />

2- Entramos via http y vemos una codigo al final de la pagina :

<img width="892" height="726" alt="image" src="https://github.com/user-attachments/assets/8d570293-40c3-4f5f-8c46-c16193d2f73c" />

Es un base64 lo decodificamos y vemos unas credenciales

<img width="252" height="112" alt="image" src="https://github.com/user-attachments/assets/74f3763a-4bcb-4fb6-97dd-e7ec2f565dc9" />

3- Entramos via ssh

<img width="510" height="348" alt="image" src="https://github.com/user-attachments/assets/9b4a0463-5fe2-478e-90b4-18a0a2635a79" />

Vemos que hay otro usuario, saltamos a el despues de encontrar un passw del usuario diego

<img width="507" height="137" alt="image" src="https://github.com/user-attachments/assets/f073c96a-bd5c-46e8-aafb-7e5827ce16b6" />

Decodificamos y entramos

<img width="309" height="113" alt="image" src="https://github.com/user-attachments/assets/e4fc77fa-fa37-4a06-abd0-2367071f4a22" />

<img width="506" height="342" alt="image" src="https://github.com/user-attachments/assets/a3959896-e9a1-4b1f-bc4c-e53ed34facd7" />

Checkeamos permisos y no vemos nada, encontramos un fichero::

Lo mismo, lo decodificamos:

<img width="309" height="61" alt="image" src="https://github.com/user-attachments/assets/cd264738-0ec0-4469-bf19-9f98c5a6b780" />

No encontramos ninguna vulnerabilidad con el usuario diego y encontramos un fichero:

<img width="404" height="563" alt="image" src="https://github.com/user-attachments/assets/f66d687e-075b-4f30-9f71-fb31c501c28c" />

Es un acertijo:

<img width="460" height="73" alt="image" src="https://github.com/user-attachments/assets/2c6bae1a-35cb-4f1c-a961-2c8e0bcd5521" />

Ya somos root!
