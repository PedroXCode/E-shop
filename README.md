# 🛒 Zaldrion E-Shop Simulator

Una aplicación de consola en C# que simula las operaciones principales de una tienda en línea (E-Shop). El proyecto implementa lógica de negocio, manejo de inventario, simulación de cliente con presupuesto y una interfaz de usuario basada en menús robustos con paginación, ordenamiento y búsqueda.

## ✨ Características Principales

Este simulador está diseñado para demostrar la programación orientada a objetos (POO) y la manipulación segura de datos de entrada en un entorno de consola.

* **Simulación de Cliente:**
    * El usuario inicia la sesión con un **presupuesto** definido.
    * Calcula y rastrea el total del carrito y el balance restante en tiempo real.
* **Gestión de Inventario Dinámico:**
    * Carga inicial de productos desde un archivo externo (`inventory.txt`) o utiliza datos por defecto si el archivo no existe o es inválido.
    * El stock se actualiza tras cada compra exitosa.
* **Navegación Avanzada:**
    * **Paginación:** Muestra listas de artículos gestionables por páginas.
    * **Ordenamiento:** Permite ordenar el inventario o el carrito por campos como Nombre, Precio, Rating y Fecha (ascendente/descendente).
    * **Búsqueda/Filtro:** Permite filtrar artículos por nombre o descripción.
* **Lógica Transaccional Segura:**
    * El proceso de **Añadir al Carrito** valida el stock disponible.
    * El **Checkout** (`H`) realiza la validación final del presupuesto y el stock antes de confirmar la compra y actualizar el inventario.
* **Interfaz de Usuario (UX):**
    * Utiliza una clase `InputHelper` para validar rigurosamente toda la entrada de usuario, asegurando que los números estén dentro de rangos y las opciones sean válidas.

## 🛠️ Tecnologías

* **Lenguaje:** C#
* **.NET:** Aplicación de Consola
* **Estructuras de Datos Avanzadas:** Uso de `Dictionary<Item, int>` para manejar el carrito y el inventario, y clases `IComparable` / `IComparer` para la lógica de ordenamiento.

## 🏁 Cómo Empezar

### 📄 Requisitos

* [SDK de .NET](https://dotnet.microsoft.com/es-es/download) (Se recomienda la versión más reciente compatible).

### ⚙️ Instalación y Ejecución

1.  **Clonar el repositorio:**
    ```sh
    git clone [https://github.com/PedroXCode/E-shop.git](https://github.com/PedroXCode/E-shop.git)
    ```
2.  **Navegar al directorio principal:**
    ```sh
    cd E-shop/src 
    ```
3.  **Ejecutar la aplicación:**
    ```sh
    dotnet run
    ```
    *(La aplicación se iniciará y te pedirá tu presupuesto inicial.)*

### 📁 Formato del Archivo de Inventario (`inventory.txt`)

Si deseas cargar tu propio inventario, crea un archivo llamado `inventory.txt` en el mismo directorio de ejecución de la aplicación (usualmente `bin/Debug/netX.X/` de tu proyecto) y usa el siguiente formato, separado por punto y coma (`;`):

| Campo | Descripción | Ejemplo |
| :--- | :--- | :--- |
| **Nombre** | Nombre del producto. | `Mouse Gamer` |
| **Descripción** | Breve descripción. | `Mouse óptico RGB` |
| **Precio** | Precio con punto decimal. | `24.99` |
| **Rating** | Calificación (entero 1-5). | `4` |
| **Fecha** | Fecha de ingreso (YYYY-MM-DD). | `2025-03-10` |
| **Stock** | Cantidad en inventario. | `15` |

**Ejemplo de línea en `inventory.txt`:**
