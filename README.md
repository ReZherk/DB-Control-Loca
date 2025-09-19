# DB Control Local

Guía práctica para **activar, desactivar y verificar** bases de datos locales en Windows (MySQL, PostgreSQL y SQL Server).

## 🎯 Objetivo

Evitar tener todas las bases de datos corriendo al mismo tiempo y consumiendo recursos, activando solo las necesarias.

## 📌 Alcance

- Entornos locales de desarrollo.
- Windows 10/11.
- Servicios instalados como Windows Services.

## 🛠 Requisitos previos

- Permisos de administrador.
- PowerShell o CMD.
- Conocer el nombre exacto del servicio de cada base de datos.

## 📂 Estructura

- **mysql/** → Guías para MySQL/MariaDB.
- **postgresql/** → Guías para PostgreSQL.
- **sqlserver/** → Guías para SQL Server.
- **scripts/** → Scripts PowerShell para automatizar.

## 🚀 Comandos básicos

### Activar un servicio

```powershell
net start <NombreDelServicio>
```

### Desactivar un servicio

```powershell
net stop <NombreDelServicio>
```

### Verificar si está corriendo

```powershell
Get-Process | Where-Object { $_.ProcessName -match "mysqld|postgres|sqlservr" }
```

### Verificar puertos activos

Aqui se encuentran los puertos mas comunes en los cuales las base de datos estan escuchando.

```powershell
netstat -ano | findstr :3306   # MySQL
netstat -ano | findstr :5432   # PostgreSQL
netstat -ano | findstr :1433   # SQL Server
```
