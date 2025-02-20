# Adaptación del Juego Snake Usando una Cola (Queue) con Arreglo

Esta guía explica paso a paso cómo se adapta el clásico juego *Snake* para utilizar una **Cola** (*Queue*) implementada mediante un arreglo.

La idea principal es gestionar el cuerpo de la serpiente como una secuencia donde:

- **El primer elemento** del arreglo representa la cola (*tail*) de la serpiente.
- **El último elemento** representa la cabeza (*head*) de la serpiente.

---

## 1. La Clase Cola

La clase `Cola` encapsula la estructura de datos y provee métodos para:

- **Agregar elementos (`enqueue`)**: Se añade al final del arreglo.
- **Eliminar elementos (`dequeue`)**: Se remueve el primer elemento, simulando el avance de la serpiente.
- **Obtener la cabeza (`peekTail`)**: Permite obtener el último elemento, que representa la posición actual de la cabeza.
- **Convertir a arreglo (`toArray`)**: Facilita recorrer y dibujar cada segmento.
- **Obtener la longitud (`length`)**: Indica el número de elementos actuales en la cola.

### Implementación en JavaScript

```javascript
class Cola {
  constructor() {
    this.items = [];
  }
  
  enqueue(element) {
    this.items.push(element);
  }
  
  dequeue() {
    return this.items.shift();
  }
  
  peekTail() {
    return this.items[this.items.length - 1];
  }
  
  toArray() {
    return this.items;
  }
  
  get length() {
    return this.items.length;
  }
}
```

---



