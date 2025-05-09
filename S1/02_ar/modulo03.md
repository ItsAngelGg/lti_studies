#  Módulo III – Especificación y Documentación  
**Licenciatura en Tecnologías de la Información (Plan 2024)**  
**Tema central:** Ingeniería de Requerimientos – Etapa de Especificación

---

## 🔹 1. Especificación en Ingeniería de Requerimientos

- Es parte del proceso iterativo que incluye:  
  **Recopilación → Especificación → Validación**.
- Busca documentar los requisitos del usuario y del sistema.
- Los requisitos deben ser:
  - Claros
  - Sin ambigüedades
  - Comprensibles
  - Completos
  - Consistentes

> ❗ Sin embargo, lograr esto en la práctica es difícil por diferencias de interpretación entre los interesados.

---

## 🔹 2. Notaciones para la Especificación

###  Texto libre en lenguaje natural
- Muy común para requisitos de usuario.
- Ejemplo:  
  > El sistema debe permitir buscar libros por título, autor o ISBN.

---

###  Lenguaje natural estructurado
- Uso de plantillas estándar para definir requisitos.

####  Historias de Usuario
Estructura:  
> **Como** [rol]  
> **Quiero** [funcionalidad]  
> **Para** [beneficio]

**Ejemplo:**
```markdown
**Título:** Solicitar préstamo de un libro  
**Descripción:**  
Como usuario  
Quiero solicitar el préstamo de un libro  
Para poder leer su contenido  
**Criterios de aceptación:**
- El usuario busca el libro
- Verificación de límite de préstamos
- Confirmación y registro del préstamo
```

####  Casos de Uso
Definidos por:  
- Actor principal  
- Precondiciones  
- Flujos principal y alternativo  
- Postcondiciones  
- Requisitos especiales

**Ejemplo: Prestar un libro**
```markdown
**Actor:** Usuario  
**Precondiciones:** Usuario autenticado, libro disponible  
**Flujo principal:**
1. Usuario busca y selecciona un libro
2. Sistema verifica condiciones
3. Se registra y confirma el préstamo
**Flujo alternativo:** Usuario excede límite de libros prestados
**Postcondiciones:** Libro marcado como prestado, envío de email de confirmación
```

---

## 🔹 3. Notaciones Gráficas

- Se usan para complementar y visualizar mejor los requisitos.
- Ejemplos:
  - Diagramas de Casos de Uso (UML)
  - Diagramas de Secuencia (UML)


