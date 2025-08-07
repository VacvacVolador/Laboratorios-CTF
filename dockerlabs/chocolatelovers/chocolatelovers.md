1- Nmap

<img width="618" height="211" alt="image" src="https://github.com/user-attachments/assets/764ff4b4-278e-4e94-a7ca-f7b1baff9465" />

2-Inspecciono el codigo fuente:

<img width="979" height="316" alt="image" src="https://github.com/user-attachments/assets/272dbce8-1019-4bf4-a25d-d4ea2cf4e9ba" />

<img width="869" height="512" alt="image" src="https://github.com/user-attachments/assets/040cc58d-8b25-4b47-aa9f-9dc89cde9ab3" />

Pruevo con admin:admin y entro:

Voy directamente a plugins y subo mi revrsehell:

<img width="678" height="387" alt="image" src="https://github.com/user-attachments/assets/6082bbea-2a48-48ea-919d-866946c440dc" />

-
<img width="603" height="85" alt="image" src="https://github.com/user-attachments/assets/0bce9678-2a0c-4260-9448-506a1a01245a" />

-

<img width="474" height="156" alt="image" src="https://github.com/user-attachments/assets/acf07f05-acef-4837-a08b-579f3c50fd67" />

Y ya me llega la shell

vemos que es vulnerable a suid a php:

<img width="763" height="263" alt="image" src="https://github.com/user-attachments/assets/a707c5ab-55a7-4a83-b6da-c9f628e0e0e6" />

Me pongo en escucha y ejecuto el comando de arriba:

<img width="424" height="83" alt="image" src="https://github.com/user-attachments/assets/f6516891-78ee-4408-abfe-2440273477db" />

Ahora buscando veo que hay un fichero que se ejecuta cada 5 segundos: lo edito y me mando otra shell definitiva ya:

<img width="681" height="62" alt="image" src="https://github.com/user-attachments/assets/6168b1ce-bff1-4234-9904-c68d8035592c" />

<img width="545" height="118" alt="image" src="https://github.com/user-attachments/assets/440c8c4b-3874-4b03-97fb-0d101337c0b5" />
