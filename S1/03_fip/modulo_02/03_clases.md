# Módulo II - Programción Orientada a Objetos

**Tema central:** Clases y objetos: definición, atributos y métodos

[⬅ Volver](../README.md) 

---

### Clase
Una clase en Java representa la definición formal de una entidad del mundo real dentro del paradigma de la programación orientada a objetos.
Es una estructura que actúa como plantilla para la creación de objetos y permite encapsular datos (atributos) y comportamientos (métodos) relacionados.

> En términos técnicos, una clase define un nuevo tipo de dato compuesto. Por convención, su nombre comienza con mayúscula y, si está compuesto por varias palabras, cada palabra también con mayúscula (CamelCase). Cada clase se guarda en un archivo `.java` que debe tener el mismo nombre que la clase que contiene. Por ejemplo, la clase `Estudiante` debe guardarse en `Estudiante.java`.

### Objeto
Un objeto es una instancia concreta de una clase. Representa una entidad individual en memoria, con valores propios en sus atributos y capacidad para ejecutar métodos definidios en su clase. Todos los objetos comparten la estrucutra de su clase, pero tienen su propio estado. La creación de objetos se realiza mediante el operador `new`, que invoca un constructor de la clase.

ej.
```markdown
Estudiante e1 = new Estudiante();
```

### Atributos
Son variables que representan el estado de un objeto. Se declaran dentro del cuerpo de la clase y su tipo, nombre y visibilidad determinan cómo se accede y manipulan. Por convención, se nombran comenzando en minúscula. Los atributos pueden ser públicos, privados, protegidos o con visibilidad por defecto, y se recomienda que sean privados para proteger la encapsulación.

### Modificacdoes de acceso
Determinarán el nivel de visibilidad de los miembros (atributos/métodos) de una clase desde otras clases. Son fundamentales para garantizar el principio de encapsulamiento.

- public : el mimebro es **accesiblde desde cualquier clase**, sin importar el parquete. Es el nivel de visibilidad más amplio.
  - ej. Un método `public` puede ser llamado desde cualquier parte del programa donde se tenga referencia al objeto.
- private : el miembro es **accesible solo dentro de la propia clase donde fue decladaro**. Es el nivl de visibilidad más restrictivo.
  - ej. Si un atributo es `private`, no puede ser accedido directamente desde otra clase. Se debe usar un método público (getter o setter) para interactuar con él.
- protected : el miembro es accesible desde:
  - Dentro de la misma clase que lo define.
  - En clases del mismo paquete.
  - En subclases, incluso su están en otro paquete.
  - Resulta útil cuando se quiere permitir acceso desde herencia pero restringir desde clases no relacionadas.
- default : cuando no se especifica ningún modificador, se aplica el acceso por defecto (package-private), es decir, el miembro es accesible solo desde clases dentro del mismo paquete.

Se recomienda declarar los atributos como `private` y proporcionar métodos públicos (getters y setters) para acceder y modificarlos de forma controlada. A estos métodos se los denomina:
- Getter : método que devuelve el valor del atributo (`getNombre()`)
- Setter : método que asigna un valor a un atributo (`setNombre(String nombre)`)

### Constructores
Un constructor es un método especial que se utiliza para crear objetos e inicializar sus atributos. **No tiene tipo de retorno (ni siquiera void)**, y su nombre debe coincidir exactamente con el nombre de la clase. Pueden haber varios constructores en una misma clase siempre que tengan distinta firma (sobrecarga).

El contructor puede recibir parámetros para inicializar atributos con valores determinados. Cuando se usan nombres en parámetros iguales a los atributos, se emplaea la palabra clave `this` para referirse al atributo de la instancia.

ej.
```markdown
public Estudiante(String nombre, int codigo) {
    this.nombre = nombre;
    this.condigo = codigo;
}
```

### Métodos
Los métodos definen las operaciones que pueden realizar los objetos de una clase. Se declaran especificando el tipo de retorno, el nombre y los parámetros (si los hay) y el cuerpo del método. Por convención, los nombres de los métodos empiezan con minúscula. Los métodos pueden usar los atributos de la clase para relaizar cálculos, modificar el estado del objeto o devolver información.

ej.
```markdown
public int calcularEdad(int anioActual) {
    return anioActual - this.anioNacimiento;
}
```
### Sobrecarga
La sobrecarga de métodos permite definir múltiples métodos con el mismo nombre, siempre que tengan distinta cantidad o tipo de parámetros. Java distingue los métodos sobrecargados según su firma (nombre + parámetros). No se permite definir métodos con igual firma, ya que el compilador no podría diferenciarlos.

### Importación de clases
Cuando se desea utilizar una clase definida en otro paquete, se debe importar usando la palabra clave `import`, seguida de la ruta del paquete y nombre de la clase. Esto debe ubicarse después del `package` (si lo hay) y antes de la declaración de la clase.

```markdown
import sistema.estudiantes.Estudiante;
```

### Atributos y métodos estáticos
Los atributos `static` pertenecen a la clase, no a sus intancias. Su valor es compartido entre todos los objetos creados a partir de la clase. Se utilizan cuando un valor debe mantenerse común a todas las instancias, como una constante o un contador global.

Los métodos `static` funcionan de forma análoga: pueden ser llamados sin crear un objeto, usando `NombreClase.metodoStatic()`. No pueden acceder directamente a los atributos o métodos de la instancia, ni usar `this`.

### Constantes (final)
Para definir un valor constante que no pueda ser modificado, se usa el modificador `final`. En cambinación con `static`, se crea una constante de clase. Por convención, los nombres de constantes se escriben en mayúsculas con guiones bajos.

ej.
```markdown
public static final double PI = 3.1415;
```

> Un método de instancia puede acceder a: 
> - Atributos y métodos de instancia
> - Atributos y métodos estáticos

> Un método estático solo puede acceder a:
> - Atributos y métodos estáticos
> - No puede usar `this` ni acceder a miembros de instancia directamente


