# Módulo II - Programción Orientada a Objetos
**Licenciatura en Tecnologías de la Información (Plan 2024)**

**Tema central:** Introducción a POO

[⬅ Volver](../README.md) 

---

## 🔹 Introducción
La POO es un paradigma que modela el software mediante objetos, los 
cuales representan entidades del mundo real. Los objetos son instancias 
de clases, y cada uno posee tres elementos fundamentales:

- Estado: representa los datos o atributos del objeto.
- Comportamiento: conjunto de métodos que definen las acciones que el objeto puede ejecutar.
- Identidad: Permite distinguir a un objeto de otros, incluso si comparten estado.

Este paradigma promueve la modularidad, reutilización de código, 
mantenibilidad y escalabilidad del software mediante el uso de 
objetos interactuantes que intercambian mensajes.

---

## 🔹 Conceptos funcamentales de la POO

### Abstracción
Proceso mediante el cual se seleccionan las características esenciales 
de un objeto, ignorando detalles irrelevaltes para el contexto. Esto 
permite modelar problemas complejos enfocándonos únicamente en la
información relevante del dominio (contexto).

### Encapsulamiento
Principio que consiste en ocultar los atributos internos de un objeto,
restringiendo su acceso desde el exterior. El acceso a dichos datos se
controla mediante métodos públicos (getters/setters), manteniendo la 
integridad del estado.

### Herencia
Mecanismo que permite definir una clase derivada (subclase) basada en otra clase existente (superclase), heredando todos sus atributos y métodos. La subclase puede añadir o redefinir funcionalidades específicas. Favorece la reutilización de código y la extensión de funcionalidades sin duplicación.

### Polimorfismo
Capacidad de un mismo método para operar de formas distintas dependiendo del tipo del objeto que lo invoca. Requiere una relación jeráquica mediante herencia. Puede ser:
- Sobreescritura (overriding): redefinir un método heredado.
- Sobrecarga (overloading): definir múltiples métodos con el mismo nombre, pero con diferente firma (parámetros).

### Instanciación
Es la creación de un objeto a partir de una clase. Al instanciar una clase, se obtiene un ejemplar con atributos y métodos definidos, pero con valores propios de cada objeto.

---

## Etapas del desarrollo Orientado a Objetos

### Análisis del sistema
Fase en la que se identifican los objetos del dominio relevantes y sus relaciones. Se construye un modelo conceptual que representa los elementos significativos del problema a resolver, prescindiendo de aquellos no pertinentes.

### Diseño del sistema
Transforma el modelo conceptual en clases concretascon sus atributos y métodos. Se definen las estructuras de datos, relaciones entre clases y la lógica de interacción entre ellas.

### Implementación del sistema
Consiste en codificar las clases diseñadas utilizando un lenguaje de programación orientado a objetos. Aquí se definen los métodos (comportamientos) y se asignan valores iniciales a los atributos (estado).

---


