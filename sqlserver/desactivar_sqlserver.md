# Desactivar SQL Server en Windows

## 📌 Descripción

Este procedimiento detiene el servicio de SQL Server para liberar recursos cuando no se está usando.

## 🛑 Comando rápido (PowerShell o CMD)

```powershell
net stop MSSQL$SQLEXPRESS
```

Nota:Mi version es la express,pero existen otra.

## 🛑 Verificar si se detuvo (PowerShell)

```powershell
Get-Process | Where-Object { $_.ProcessName -match "sqlservr" }
```

Nota:Si no devuelve nada significa que esta detenido.
