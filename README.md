 ### Diagrama de Clases: Estadística
 
 ```mermaid
 classDiagram
     EstadisticaBase <|-- EstadisticaCuantitativaBasica
     EstadisticaBase <|-- ClaseCuantitativa
     EstadisticaBase <|-- ClaseCualitativa
     
     Main ..> EstadisticaBase : usa
 
     class EstadisticaBase {
         +dataset
     }
     class EstadisticaCuantitativaBasica {
         +mediana()
         +media()
         +percentil()
     }
     class ClaseCuantitativa {
         +varianza()
         +desviacionEstandar()
     }
     class ClaseCualitativa {
         +moda()
         +frecuencia()
     }
     class Main {
         +ejecutar()
     }
