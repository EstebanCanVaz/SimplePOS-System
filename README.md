# SimplePOS System

Un sistema de punto de venta (POS) desarrollado en Java con interfaz gráfica de escritorio, diseñado para gestionar ventas, inventario, clientes y generar reportes.

## 🚀 Características

- **Gestión de Ventas**: Registro y procesamiento de ventas con múltiples productos
- **Gestión de Inventario**: Control de productos con stock y precios
- **Gestión de Clientes**: Base de datos de clientes con información completa
- **Reportes**: Generación de reportes de ventas por fechas
- **Interfaz Gráfica**: Interfaz de usuario intuitiva desarrollada con Java Swing
- **Base de Datos**: Integración con MySQL para persistencia de datos
- **Arquitectura MVC**: Implementación del patrón Modelo-Vista-Controlador

## 🛠️ Tecnologías Utilizadas

- **Java**: Lenguaje principal del proyecto
- **Java Swing**: Para la interfaz gráfica de usuario
- **MySQL**: Base de datos para almacenamiento de datos
- **JDBC**: Conectividad con la base de datos
- **Maven**: Gestión de dependencias y construcción del proyecto
- **JCalendar**: Componente para selección de fechas en reportes

## 📋 Requisitos Previos

- Java JDK 22 o superior
- Maven 3.6+
- MySQL Server 8.0+
- Git

## 🗄️ Estructura de la Base de Datos

El sistema utiliza las siguientes tablas principales:
- **clientes**: Información de clientes
- **productos**: Catálogo de productos e inventario
- **ventas**: Registro de transacciones
- **detalle_ventas**: Detalle de productos por venta

## 🏗️ Arquitectura del Proyecto

```
src/main/java/
├── com.mycompany.proyectopoo/
│   └── ProyectoPOO.java          # Clase principal
├── Configuracion/
│   └── CConexion.java            # Configuración de base de datos
├── Controlador/
│   ├── ControladorCliente.java   # Lógica de clientes
│   ├── ControladorProducto.java  # Lógica de productos
│   ├── ControladorVenta.java     # Lógica de ventas
│   └── ControladorReportes.java  # Lógica de reportes
├── Formularios/
│   ├── FrmMenuPrincipal.java     # Menú principal
│   ├── FrmClientes.java          # Gestión de clientes
│   ├── FrmProducto.java          # Gestión de productos
│   ├── FrmVentas.java           # Registro de ventas
│   ├── FrmReportesFechas.java   # Reportes por fechas
│   └── FrmBuscarComprobante.java # Búsqueda de comprobantes
└── Modelo/
    ├── ModeloCliente.java        # Modelo de datos de clientes
    ├── ModeloProducto.java       # Modelo de datos de productos
    └── PorPagar.java            # Modelo de pagos pendientes
```

## 🚀 Instalación y Configuración

### 1. Clonar el repositorio
```bash
git clone https://github.com/tu-usuario/SimplePOS-System.git
cd SimplePOS-System
```

### 2. Configurar la base de datos
1. Crear una base de datos MySQL llamada `simplepos`
2. Importar el esquema de la base de datos (archivo SQL proporcionado)
3. Configurar las credenciales en `Configuracion/CConexion.java`

### 3. Compilar y ejecutar
```bash
# Compilar el proyecto
mvn clean compile

# Ejecutar la aplicación
mvn exec:java
```

## 📖 Uso del Sistema

### Menú Principal
- **Clientes**: Gestionar información de clientes
- **Productos**: Administrar inventario y productos
- **Ventas**: Registrar nuevas ventas
- **Reportes**: Generar reportes de ventas por fechas

### Gestión de Ventas
1. Seleccionar cliente desde la lista
2. Buscar y agregar productos al carrito
3. Especificar cantidades
4. Procesar el pago
5. Generar comprobante

### Reportes
- Filtrado por fechas específicas
- Exportación de datos
- Visualización de ventas totales

## 🔧 Configuración de la Base de Datos

Asegúrate de configurar correctamente la conexión a MySQL en `Configuracion/CConexion.java`:

```java
// Ejemplo de configuración
private static final String URL = "jdbc:mysql://localhost:3306/simplepos";
private static final String USER = "tu_usuario";
private static final String PASSWORD = "tu_password";
```

## 📝 Funcionalidades Principales

### CRUD Operations
- **Create**: Crear nuevos clientes, productos y ventas
- **Read**: Consultar información de clientes, productos y ventas
- **Update**: Actualizar datos de clientes y productos
- **Delete**: Eliminar registros (con validaciones)

### Reportes y Consultas
- Reportes de ventas por rango de fechas
- Búsqueda de comprobantes
- Estadísticas de ventas

## 🤝 Contribuir

1. Fork el proyecto
2. Crear una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abrir un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 👥 Autores

- **Esteban Canto** - *Desarrollo inicial* - [EstebanCanVaz](https://github.com/EstebanCanVaz)

## 🙏 Agradecimientos

- NetBeans IDE por el entorno de desarrollo
- MySQL por la base de datos
- JCalendar por el componente de fechas 