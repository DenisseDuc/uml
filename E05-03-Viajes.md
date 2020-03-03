classDiagram
	Vuelo
    Avión  
    Billete
    Persona
    
    
    Vuelo  -- Persona : 0..* Viaja 0..* 
    Vuelo -- Avión : 0..* es realizado 1 
    
    class Vuelo{
		-plazas: int
        -fecha: date
	}
	class Persona{
		-nombre : String 
        -apellido : String
        -fecha_nac : Date
        -sexo : char
	}
	class Avión{
		modelo: String
        -capacidad: int
	}

    class Billete {
        -asiento : int
    }