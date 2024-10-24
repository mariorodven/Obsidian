
```python
import random
import json

def generar_amigo_invisible(participantes):
    # Copiar la lista de participantes para hacer la asignación
    asignaciones = participantes[:]
    
    # Bucle hasta que todos tengan un amigo distinto a ellos mismos
    while True:
        random.shuffle(asignaciones)  # Mezclar las asignaciones
        # Si no hay coincidencias (nadie es su propio amigo), salimos del bucle
        if all(participantes[i] != asignaciones[i] for i in range(len(participantes))):
            break
    
    # Crear el diccionario de participantes y sus amigos invisibles
    amigo_invisible = {participantes[i]: asignaciones[i] for i in range(len(participantes))}
    
    return amigo_invisible

def main():
    # Pedir el número de participantes
    num_participantes = int(input("Introduce el número de participantes: "))
    
    # Pedir los nombres de los participantes
    participantes = []
    for i in range(num_participantes):
        nombre = input(f"Introduce el nombre del participante {i + 1}: ")
        participantes.append(nombre)
    
    # Generar las asignaciones de amigo invisible
    resultado = generar_amigo_invisible(participantes)
    
    # Imprimir el resultado en formato JSON
    print(json.dumps(resultado, indent=4))

if __name__ == "__main__":
    main()
```

### Explicación del código:

1. **Entrada de datos**: El programa primero pide el número de participantes y luego sus nombres a través de la terminal.
    
2. **Mezcla de nombres**: La función `random.shuffle()` mezcla los nombres de los participantes hasta que ningún participante quede asignado a sí mismo.
    
3. **Generación del diccionario**: El diccionario resultante asigna a cada participante su respectivo amigo invisible.
    
4. **Formato JSON**: Finalmente, el diccionario se imprime en formato JSON utilizando `json.dumps()`.
    

### Ejemplo de uso:
```bash
Introduce el número de participantes: 4
Introduce el nombre del participante 1: Carlos
Introduce el nombre del participante 2: Ana
Introduce el nombre del participante 3: Luis
Introduce el nombre del participante 4: María
```

### Salida en formato JSON:
```json
{
    "Carlos": "Luis",
    "Ana": "María",
    "Luis": "Carlos",
    "María": "Ana"
}
```

Este código es una manera sencilla de generar las asignaciones de amigo invisible en Python y funciona bien para cualquier cantidad de participantes.