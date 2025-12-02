# E-shop

E‑shop Simulator
Un simulador de tienda online en C# (consola) que permite gestionar inventario, carrito de compras y presupuesto del cliente. El programa reproduce la experiencia de un e‑commerce básico directamente en la terminal.
🚀 Características principales
- Inventario dinámico: carga desde archivo inventory.txt o usa un inventario por defecto.
- Gestión de artículos: cada producto tiene nombre, descripción, precio, rating y fecha de alta.
- Carrito de compras: añadir, remover y visualizar artículos con control de stock.
- Presupuesto del cliente: el sistema valida que las compras no excedan el presupuesto disponible.
- Checkout seguro: actualiza inventario y presupuesto tras la compra.
- Interfaz interactiva: menús en consola con opciones de búsqueda, ordenación y paginación.
- Ordenación flexible: por nombre, precio, descripción, rating o fecha (ascendente/descendente).
📂 Estructura del proyecto
E-shop/
 └── src/
     └── Program.cs   # Código principal con toda la lógica
     └── inventory.txt (opcional) # Archivo de inventario externo


🛠️ Requisitos
- .NET 6.0 o superior
- Consola compatible con UTF‑8 (para caracteres y símbolos)
▶️ Ejecución
- Clona el repositorio:
git clone https://github.com/PedroXCode/E-shop.git
cd E-shop/src
- Compila y ejecuta:
dotnet run
- Introduce tu presupuesto inicial y comienza a comprar.
📑 Ejemplo de inventario (inventory.txt)
Formato esperado:
Nombre;Descripción;Precio;Rating;Fecha;Stock
Mouse Gamer;Mouse RGB;24.99;4;2025-03-10;15
Teclado Mecánico;Switches blue;54.99;5;2025-01-22;10


🎮 Uso básico
- [N] Página siguiente / [P] Página anterior
- [B] Buscar artículos
- [O] Ordenar inventario
- [A] Añadir al carrito
- [C] Ir al carrito
- [R] Remover del carrito
- [H] Checkout
- [E] Salir
