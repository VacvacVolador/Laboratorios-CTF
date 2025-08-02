1-Ping   

<img width="511" height="167" alt="image" src="https://github.com/user-attachments/assets/5a26c225-cfb8-4783-a974-ca8545466fc1" />

2- Escaneo NMAP   

<img width="765" height="312" alt="image" src="https://github.com/user-attachments/assets/1f7b3fa8-0999-4183-92e2-a65839c2aa62" />

3- Visitamos http y vemos solo una imagen de un huevo kinder. Inspeciono la pagina y no encuentro nada , asi que descargo la imagen.

<img width="819" height="809" alt="image" src="https://github.com/user-attachments/assets/d123bf05-1f88-41b3-93a8-6127394d0359" />

Una vez descargada la investigamos un poco mas a fondo.   

<img width="377" height="174" alt="image" src="https://github.com/user-attachments/assets/c25b6def-a074-409e-9c90-2c4a142e83f8" />   

Hago un steghide y la descomprimo sin contraseña y bingo. Pero no tiene nada! Seguimos buscando y encontramos un usuario en la imagen.

<img width="629" height="389" alt="image" src="https://github.com/user-attachments/assets/957e0b0b-ef51-470c-85c3-9ff031a9d387" />

4- Ya tenemos un usuario, ahora nos falta la contraseña, asi que fuerza bruta con hydra.  

<img width="833" height="328" alt="image" src="https://github.com/user-attachments/assets/6fafe74e-572c-4393-b288-dce3feb98b67" /> 

5- Una vez hydra nos arroja la contraseña entramos via ssh y escalamos permisos, esta vez , facil!  

<img width="572" height="211" alt="image" src="https://github.com/user-attachments/assets/7047f3a4-4836-42b7-a932-3166bae5a789" />





