``` mermaid
classDiagram
    Persona --|> Empleado
    Persona --|> Cliente
    Empleado"0..*" -- "0..*" Directivo : subordinado
    Empresa --|> Empleado
    Directivo --|> Empleado
    Cliente--|> Empresa

    class Persona{
        -Nombre : String
        -Edad : Integer
        +Mostrar() void
    }

    class Empleado{
        -SueldoBruto : Integer
        -Caluclar_salarioneto : Integer
        +Mostrar() void
    }
    
    class Cliente{
        -telefono : integer
        +Mostrar() void
    }

    class Empresa{
        -Nombre : String
        -Cif :String
    }
    class Directivo{
        +categoria : String
        +Mostrar()
    }
```