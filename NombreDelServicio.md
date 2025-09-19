## 🔍 Cómo encontrar el nombre exacto del servicio mysqld|postgres|sqlservr en Windows

1. **Abrir el administrador de servicios**

   - Presiona `Win + R`, escribe `services.msc` y pulsa **Enter**.

2. **Buscar mysqld|postgres|sqlservr en la lista**

   - Localiza un servicio con nombre similar a:
     - `MySQL80` (MySQL 8.0)
     - `MySQL57` (MySQL 5.7)
     - `mysql` (instalaciones personalizadas o XAMPP/WAMP)

3. **Usar el nombre en el comando**
   ```bash
   net stop NOMBRE_DEL_SERVICIO
   ```

En este caso los que aparecen se uso como ejemplo a mysql.
