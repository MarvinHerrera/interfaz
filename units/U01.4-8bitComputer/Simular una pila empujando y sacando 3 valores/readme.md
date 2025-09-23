### HERRERA MIRANDA MARVIN JAVIER 23210602  

## PRACTICA 8BITS: SIMULACIÓN DE PILA EMPUJANDO Y SACANDO 3 VALORES  

```asm
; PRACTICA: Simulación de pila con 3 valores
;
; Empuja tres valores a la pila y luego los extrae
; Mostrando en el display cada valor en orden inverso

start:
    clra
    data SP, 0xFF      ; inicializamos el puntero de pila al final de memoria (255)

    ; --- Empujar valores ---
    data Ra, 10        ; primer valor
    push Ra

    data Ra, 20        ; segundo valor
    push Ra

    data Ra, 30        ; tercer valor
    push Ra

    ; --- Extraer valores (LIFO) ---
    pop Rd             ; debería mostrar 30
    pop Rd             ; debería mostrar 20
    pop Rd             ; debería mostrar 10

end:
    hlt                ; detener ejecución
