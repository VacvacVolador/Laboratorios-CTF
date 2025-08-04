1- Ping y NMAP

<img width="783" height="412" alt="image" src="https://github.com/user-attachments/assets/57bba441-88e3-492d-a18e-1c14591628a9" />

2-Escaneo con gobuster

<img width="945" height="618" alt="image" src="https://github.com/user-attachments/assets/ccbfceea-8641-471b-9629-a47b4a21a093" />

Veo que hay un jenkins y busco haber si hay algun xploit para esta version 2.441, encuentro una.

<img width="926" height="534" alt="image" src="https://github.com/user-attachments/assets/609d0600-bf1b-4830-ad3f-7b0d4adbd06e" />

<img width="612" height="186" alt="image" src="https://github.com/user-attachments/assets/3b7e0b7d-e568-449c-9ed0-440645b7db1a" />

<img width="743" height="645" alt="image" src="https://github.com/user-attachments/assets/3664c53a-a8ff-4aca-b40f-66bbec4d8070" />

Miro como se usa y funciona!

3- Veo que hay dos usuarios, pinguinito y bobby, tocara fuerza bruta

<img width="947" height="584" alt="image" src="https://github.com/user-attachments/assets/617ed80f-6b42-4f0a-a135-9408cd0cc552" />

Una vez con la contraseña accedo via ssh.

<img width="806" height="211" alt="image" src="https://github.com/user-attachments/assets/1fd7f68b-e32e-409c-9e6f-182a0b17fdd2" />

4- Escalada a usuario pinguinito y despues a root.

<img width="485" height="98" alt="image" src="https://github.com/user-attachments/assets/fd536002-6882-4ca1-ad6a-34dcd7c25287" />

GTFOBins y escalo a usuario pinguinito.

<img width="705" height="217" alt="image" src="https://github.com/user-attachments/assets/ffa0b1f3-410f-4094-95ae-16eaa4c35b8b" />

Ahora vemos que hay un .py , vamos a darle permisos de escritura y lo vamos a modificar, no tiene ni vim ni nano, aqui me costo un poco.

<img width="723" height="354" alt="image" src="https://github.com/user-attachments/assets/f7ec950e-a288-41ec-ab6f-27e4e4493ae5" />
