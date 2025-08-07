1-NMAP

<img width="634" height="287" alt="image" src="https://github.com/user-attachments/assets/89a2ffe3-ecc5-4b53-862b-576a9b8e54c9" />

2-Gobuster para ver directorios

<img width="749" height="386" alt="image" src="https://github.com/user-attachments/assets/19a70024-2506-4285-9293-d72505ec462f" />

No he encontrado ningun util, al menos a simple vista, analizando el codigo de la pagina fuente he visto un .js que tambien lo he analizado y he encontrado esto:

<img width="1280" height="427" alt="image" src="https://github.com/user-attachments/assets/6ba12a10-059d-4f08-bde6-6925fe1cac5b" />

Donde hay esto:

<img width="459" height="136" alt="image" src="https://github.com/user-attachments/assets/579db617-76c0-4095-b227-06b7b634b097" />

Conectamos y consultamos como escalar:

<img width="615" height="385" alt="image" src="https://github.com/user-attachments/assets/69d9b467-dbee-445e-b3fb-830a2507d6ec" />

-

<img width="558" height="63" alt="image" src="https://github.com/user-attachments/assets/514f4c26-fb36-4ffe-92c9-4064a44ec4ae" />

Ya con el usuario chocolate encuentro un fichero que veo que se ejecuta cada 5 segundos, lo edito asi:


Me pongo en escucha y ya nos llega la shell
