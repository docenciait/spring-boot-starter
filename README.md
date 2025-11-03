# Spring Boot Minimal + MySQL + Docker Compose

## 🚀 Ejecución rápida

```bash
docker compose build
docker compose up -d
```

Accede a la aplicación en: [http://localhost:8080](http://localhost:8080)

Base de datos MySQL en el puerto **3306** con usuario `spring` / password `spring`.

- Usuario `root` con password `root`

```sql
mysql -h 127.0.0.1 -u spring -p
```

- Reconstruir y levantar todo (recomendado cuando hay cambios en la app):

```bash
docker compose down -v
docker compose up -d --build
```

- Logs:

```bash
docker compose logs -f mysql
docker compose logs -f app
```

- Esto es sólo si se quiere recrear la app:

```bash
docker compose build app
docker compose up -d --no-deps --force-recreate app
```

- Verificar con curl:

```bash
curl http://localhost:8080/api/clientes
```
