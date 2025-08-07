1-NMAP

<img width="618" height="200" alt="image" src="https://github.com/user-attachments/assets/b82874f3-d68e-480b-a079-5762f8fbfcf1" />

2- Gobuster x2:

<img width="751" height="405" alt="image" src="https://github.com/user-attachments/assets/ab87be25-c51e-4d87-8e8e-7fb4c7a3a229" />

<img width="759" height="409" alt="image" src="https://github.com/user-attachments/assets/8957e596-aa0f-4986-8f45-9345616ff0a7" />

Descubrimos la ruta de panel de login de wordpress::

3- VAmos a intentar descubrir usuarios:

wpscan --url http://172.17.0.2/wordpress -e u,p

<img width="572" height="128" alt="image" src="https://github.com/user-attachments/assets/998c0d00-1f2d-4d5b-a887-42ef0d32743d" />

4- Ya tenemos el usuario, vamos a por la contraseña:

wpscan --url http://172.17.0.2/wordpress -usernames mario -passwords <wordlist>

<img width="492" height="178" alt="image" src="https://github.com/user-attachments/assets/cc03963e-5f58-4da5-be2c-e277755eb146" />

5- Vamos a añadir un pluggin camuflado de reverse shell:

<img width="656" height="431" alt="image" src="https://github.com/user-attachments/assets/9b964515-4dc6-4278-93f0-9d1cdb1eef80" />

<img width="521" height="175" alt="image" src="https://github.com/user-attachments/assets/11977c6d-55b8-499c-96dd-fc31c6bd9c27" />

Nos ponemos en escucha y ejectuamos cualquier pagina del sitio.

Y ya nos llega la shell:

<img width="432" height="289" alt="image" src="https://github.com/user-attachments/assets/1036eb38-8639-4a6b-a876-5adacbf5fb0a" />

Escalada:

<img width="473" height="168" alt="image" src="https://github.com/user-attachments/assets/2b84a45c-bd1c-4021-abba-a75f5388b0fa" />

Consultamos GTFOBins y escalamos:

<img width="349" height="111" alt="image" src="https://github.com/user-attachments/assets/d7aa1d6d-e24f-4149-b96b-907f287845f5" />

