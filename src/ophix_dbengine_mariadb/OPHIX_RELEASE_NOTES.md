# Ophix Dbengine Mariadb Release Notes

## 2026.10.04.01

- Reworked `README.md`'s opening with a hook-first pitch (Ophix's recommended default for
  operators who don't have a database opinion yet, one install away), as part of the
  16-package taskserver-release-wave README overhaul.

## 2026.09.29.01

- Initial release. Split out of `ophix-server-base`, where `mysqlclient` was
  previously a hard dependency regardless of which database engine a server
  actually used — every non-MariaDB install (Postgres, SQL Server, Oracle,
  CockroachDB) paid the cost of a driver it never needed, including
  `mysqlclient`'s C-extension build requirements on platforms without a
  prebuilt wheel. MariaDB/MySQL are now symmetric with every other engine:
  install the matching `ophix-dbengine-*` plugin for whichever one you use.
  MariaDB stays the *recommended* default in install docs — just no longer
  silently bundled for everyone regardless of choice.
