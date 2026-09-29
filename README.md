# ophix-dbengine-mariadb

MariaDB/MySQL database engine plugin for [ophix-server-base](https://github.com/ophixproject/ophix-server-base).

Bundles `mysqlclient`. Set `DB_ENGINE=mariadb` (or `mysql`) in `.env` to use it — this is also
the engine every Ophix server defaults to if `DB_ENGINE` is unset, but the driver itself is only
present if this plugin is installed.

MariaDB is Ophix's recommended default database — most install docs suggest installing this
plugin alongside a domain package to get started with no further configuration. It's a real
plugin like every other supported engine (Postgres, SQL Server, Oracle, CockroachDB each have
their own `ophix-dbengine-*` package too); nothing is silently bundled regardless of which engine
a server actually uses.

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
