1- Provamos ping.  

<img width="525" height="184" alt="image" src="https://github.com/user-attachments/assets/ce83095d-9605-4883-88c5-32244e3b33c3" />     

2- Escaneo de NMAP  

<img width="788" height="285" alt="image" src="https://github.com/user-attachments/assets/36f39687-1395-44e1-a2ad-f6ac994ab688" />        

-sC = Incluye cosas como: leer banners, buscar vulnerabilidades simples, etc.     
-sV = detección de versiones.     
-T4 = Velocidad de escaneo. Va de T0 (muy lento) a T5 (muy agresivo).    
-Pn = No hace ping al host.    


Vemos que solo tiene abierto el puerto ssh(22)    
Busco un exploit, encuentro pero no logro hacerlo funcionar.   

<img width="934" height="187" alt="image" src="https://github.com/user-attachments/assets/a5d234e2-1594-480a-a174-e5e50399834d" />    

3- Como todas las maquinas tienen el usuario root, intento usar fuerza bruta.   

<img width="677" height="319" alt="image" src="https://github.com/user-attachments/assets/8930651c-f7ef-4d09-a175-f0ef6aff0c55" />     

Y encontro la password para root.   
Hacemos login y ya somos root.    
<img width="630" height="263" alt="image" src="https://github.com/user-attachments/assets/07c5d230-c6eb-426d-81d2-826887a6588c" />


