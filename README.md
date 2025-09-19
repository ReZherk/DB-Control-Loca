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
