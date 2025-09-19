# Activar MySQL en Windows

## 📌 Descripción

Este procedimiento inicia el servicio de MySQL/MariaDB en Windows para que acepte conexiones locales o remotas.

## 🚀 Comando rápido (PowerShell o CMD)

```powershell
net start MySQL94
```

Nota:El "94" es la que yo tengo.

## 🚀 Verificar que esta activo(PowerShell)

```powershell
Get-Process | Where-Object { $_.ProcessName -match "mysqld" }
```

## 🚀 Verificar puerto

```powershell
netstat -ano | findstr :3306
```

Nota:
-Debe salir algo como "LISTENING".

-Si el puerto 3306 esta ocupado,no iniciara.Puedes cambiar el puerto en el archivo "my.ini".(Buscar un video en yotube).
