1- nmap

<img width="625" height="218" alt="image" src="https://github.com/user-attachments/assets/5ca5d5d9-492a-459d-90fd-db4934d2f62b" />

2- Buscamos directorios gobuster

<img width="753" height="688" alt="image" src="https://github.com/user-attachments/assets/33fb3c94-c5d1-4418-805f-fa0976304c53" />

Primero hago scan sobre la ip y luego sobre la ip/galery y encontramos esto:

Investigando un poco vemos un sitio para subir ficheros

<img width="537" height="179" alt="image" src="https://github.com/user-attachments/assets/e3bd9744-0e30-4bbd-a35b-6fe2997eb9f7" />

Creamos una shell : y la subimos:

<img width="529" height="138" alt="image" src="https://github.com/user-attachments/assets/de606102-8c82-4951-b5c2-8e8fbb2fdf10" />

Guardamos y la ejecutamos via http, previamente nos ponemos en escucha:

<img width="368" height="60" alt="image" src="https://github.com/user-attachments/assets/ddd5e7c0-616a-45e6-a564-d65b39a8c8b6" />

3- Escalada:

<img width="405" height="103" alt="image" src="https://github.com/user-attachments/assets/93182d7f-aa1c-4681-b450-4d19fc11135c" />

Consultamos GTFOBins y vemos que para escalar tenemos que ejecutar un comando dentro de nano:

<img width="685" height="70" alt="image" src="https://github.com/user-attachments/assets/687a9607-224c-440b-85e3-c55ef4a50492" />

sudo nano
^R^X
reset; sh 1>&0 2>&0

<img width="473" height="109" alt="image" src="https://github.com/user-attachments/assets/58c32c28-ee7a-452f-98ed-195b1a22a41d" />


<img width="365" height="163" alt="image" src="https://github.com/user-attachments/assets/85de076e-1c33-412e-bf63-a5b7c57e9682" />


<img width="399" height="130" alt="image" src="https://github.com/user-attachments/assets/337c21b5-ab61-4411-989f-e80f7b0b9d64" />



