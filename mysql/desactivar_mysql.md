# Desactivar MySQL en Windows

## 📌 Descripción

Este procedimiento detiene el servicio de MySQL/MariaDB para liberar recursos cuando no se está usando.

## 🛑 Comando rápido (PowerShell o CMD)

```powershell
net stop MySQL80
```

Nota:Mi version es la 80,la tuya puede ser otra,revisar el "NombreDelServicio.md" en la raiz del repositorio.

## 🛑 Verificar si se detuvo (PowerShell)

```powershell
Get-Process | Where-Object { $_.ProcessName -match "mysqld" }
```

Nota:Si no devuelve nada significa que esta detenido.
