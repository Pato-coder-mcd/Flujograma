# Flujograma del Algoritmo RSA

A continuación se presenta un flujograma que describe paso a paso el proceso de generación de claves, cifrado y descifrado en el algoritmo RSA.

```mermaid
flowchart TD
    A[Inicio] --> B[Generación de Claves]
    B --> C[Seleccionar dos números primos grandes p y q]
    C --> D[Calcular n = p * q]
    D --> E[Calcular la función totiente]
    E --> F[Elegir exponente de cifrado e]
    F --> G[Calcular exponente de descifrado d]
    G --> H{Claves generadas}
    H --> I[Clave Publica: e y n]
    H --> J[Clave Privada: d y n]
    
    J --> K[Cifrado]
    K --> L[Convertir mensaje M en numero m]
    L --> M[Calcular texto cifrado]
    M --> N[Enviar texto cifrado]

    N --> O[Descifrado]
    O --> P[Recibir texto cifrado]
    P --> Q[Calcular mensaje original]
    Q --> R[Convertir numero m al mensaje original M]
    R --> S[Mensaje original M recuperado]
    S --> T[Fin]



    
