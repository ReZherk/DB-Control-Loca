# Activar SQL Server en Windows

## 📌 Descripción

Este procedimiento inicia el servicio de SQL Server para aceptar conexiones locales o remotas.

## 🚀 Comando rápido (PowerShell o CMD)

```powershell
net start MSSQL$SQLEXPRESS
```

## 🚀 Verificar que esta activo (PowerShell)

```powershell
Get-Process | Where-Object { $_.ProcessName -match "sqlservr" }
```

## 🚀 Verificar puerto (PowerShell o CMD)

```powershell
netstat -ano | findstr :1433
```

Nota:

- El puerto se configura en SQL Server Configuration Manager → TCP/IP → IPAll.
- Si el servicio no inicia, puede que el puerto esté ocupado o el protocolo TCP/IP esté deshabilitado.
