1-Ping.    

<img width="505" height="149" alt="image" src="https://github.com/user-attachments/assets/0ac20a92-4cb1-4783-92d4-cb09d58582bc" />

2- Escaneo NMAP   

<img width="769" height="318" alt="image" src="https://github.com/user-attachments/assets/e1c94f8d-b6ab-4670-93a2-364432ded023" />

3- Visitamos la http y vemos que hay un nombre nails, inspecciono la pagina y no veo nada raro, pruevo con gobuster y tampoco encuentro nada donde explotar.

4- Voy a hacer fuerza bruta a ese nombre de usuario, y veo que tarda mucho, y leyendo prove de invertir el dicionario de rockyou, funciono.

<img width="829" height="204" alt="image" src="https://github.com/user-attachments/assets/d6fda0f3-2eb4-4b60-a2e5-6ba59abedce6" />    

Una vez invertido el diccionario, vamos con hydra.

<img width="808" height="323" alt="image" src="https://github.com/user-attachments/assets/c8720886-f2e3-4102-8b12-4187ff45ff00" />   

Econtramos la passw y nos logeamos.

5- Accesso ssh   

<img width="691" height="71" alt="image" src="https://github.com/user-attachments/assets/66c3dbd7-6ea1-4ccb-b806-3b1d9f103a5a" />
6- Escalar permisos, provamos como siempre el primero sudo -l y ya encontramos algo.


<img width="496" height="243" alt="image" src="https://github.com/user-attachments/assets/546a5eaa-16c6-4173-bb7b-f18e232d2eb3" />   

Vemos que puede ejcutar comandos y tiramos una consola con el nombre de sonic, y en el perfil de sonic encontramos una contraseña, que no se para que es todavia.

<img width="487" height="88" alt="image" src="https://github.com/user-attachments/assets/e7ef4385-f1ee-4843-950f-8dad5a0f0ada" />

Mismo procedimiento que el otro usuario y facil, ya tenemos root.






