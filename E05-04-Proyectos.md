classDiagram
    Proyecto o-- Ciclo : 1..*
    Ciclo -- Ejecutable
    Ciclo o-- Fase
    Fase o-- Iteracion : 1..* 
    Iteracion -- Artefacto : 1..*
    Artefacto <|-- Documento
    Artefacto <|-- Software
    Iteracion o-- Actividad : 1..* 0..*
    Actividad o-- Recurso : 0..*
    Recurso <|-- Humano
    Recurso <|-- Material


    class Proyecto {
        -nombre: String
        -avance: float
    }

    class Ciclo {
    }

    class Ejecutable {
    -bytes
    }

    class Fase {
    -tipo: tipoFase
    }

    class Iteracion {
        -comienzo: Date
    }

    class Artefacto {
    }

    class Documento {
        -nombre:String
        -ubicacion
    }

    class Software {
        -bytes
    }

    class Actividad {
        -duracion: int
        -avance: float
    }

    class Recurso {
    }

    class Humano {
        -nombre: String
    }

    class Material {
        -inventario: String
    }