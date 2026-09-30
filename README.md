# ophix-dbengine-mariadb

**Don't have a database opinion yet? [Ophix](https://ophix.io)'s recommended default, one install away.**

Not every operator arrives with a database already decided — MariaDB is what Ophix recommends if you're starting from scratch. `ophix-dbengine-mariadb` is what makes `DB_ENGINE=mariadb` actually work: install this plugin alongside any domain package and you're running on a solid, widely-supported default.

Bundles `mysqlclient`. Set `DB_ENGINE=mariadb` (or `mysql`) in `.env` to use it — this is also
the engine every Ophix server defaults to if `DB_ENGINE` is unset, but the driver itself is only
present if this plugin is installed. It's a real plugin like every other supported engine
(Postgres, SQL Server, Oracle, CockroachDB each have their own `ophix-dbengine-*` package too);
nothing is silently bundled regardless of which engine a server actually uses.

---

## Installation

```bash
pip install ophix-dbengine-mariadb
```

Set in `.env` (or just leave `DB_ENGINE` unset — `mariadb` is the default):

```bash
DB_ENGINE=mariadb
DB_HOST=your-mariadb-host
DB_PORT=3306
DB_NAME=ophix_db
DB_USER=ophixuser
DB_PASSWORD=yourpassword
```

For TLS, set `DB_SSL_CA` to the path of your CA certificate.
