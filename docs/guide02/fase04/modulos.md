# Módulos del Prototipo POS Restaurante

A continuación se describen los módulos principales del sistema POS, su funcionalidad, entradas, salidas y opciones disponibles.

---

## 1️⃣ Gestión de Mesas
**Objetivo:** Administrar visualmente las mesas del restaurante.  

**Opciones principales:**
- Abrir Mesa
- Cerrar Mesa

**Entrada:** Selección de mesa por parte del mozo.  
**Salida:** Estado actualizado de la mesa (Disponible/Ocupada).

---

## 2️⃣ Toma y Envío de Pedidos
**Objetivo:** Registrar los pedidos de los clientes y enviarlos a cocina de forma eficiente.  

**Opciones principales:**
- Selección de platos del menú
- Agregar cantidad y observaciones
- Enviar pedido a cocina

**Entrada:** Mesa ocupada y selección de productos.  
**Salida:** Pedido registrado y visible en cocina.

---

## 3️⃣ Comunicación con Cocina
**Objetivo:** Mostrar los pedidos pendientes y actualizar su estado cuando estén listos para entregar.  

**Opciones principales:**
- Ver pedidos pendientes
- Marcar pedidos como “Listo para entregar”

**Entrada:** Pedidos enviados desde los mozos.  
**Salida:** Estado actualizado del pedido visible para el mozo.

---

## 4️⃣ Menú (Solo Lectura)
**Objetivo:** Permitir la consulta rápida del menú de platos y sus precios.  

**Opciones principales:**
- Consultar categorías de platos
- Consultar precios y descripciones

**Entrada:** Solicitud de información por parte del mozo.  
**Salida:** Información del menú visible en pantalla.

---

## 5️⃣ Generación de Cuenta y Cierre
**Objetivo:** Calcular el total de la cuenta, registrar el pago y liberar la mesa.  

**Opciones principales:**
- Calcular subtotal de pedidos
- Registrar pago simple
- Cambiar estado de la mesa a Disponible

**Entrada:** Pedidos consumidos en la mesa.  
**Salida:** Total de la cuenta, pago registrado y mesa disponible.

---

## Diagrama de Módulos (Gráfico)

![Diagrama de módulos POS Restaurante](Diagrama_Restaurante%20POS.png)



