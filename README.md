# ACTD

# Pasos para conectar y verificar el estado de ACTD en el CGR

## 1. SSH al CGR  
Accede al CGR a través de SSH.

## 2. SSH al GOS IPv4 desde el CGR  
Puedes conectarte usando IPv6 si está disponible, pero la dirección `10.8.58.6` siempre debería ser accesible después de que el CGR complete el registro en FND.  

Ejecuta el siguiente comando:  
```bash
ssh -l cg-nms-administrator 10.8.58.6
