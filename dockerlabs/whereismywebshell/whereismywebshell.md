1- Ping y NMAP

<img width="772" height="412" alt="image" src="https://github.com/user-attachments/assets/fcc53898-7def-4247-8836-35dc70cb2524" />

2- He estado comprovando la pagina web y no tiene nada donde urgar. Provaremos con gobuster

<img width="955" height="425" alt="image" src="https://github.com/user-attachments/assets/5913ac3b-c1f3-48dd-a388-cfd33fe2643e" />

Vemos un shell.php un poco sospechoso, provamos de hacer fuzzing a ver que hay por ahi.

3- fuzzing

<img width="943" height="389" alt="image" src="https://github.com/user-attachments/assets/63b6f11c-df11-454b-b50e-d5e7651bde55" />

Vemos que es el parameter.

4- Pasaremos a tirar una reverse shell.

<img width="630" height="114" alt="image" src="https://github.com/user-attachments/assets/1e25de80-9537-4801-980e-9e32348a0b25" />
<img width="725" height="78" alt="image" src="https://github.com/user-attachments/assets/88b4e607-475a-409a-94be-3b0017c27277" />

Primero nos ponemos en escucha, y luego intro a la http.

5- Escalada

He estado provando y al final he encontrado esto: 

<img width="385" height="189" alt="image" src="https://github.com/user-attachments/assets/9ddfd90a-b1d2-4174-bd46-ef4d4abab836" />

ls -a es para ver archivos ocultos.
