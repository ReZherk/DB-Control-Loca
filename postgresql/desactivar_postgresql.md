# Desactivar PostgreSQL en Windows

## 📌 Descripción

Este procedimiento detiene el servicio de PostgreSQL para liberar recursos cuando no se está usando.

## 🛑 Comando rápido (PowerShell o CMD)

```powershell
net stop postgresql-x64-17
```

Nota:Cambiar por la version que tienes en mi caso es la "17".

## 🛑 Verificar que se detuvo (PowerShell)

```powershell
Get-Process | Where-Object { $_.ProcessName -match "postgres" }
```

Nota:No te debe devolver nada.
