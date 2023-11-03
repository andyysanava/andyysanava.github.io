@startuml
scale 3

abstract class MediosTransporte{
    -velocidad: float
    -tipoDeCombustible: String
    -autonomia: int
    +especificarVelocidad(float velocidad):void
    +especificarCombustible(String tipoDeCombustible):void
    +especificarRecorrido():void
}

class Terrestres{
    -numeroDeRuedas: int
    -numeroDePuertas: int
    -motor: String
    +especificarTipoDeMotor(String motor):void
    +especificarNumeroDeRuedas(int ruedas):void
    +especificarNumeroDePuertas(int puertas):void
}

class Acuaticos{
    -pesoMax: int
    -tipoDePropulsion: String
    -dimensiones: int
    +especificarPesoMax(int pesoMax):void
    +especificarTipoDePropulsion(String tipoDePropulsion):void
    +calcularDimensiones(int dimensiones):void
}

class Aereos{
    -alturaMax: int
    -tipoDePropulsion: String
    -envergadura: int
    +calcularAlturaMax(int alturaMax):void
    +especificarTipoDePropulsion(String tipoDePropulsion):void
    +especificarEnvergadura(int envergadura):void
}

class Subterráneos{
    -sistemaDeFrenado: String
    -tamaño: float
    -cargaMax: int
    +especificarSistemaDeFrenado(String sistemaDeFrenado):void
    +calcularTamaño(float tamaño):void
    +calcularCargaMax(int cargaMax):void
}

class Supraterráneos{
    -tipoDeNeumaticos: String
    -cargaMax: int
    -tamaño: float
    +especificarTipoDeNeumaticos(String tipoDeNeumaticos):void
    +calcularCargaMax(int cargaMax):void
    +clacularDimensiones(float tamaño):void
}

class Trajinera{
    -color: String
    -capacidadMax: int
    -precio: int
    +avanzar():void
    +retroceder():void
    +frenar():void
}

class Barco{
    -color: String
    -capacidadMax: int
    -marca: String
    +avanzar():void
    +frenar():void
    +tocarLaBocina():void
}

class Helicoptero{
    -color: String
    -marca: String
    -puertas: int
    +despegar():void
    +aterrizar():void
    +cambiarTrayectoria():void
}

class Avion{
    -color: String
    -marca: String
    -precio: int
    +avanzar():void
    +retroceder():void
    +despegar():void
}

class Metro{
    -color: String
    -capacidadMax: int
    -numeroDeAsientos: int
    +avanzar():void
    +especificarAsientosDisponibles():void
    +frenar():void
}

class Suburbano{
    -color: String
    -marca: String
    numeroDeParadas: int
    +avanzar():void
    +nombrarLaSiguienteEstacion():void
    +cambiarDeVia():void
}

class Taxi{
    -tarifas: int
    -modelo: String
    -kilometraje: int
    +calcularPrecioTotal(int tarifas):void
    +girar(String lado): void
    +usarFrenoDeMano():void
}

class Combi{
    -placas: int
    -informacionDelConductor: String
    -numeroDeAsientos: int
    +cerrarLaPuerta():void
    +abrirLapuerta():void
    +devolverCambio(int billete):void
}
MediosTransporte <|-- Terrestre
MediosTransporte <|-- Acuaticos
MediosTransporte <|-- Aereos
Terrestres <|-- Subterraneos
Terrestres <|-- Supraterraneos
Acuaticos <|-- Barco
Acuaticos <|-- Trajinera
Aereos <|-- Avion
Aereos <|-- Helicoptero
Subterraneos <|-- Metro
Subterraneos <|-- Suburbano
Supraterraneos <|-- Taxi
Supraterraneos <|-- Combi
@enduml

<!-- View/Command Palette/plantuml -->
