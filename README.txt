Быстрый веб-сканер для поиска sql-инъекции Sqlscan 

Перед вами один из самых доступных способов взлома сайта. Суть таких инъекций – внедрение в данные (передаваемые через GET, POST запросы или значения Cookie) произвольного SQL кода. Если сайт уязвим и выполняет такие инъекции, то по сути есть возможность творить с БД (чаще всего это MySQL) что угодно.

Качаем curl и php:
apt install php curl

Теперь инструмент:
curl https://raw.githubusercontent.com/Cvar1984/sqlscan/dev/build/main.phar --output $PREFIX/bin/sqlscan

Делаем файл исполняемым:
chmod +x $PREFIX/bin/sqlscan

А вот несколько примеров запуска:
sqlscan http://example.gov --scan
sqlscan файл_с_ссылками.txt --scan

Всем сочных инъекций