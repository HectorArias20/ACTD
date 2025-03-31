# ACTD

# Pasos para conectar y verificar el estado de ACTD en el CGR

## 1. SSH al CGR  
Accede al CGR a través de SSH.

## 2. SSH al GOS IPv4 desde el CGR  
Puedes conectarte usando IPv6 si está disponible, pero la dirección `10.8.58.6` siempre debería ser accesible después de que el CGR complete el registro en FND.  

Ejecuta el siguiente comando:  
```bash
ssh -l cg-nms-administrator 10.8.58.6

```
Nota: El GOS IPv4 es el mismo en todos los CGRs. Usa el usuario y contraseña del CGR.

## 3. Navegar a la carpeta de ioxclient
El cliente puede estar en diferentes ubicaciones, como /root, /software/downloads/, o /home/cg-nms-administrator.

Ejemplo de navegación a una versión específica:
```bash
cd /software/downloads/ioxclient_1.9.2.0_linux_386
```

## 4. Verificar el estado de actd
Ejecuta el siguiente comando:
```bash
./ioxclient app status actd
```

## 5. Activar actd si está en estado "DEPLOYED"
Si el estado es DEPLOYED, actívalo con:
```bash
./ioxclient app activate actd
```
## 6. Iniciar actd si está en estado "ACTIVATED"
Si el estado es ACTIVATED, inícialo con:
```bash
./ioxclient app start actd
```

## Nota: Puede verificar el estado nuevamente 
