1- Ping y NMAP(el primer nmap no me ha arrojado el ftp no se el porque)

<img width="778" height="533" alt="image" src="https://github.com/user-attachments/assets/49a792e3-f31a-4e0f-857a-8ff977be026c" />

<img width="735" height="615" alt="image" src="https://github.com/user-attachments/assets/87d71354-d98f-4691-8538-dbd96e36b951" />

2- Visitar html, prevamiente uso de gobuster para descubrir rutas.

<img width="1155" height="136" alt="image" src="https://github.com/user-attachments/assets/74db8132-18ba-4212-9692-e30440ce5925" />

3- Entramos al puerto :3000 y vemos que hay un grafana, buscamos algun xploit y encontramos un de facil:

<img width="941" height="174" alt="image" src="https://github.com/user-attachments/assets/994d54c2-c7e6-41eb-8938-616078da705f" />

<img width="820" height="217" alt="image" src="https://github.com/user-attachments/assets/1f1e7391-cd7f-4319-843e-26b15e8766b4" />

<img width="635" height="462" alt="image" src="https://github.com/user-attachments/assets/c997e0ba-1994-4f90-acf6-c16d9187db83" />

4- Ahora vamos a la ruta que nos ha indicado el html.

<img width="218" height="42" alt="image" src="https://github.com/user-attachments/assets/a191f5ea-3faa-4c30-bffc-11aed9c9ed85" />

Tenemos una passw, ahora tenemos que ver donde se usa, vemos que tiene el ftp abierto, voy a ver y encuentro una base de datos.

<img width="939" height="532" alt="image" src="https://github.com/user-attachments/assets/a491defa-7731-4be9-8cd3-2b3c2920ffd0" />

Buscando vi que se podia abrir con keepassxc database.kdbx asi que lo instale y lo abri.

<img width="360" height="251" alt="image" src="https://github.com/user-attachments/assets/e640c301-a3fa-4f36-8bc6-2f0146386a99" />

5- Ya tenemos usuario y passw para ssh:

<img width="797" height="421" alt="image" src="https://github.com/user-attachments/assets/bdcd75c8-cf70-4b0a-88a0-24b4f4303512" />

6- Hacemos sudo -l y vemos que hay un fichero .py vulnerable para ejecutar con root. Vamos a editarlo.

<img width="341" height="116" alt="image" src="https://github.com/user-attachments/assets/8ad77495-292b-4080-ba46-5b3db819e5ba" />

<img width="302" height="259" alt="image" src="https://github.com/user-attachments/assets/59003fe7-3a2f-47f4-9f78-f0fe1ee2423b" />

<img width="399" height="96" alt="image" src="https://github.com/user-attachments/assets/10406b8f-9518-461f-aa21-7213f5ea2215" />
