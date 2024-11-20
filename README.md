!!! Le PCB réalisé pour le V-NOM n'utilise pas le même µP que la STM32 qu'on utilise pour tester le lidar, il faut bien garder ça en tête et il faudra modifier le code en conséquence !!!

#Configuration de l'ioc

On configure un USART pour pouvoir récupérer les trames du Lidar. 

En choisissant USART1 on tombe par défaut sur les pins PC4 et PC5, ce qui pose problème car ils sont aussi liés à PA2 ET PA3 qui représentent l'USART2 qu'on utilise pour débugger.  
Cela peut provoquer des courts-circuits donc on change évidemment les pins de celui-ci. Dans notre cas on atterit alors sur PA9 ET PA10.


