1-NMAP

<img width="613" height="321" alt="image" src="https://github.com/user-attachments/assets/3c4fece6-b4fe-4f8a-b020-589f38e76577" />

2-Gobuster  

<img width="598" height="342" alt="image" src="https://github.com/user-attachments/assets/51b95c06-8857-41bf-9ac6-2fcbec739521" />

Vemos que nos aparece un panel de login, es vulnerable a sqli

<img width="208" height="104" alt="image" src="https://github.com/user-attachments/assets/1d466c00-e6e8-4716-801d-8ed483ee3c35" />

Una vez dentro vemos que nos dice que hay un fichero de logs disponible:

<img width="1532" height="283" alt="image" src="https://github.com/user-attachments/assets/739db726-aee9-41ea-839a-037fa72e2238" />

Nos conectamos via ssh al usuario y pass:

<img width="529" height="471" alt="image" src="https://github.com/user-attachments/assets/b92da3e4-1aeb-43b7-99f4-bf4229ad11f4" />

encontramos otro usuario:

hacemos un ps aux y vemos que esta corriendo un socat

<img width="450" height="77" alt="image" src="https://github.com/user-attachments/assets/44ccad70-623c-4aa6-a1cf-9b891055ab6e" />

tratamos la consola y hacemos lo mismo con este usuario:

<img width="748" height="599" alt="image" src="https://github.com/user-attachments/assets/af5b42ec-2d18-4569-82fb-99a78d7851c7" />

<img width="339" height="104" alt="image" src="https://github.com/user-attachments/assets/d5aff983-5c76-4834-a875-1163583a93c1" />

Encontramos esto que se esta ejecutando con el cron cada minuto cada dia .... y lo modificamos:

<img width="528" height="118" alt="image" src="https://github.com/user-attachments/assets/01fcd627-bb73-45ed-b400-c492b3c52ef1" />

