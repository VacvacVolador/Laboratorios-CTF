1- PING + NMAP

<img width="774" height="472" alt="image" src="https://github.com/user-attachments/assets/57fb8d11-af62-41d3-ae0a-2713e5f77ef3" />

2- Gobuster , per buscar directoris

<img width="952" height="438" alt="image" src="https://github.com/user-attachments/assets/18dffbd9-5f44-4b52-9114-1c66e41b8b50" />

3- Voy a provar a ver si es vulnerable a wfuzz:

<img width="945" height="334" alt="image" src="https://github.com/user-attachments/assets/5b437aaf-f1ed-4808-95c7-01618913d2b9" />

Vale, vemos que con la palabra secret podemos ejecutar.

4- ver usuarios exsistentes:

<img width="959" height="889" alt="image" src="https://github.com/user-attachments/assets/bc330563-e32a-4700-ab08-76874638a8a8" />

Tenemos dos usuarios, vamos a intentar a ver si tienen la clave publica ssh y asi podremos usarla.

<img width="851" height="884" alt="image" src="https://github.com/user-attachments/assets/a4d51589-1ef2-4bc7-987a-a7a7acdf36b8" />

5- Una vez tenemos la clave copiada en un fichero .txt le damos permisos y entramos.

<img width="394" height="92" alt="image" src="https://github.com/user-attachments/assets/5d8026b8-5817-4fd7-a5fe-80167443bc46" />

<img width="289" height="41" alt="image" src="https://github.com/user-attachments/assets/ec1da975-23ae-4a08-a5b0-7dff2816d590" />

6- Escalar a usuario luisillo primero:

<img width="845" height="119" alt="image" src="https://github.com/user-attachments/assets/554f6528-a2e3-4874-a01a-ea96c81cd7aa" />

<img width="767" height="195" alt="image" src="https://github.com/user-attachments/assets/2e5ecfc6-0e33-4f2f-b0e5-88f583f5b2d6" />

Una vez somos luisillo, vemos que ejecuta un script en pyton, y llama a otro script y da error, aprovecharemos para crear el script que llama y darnos permisos de root.

<img width="946" height="391" alt="image" src="https://github.com/user-attachments/assets/340f5812-f6ec-4b6b-81e0-f21653d7be1a" />


