# SimplePOS System

A Point of Sale (POS) system developed in Java with desktop GUI, designed to manage sales, inventory, customers, and generate reports.

## 🚀 Features

- **Sales Management**: Registration and processing of sales with multiple products
- **Inventory Management**: Product control with stock and pricing
- **Customer Management**: Customer database with complete information
- **Reports**: Generation of sales reports by dates
- **Graphical Interface**: Intuitive user interface developed with Java Swing
- **Database**: MySQL integration for data persistence
- **MVC Architecture**: Implementation of the Model-View-Controller pattern

## 🛠️ Technologies Used

- **Java**: Main programming language
- **Java Swing**: For graphical user interface
- **MySQL**: Database for data storage
- **JDBC**: Database connectivity
- **Maven**: Dependency management and project building
- **JCalendar**: Date selection component for reports

## 📋 Prerequisites

- Java JDK 22 or higher
- Maven 3.6+
- MySQL Server 8.0+
- Git

## 🗄️ Database Structure

The system uses the following main tables:
- **customers**: Customer information
- **products**: Product catalog and inventory
- **sales**: Transaction records
- **sale_details**: Product details per sale

## 🏗️ Project Architecture

```
src/main/java/
├── com.mycompany.proyectopoo/
│   └── ProyectoPOO.java          # Main class
├── Configuracion/
│   └── CConexion.java            # Database configuration
├── Controlador/
│   ├── ControladorCliente.java   # Customer logic
│   ├── ControladorProducto.java  # Product logic
│   ├── ControladorVenta.java     # Sales logic
│   └── ControladorReportes.java  # Reports logic
├── Formularios/
│   ├── FrmMenuPrincipal.java     # Main menu
│   ├── FrmClientes.java          # Customer management
│   ├── FrmProducto.java          # Product management
│   ├── FrmVentas.java           # Sales registration
│   ├── FrmReportesFechas.java   # Date reports
│   └── FrmBuscarComprobante.java # Receipt search
└── Modelo/
    ├── ModeloCliente.java        # Customer data model
    ├── ModeloProducto.java       # Product data model
    └── PorPagar.java            # Pending payments model
```

## 🚀 Installation and Setup

### 1. Clone the repository
```bash
git clone https://github.com/EstebanCanVaz/SimplePOS-System.git
cd SimplePOS-System
```

### 2. Configure the database
1. Create a MySQL database named `simplepos`
2. Import the database schema (provided SQL file)
3. Configure credentials in `Configuracion/CConexion.java`

### 3. Compile and run
```bash
# Compile the project
mvn clean compile

# Run the application
mvn exec:java
```

## 📖 System Usage

### Main Menu
- **Customers**: Manage customer information
- **Products**: Administer inventory and products
- **Sales**: Register new sales
- **Reports**: Generate sales reports by dates

### Sales Management
1. Select customer from the list
2. Search and add products to cart
3. Specify quantities
4. Process payment
5. Generate receipt

### Reports
- Filtered by specific dates
- Data export
- Total sales visualization

## 🔧 Database Configuration

Make sure to properly configure the MySQL connection in `Configuracion/CConexion.java`:

```java
// Configuration example
private static final String URL = "jdbc:mysql://localhost:3306/simplepos";
private static final String USER = "your_username";
private static final String PASSWORD = "your_password";
```

## 📝 Main Features

### CRUD Operations
- **Create**: Create new customers, products and sales
- **Read**: Query customer, product and sales information
- **Update**: Update customer and product data
- **Delete**: Delete records (with validations)

### Reports and Queries
- Sales reports by date range
- Receipt search
- Sales statistics

## 🤝 Contributing

1. Fork the project
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 👥 Authors

- **Esteban Canto** - *Initial development* - [EstebanCanVaz](https://github.com/EstebanCanVaz)

## 🙏 Acknowledgments

- NetBeans IDE for the development environment
- MySQL for the database
- JCalendar for the date component 