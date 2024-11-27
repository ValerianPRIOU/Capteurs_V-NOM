# Lidar

***!!! Le PCB réalisé pour le V-NOM n'utilise pas le même µP que la STM32 qu'on utilise pour tester le lidar, il faut bien garder ça en tête et il faudra modifier le code en conséquence !!!***

**1 - Configuration de l'ioc**

![pinout](https://github.com/user-attachments/assets/90f39e0a-fe7a-4c96-b8e5-be0f2ea05c86)

On configure un USART pour pouvoir récupérer les trames du Lidar. 

En choisissant USART1 on tombe par défaut sur les pins PC4 et PC5, ce qui pose problème car ils sont aussi liés à PA2 ET PA3 qui représentent l'USART2 qu'on utilise déjà pour débugger.  
Cela peut provoquer des courts-circuits donc on change évidemment les pins de celui-ci. Dans notre cas on atterit alors sur PA9 ET PA10.


![image](https://github.com/user-attachments/assets/aca73b9e-295d-4ee6-870a-59c67b41d228)
