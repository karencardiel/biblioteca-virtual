# Virtual Library Management System

Este proyecto es un sistema de gestión de biblioteca virtual desarrollado en Python, que utiliza los principios de la programación orientada a objetos (POO) para administrar préstamos, inventarios y notificaciones de manera eficiente. El objetivo es proporcionar una experiencia fluida para los usuarios y facilitar la interacción con las publicaciones.

## Características

- Gestión de usuarios y publicaciones.
- Control de préstamos y devoluciones.
- Notificaciones personalizadas.
- Organización modular del código utilizando clases, herencia, encapsulación, polimorfismo y abstracción.
- Sistema extensible con una jerarquía de clases que incluye:
  - 5 clases principales: `Usuario`, `Publicacion`, `Prestamo`, `Notificacion` y `Evento`.
  - 50 subclases específicas que implementan diversas funcionalidades.

## Requisitos

- Python 3.8 o superior.
- Bibliotecas estándar de Python (no se requieren dependencias externas).

## Cómo usarlo

### Opción 1: Ejecutar Localmente

1. Clona este repositorio:

   ```bash
   git clone https://github.com/tuusuario/virtual-library-system.git
   cd virtual-library-system
   ```

2. Ejecuta el script principal del sistema:

   ```bash
   python library_system.py
   ```

3. Interactúa con el menú principal para realizar acciones como:

   - Agregar usuarios.
   - Registrar publicaciones.
   - Solicitar y devolver préstamos.
   - Consultar inventario.
   - Enviar notificaciones.

### Opción 2: Probar en Google Colab

Haz clic en el siguiente enlace para ejecutar el proyecto directamente en Google Colab, sin necesidad de configuraciones adicionales:

[![Abrir en Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SOsZwAiIZhTIvcKijrnvOh2tTXpAQFkM?usp=sharing)

## Principios de POO en el Código

### 1. Encapsulación
Los atributos sensibles están protegidos mediante prefijos de doble guion bajo (`__`) y solo se acceden a través de métodos definidos en las clases. Ejemplo:

```python
class Usuario:
    def __init__(self, nombre, id_usuario):
        self.__nombre = nombre
        self.__id_usuario = id_usuario
```

### 2. Herencia
La estructura del sistema utiliza herencia para promover la reutilización de código. Por ejemplo, varias subclases de `Publicacion` como `Libro` y `Revista` comparten atributos y métodos comunes.

```python
class Libro(Publicacion):
    def consultar_disponibilidad(self):
        return f"El libro '{self._titulo}' está {'disponible' if self._disponible else 'no disponible'}."
```

### 3. Polimorfismo
Los métodos se redefinen en las subclases para proporcionar comportamientos específicos según el contexto.

```python
class NotificacionCorreo(Notificacion):
    def enviar_notificacion(self):
        return f"Enviando correo a {self._usuario}: {self._mensaje}"
```

### 4. Abstracción
Las clases abstractas definen interfaces que deben ser implementadas por sus subclases.

```python
from abc import ABC, abstractmethod

class Notificacion(ABC):
    @abstractmethod
    def enviar_notificacion(self):
        pass
```

## Ejemplo de Interacción

- **Registrar un libro:**
  ```bash
  Opción 2: Agregar publicación.
  Título: "Cien Años de Soledad"
  Autor: "Gabriel García Márquez"
  ```

- **Solicitar un préstamo:**
  ```bash
  Opción 3: Solicitar préstamo.
  Usuario: "Karen Cardiel"
  Publicación: "Cien Años de Soledad"
  ```

- **Consultar disponibilidad:**
  ```bash
  Opción 6: Consultar disponibilidad.
  Resultado: "El libro 'Cien Años de Soledad' está no disponible."
  ```

## Resultados y conclusión

El sistema se desarrolló exitosamente, implementando los pilares de POO y facilitando la gestión eficiente de una biblioteca virtual. Este proyecto también mejoró el entendimiento práctico de conceptos avanzados de POO y motivó la investigación sobre mejores prácticas de diseño de software.

## Créditos

- **Karen Cardiel Olea**  
- **Elisabet Arelly Sulú Vela**  
- Profesor: **Ernesto Manuel Ihuit Dzib**  
- Universidad Politécnica de Yucatán  
- Asignatura: Paradigmas de Programación
**Fecha de entrega:** Octubre 13, 2024

---
**Nota**: Este programa fue desarrollado como parte de un proyecto académico. ¡Esperamos que sea útil para aprender más sobre programación orientada a objetos y la gestión de bibliotecas virtuales!
