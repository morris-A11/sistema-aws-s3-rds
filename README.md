\# Sistema de Almacenamiento AWS S3 + RDS + Lambda



\## Descripción

Sistema automático que registra en una base de datos MySQL cada archivo subido a un bucket S3, usando una función Lambda como intermediario.



\## Servicios AWS utilizados

\- \*\*S3\*\* — Almacenamiento de archivos con versionado

\- \*\*RDS MySQL\*\* — Base de datos para registro de archivos

\- \*\*Lambda\*\* — Función Python que conecta S3 con RDS

\- \*\*IAM\*\* — Roles y permisos seguros

\- \*\*VPC\*\* — Red privada para comunicación entre servicios



\## Arquitectura

S3 (archivo subido) → Lambda (triggered) → RDS MySQL (registro guardado)



\## Tabla de base de datos

| Campo | Tipo |

|-------|------|

| id | INT AUTO\_INCREMENT |

| nombre\_archivo | VARCHAR(255) |

| tamanio\_bytes | BIGINT |

| fecha\_subida | TIMESTAMP |

| subido\_por | VARCHAR(100) |



\## Autor

Adrián Álvarez Jaramillo

