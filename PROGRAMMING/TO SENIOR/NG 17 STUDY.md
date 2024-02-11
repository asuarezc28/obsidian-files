-SIGNALS
zone.js es sustituido, que se usaba para detección de cambios
zone.js recorría todos los componentes
onpush --> los componentes que tu le especificabas cambiaban y no era eficiente y era engorroso
ES UN MODELO DE REACTIVIDAD : ES COMO VAMOS A MANEJAR LOS CAMBIOS EN MI APP, 
SIGNALS RECONOCE EL COMPONENTE QUE CAMBIÓ
![[Pasted image 20240201215717.png]]

cumple dos funciones:
-guarda un valor
-notificar cuando este valor fue cambiado
-almacena primitivos y array de objetos

3 METODOS PARA MODIFICAR EL VALOR
![[Pasted image 20240201220042.png]]
![[Pasted image 20240201220212.png]] 
![[Pasted image 20240201220658.png]]


SEÑAL COMPUTADA, LA PAPÁ
no tiene metodos de cambio, su valor cambia cuando hay una signal dependiente
![[Pasted image 20240201220853.png]]
se queda escuchando y si cambia y es igual a favorito, se modifica:
![[Pasted image 20240201221126.png]]

EFFECT
![[Pasted image 20240201221222.png]]