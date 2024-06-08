# Flujograma del Algoritmo RSA

A continuación se presenta un flujograma que describe paso a paso el proceso de generación de claves, cifrado y descifrado en el algoritmo RSA.

```mermaid
flowchart TD
    A[Inicio] --> B[Generación de Claves]
    B --> C[Seleccionar dos números primos grandes p y q]
    C --> D[Calcular n = p * q]
    D --> E[Calcular la función totiente φ(n) = (p - 1) * (q - 1)]
    E --> F[Elegir exponente de cifrado e]
    F --> G[Calcular exponente de descifrado d]
    G --> H{Claves generadas}
    H --> I[Clave Pública: (e, n)]
    H --> J[Clave Privada: (d, n)]
    
    J --> K[Cifrado]
    K --> L[Convertir mensaje M en número m]
    L --> M[Calcular texto cifrado c = m^e mod n]
    M --> N[Enviar texto cifrado c]

    N --> O[Descifrado]
    O --> P[Recibir texto cifrado c]
    P --> Q[Calcular mensaje m = c^d mod n]
    Q --> R[Convertir número m de vuelta al mensaje M]
    R --> S[Mensaje original M recuperado]
    S --> T[Fin]

    
