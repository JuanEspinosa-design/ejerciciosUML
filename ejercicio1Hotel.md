```mermaid
classDiagram

    class Hotel {
        -string nombre
        -vector<Habitacion> habitaciones
        -vector<Cliente*> clientes
        +Hotel(string n)
        +void agregarHabitacion(int, string)
        +void registrarCliente(Cliente* cliente)
        +void mostrarHabitaciones() const
        +void mostrarClientes() const
    }

    class Habitacion {
        -int numero
        -string tipo
        -bool ocupada
        +Habitacion(int numero, string tipo)
        +int getNumero() const
        +string getTipo() const
        +bool estaOcupada() const
        +void ocupar()
        +void desocupar()
    }

    class Cliente {
        -int id
        -string nombre
        +Cliente(int i, string n)
        +int getId() const
        +string getNombre() const
    }

    Hotel *-- Habitacion 
    Hotel o-- Cliente
```
