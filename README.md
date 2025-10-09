# 📘 Sistema de Gestión de Tutorías  
### Parcial 2 - Programación Orientada a Objetos  
**Autor:** Juan Pablo Camacho 
**Fecha:** Octubre 2025  

---

## 🧩 Descripción General  
Este proyecto implementa un **Sistema de Gestión de Tutorías** en Python, diseñado para demostrar los principios de la **Programación Orientada a Objetos (POO)** y el uso de una **base de datos SQLite** para la persistencia de datos.  

El sistema permite **registrar usuarios (tutores y estudiantes)**, **ofrecer sesiones de tutoría**, **reservarlas**, y **visualizar todas las sesiones disponibles** mediante una **interfaz de consola interactiva**.

---

## ⚙️ Funcionalidades Principales  

1. **Registrar Usuario**  
   - Permite registrar tanto tutores como estudiantes.  
   - Validación de datos y control de duplicidad de correos.  

2. **Tutor: Ofrecer Sesión de Tutoría**  
   - El tutor selecciona una materia y define fecha/hora de la tutoría.  
   - Las sesiones quedan disponibles para ser reservadas.  

3. **Estudiante: Reservar Sesión**  
   - El estudiante puede ver todas las sesiones disponibles y reservar una.  
   - El estado de la sesión cambia automáticamente a *“reservada”*.  

4. **Ver Sesiones Disponibles**  
   - Muestra todas las sesiones que aún no han sido reservadas.  

5. **Salir del Sistema**  
   - Permite cerrar el programa de forma ordenada.  

---

## 🧠 Conceptos de Programación Orientada a Objetos Aplicados  

### 🔹 Herencia  
- **Clase padre:** `Usuario`  
- **Clases hijas:** `Tutor` y `Estudiante`  
- Uso de `super()` para invocar el constructor de la clase padre.  

### 🔹 Polimorfismo  
- Método sobrescrito: `puede_reservar()`  
  - En `Tutor` → retorna `False`  
  - En `Estudiante` → retorna `True`  
- Permite verificar de forma automática quién puede reservar sesiones.  

### 🔹 Encapsulamiento  
- Métodos que controlan el acceso a la base de datos y la validación de entradas del usuario.  

---

## 🗄️ Base de Datos (SQLite)  

El sistema utiliza un archivo llamado **`tutorias.db`**, que se crea automáticamente al ejecutar el programa.  
Se implementan tres tablas principales:

| Tabla | Descripción |
|-------|--------------|
| `usuarios` | Guarda los datos de tutores y estudiantes. |
| `materias` | Contiene las materias disponibles para las tutorías. |
| `sesiones` | Registra las tutorías ofrecidas, reservadas o disponibles. |

### 📚 Materias precargadas:
- Matemáticas  
- Física  
- Química  
- Programación  
- Inglés  
- Estadística  
- Cálculo  
- Álgebra Lineal  

---



