# Activar PostgreSQL en Windows

## 📌 Descripción

Este procedimiento inicia el servicio de PostgreSQL en Windows para aceptar conexiones locales o remotas.

## 🚀 Comando rápido (PowerShell o CMD)

```powershell
net start postgresql-x64-17
```

Nota:Revisar la version que tienes en mi caso es "17".

## 🚀 Verificar que esta activo (PowerShell)

```powershell
Get-Process | Where-Object { $_.ProcessName -match "postgres" }
```

## 🚀 Verificar puerto (PowerShell o CMD)

```powershell
netstat -ano | findstr :5432
```
