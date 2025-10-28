 ### Diagrama de Clases (con Relaciones)
 
 ```mermaid
 classDiagram
     direction BT
     
     class Main {
         +ejecutar_analisis()
     }
 
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
         +varianza()
         +percentil()
         +resumen()
     }
 
     class EstadisticaCualitativa {
         +moda()
         +tabla_frecuencias()
         +resumen()
     }
 
     %% "Amplia" (Hereda de)
     EstadisticaBase <|-- EstadisticaCuantitativa
     EstadisticaBase <|-- EstadisticaCualitativa
     
     %% "Utiliza" (Depende de)
     Main ..> EstadisticaBase : utiliza
     Main ..> EstadisticaCuantitativa : utiliza
     Main ..> EstadisticaCualitativa : utiliza
