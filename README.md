 ```mermaid
 classDiagram
     direction BT
     
     class EstadisticaBase {
         <<abstract>>
         +datos
         +cantidad_datos()
         +tipo_datos()
         +resumen()*
     }
     
     class EstadisticaCuantitativa {
         +media()
         +mediana()
         +moda()
         +varianza()
         +desviacion_estandar()
         +percentil()
         +cuartiles()
         +minimo()
         +maximo()
         +promedio()
         +resumen()
     }
 
     class EstadisticaCualitativa {
         +moda()
         +tabla_frecuencias()
         +resumen()
     }
 
     EstadisticaBase <|-- EstadisticaCuantitativa
     EstadisticaBase <|-- EstadisticaCualitativa
