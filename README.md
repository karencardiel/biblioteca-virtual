# 📚 Virtual Library Management System

This project is a virtual library management system developed in Python, which uses object-oriented programming (OOP) principles to efficiently manage loans, inventory, and notifications. The goal is to provide a smooth experience for users and facilitate interaction with publications.

## ✨ Features

- 👥 User and publication management
- 📖 Loan and return control
- 🔔 Personalized notifications
- 🏗️ Modular code organization using classes, inheritance, encapsulation, polymorphism, and abstraction
- 🔧 Extensible system with a class hierarchy that includes:
  - **5 main classes**: `Usuario`, `Publicacion`, `Prestamo`, `Notificacion`, and `Evento`
  - **50 specific subclasses** that implement various functionalities

## 📋 Requirements

- Python 3.8 or higher
- Python standard libraries (no external dependencies required)

## 🚀 How to Use

### Option 1: Run Locally

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/virtual-library-system.git
   cd virtual-library-system
   ```

2. Run the main system script:
   ```bash
   python library_system.py
   ```

3. Interact with the main menu to perform actions such as:
   - ➕ Add users
   - 📚 Register publications
   - 🔄 Request and return loans
   - 📊 Check inventory
   - 📧 Send notifications

### Option 2: Try on Google Colab

Click the following link to run the project directly in Google Colab, without additional setup:

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SOsZwAiIZhTIvcKijrnvOh2tTXpAQFkM?usp=sharing)

## 🏛️ OOP Principles in the Code

### 1. 🔒 Encapsulation
Sensitive attributes are protected using double underscore prefixes (`__`) and are only accessed through methods defined in the classes. Example:

```python
class Usuario:
    def __init__(self, nombre, id_usuario):
        self.__nombre = nombre
        self.__id_usuario = id_usuario
```

### 2. 👨‍👩‍👧‍👦 Inheritance
The system structure uses inheritance to promote code reusability. For example, several subclasses of `Publicacion` like `Libro` and `Revista` share common attributes and methods.

```python
class Libro(Publicacion):
    def consultar_disponibilidad(self):
        return f"The book '{self._titulo}' is {'available' if self._disponible else 'not available'}."
```

### 3. 🎭 Polymorphism
Methods are redefined in subclasses to provide specific behaviors according to context.

```python
class NotificacionCorreo(Notificacion):
    def enviar_notificacion(self):
        return f"Sending email to {self._usuario}: {self._mensaje}"
```

### 4. 🎨 Abstraction
Abstract classes define interfaces that must be implemented by their subclasses.

```python
from abc import ABC, abstractmethod

class Notificacion(ABC):
    @abstractmethod
    def enviar_notificacion(self):
        pass
```

## 💡 Interaction Examples

### 📖 Register a Book
```bash
Option 2: Add publication
Title: "One Hundred Years of Solitude"
Author: "Gabriel García Márquez"
```

### 🔄 Request a Loan
```bash
Option 3: Request loan
User: "Karen Cardiel"
Publication: "One Hundred Years of Solitude"
```

### 📊 Check Availability
```bash
Option 6: Check availability
Result: "The book 'One Hundred Years of Solitude' is not available."
```

## 🎯 System Architecture

| Component | Description |
|-----------|-------------|
| **Main Classes** | Core system functionality |
| **Subclasses** | Specialized implementations |
| **Interfaces** | Abstract method definitions |
| **Inheritance Tree** | Hierarchical class relationships |

## 📂 File Structure
```
virtual-library-system/
├── 📝 library_system.py
├── 👥 usuario.py
├── 📚 publicacion.py
├── 🔄 prestamo.py
├── 🔔 notificacion.py
├── 📅 evento.py
└── 📖 README.md
```

## 🏆 Results and Conclusion

The system was successfully developed, implementing OOP pillars and facilitating efficient management of a virtual library. This project also improved practical understanding of advanced OOP concepts and motivated research on software design best practices.

## 👥 Credits

- **Karen Cardiel Olea**
- **Elisabet Arelly Sulú Vela**
- Professor: **Ernesto Manuel Ihuit Dzib**
- Universidad Politécnica de Yucatán
- Subject: Programming Paradigms

## 📅 Submission Date

October 13, 2024

---

**Note:** This program was developed as part of an academic project. We hope it's useful for learning more about object-oriented programming and virtual library management! 🎓

⭐ **Star this repository if you find it helpful!**
