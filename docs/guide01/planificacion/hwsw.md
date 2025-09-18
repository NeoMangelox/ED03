# Requisitos de Hardware y Software
En esta sección se detallan los recursos técnicos necesarios para el desarrollo del sistema POS para restaurantes. Se especifican tanto las características de hardware mínimas como el software de soporte asignado a las distintas actividades del proyecto.  

## Hardware
- **Servidor local (Base de datos)**  
  - PC con **Windows 11** (o Windows 10 actualizado) y al menos 16 GB de RAM.
	- Si se necesita compilar para Android/iOS, se requiere:
	    - **Android SDK** (emulador Android, al menos 8 GB RAM).
	    - **Mac** (opcional, solo si se va a compilar para iOS).
- **Estaciones de trabajo (desarrollo y pruebas)**  
  - Procesador: Intel i5 o superior  
  - Memoria RAM: 8 GB mínimo  
  - Almacenamiento: 256 GB SSD  
  - Conexión a internet estable (mínimo 5 Mbps)  
- **Dispositivos de operación (uso en restaurante)**  
  - Tablets o smartphones Android (Android 10 o superior, 3 GB RAM mínimo) para mozos y cocina.

## Software
Se agrupan según la etapa del desarrollo:  

- **Sistema Operativo**  
  - Windows 10/11 para estaciones de trabajo  
  - Ubuntu Server 22.04 para el servidor de base de datos (opcional)  

- **Lenguajes de Programación**  
  - **frontend + backend:** C# con .NET 7/8 y MAUI para el frontend multiplataforma y la lógica de negocio.

- **Entorno de Desarrollo**  
  - IDE principal: **Visual Studio 2022** (Community)
  - Framework: .NET MAUI

- **Control de Versiones**  
  - Git + GitHub para repositorio remoto y control de versiones  

- **Base de Datos**  
  - MySQL

- **Herramientas de Gestión**  
  - ProjectLibreIA
