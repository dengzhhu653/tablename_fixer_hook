TableName fixer hook

Since HIVE-16907 the '.' was forbiddne from table names because that was not really an intentional extension of the standard.

To help migrating from `db.table` formatted queries this hook can be used to fix table-names on-the-fly.

installation:

* download a built jar from https://github.com/kgyrtkirk/tablename_fixer_hook/releases
* put the jar onto the HiveServer2's classpath by adding it to hive.aux.jars.path
* set the property 'hive.semantic.analyzer.hook' to include 'hu.rxd.hive.tablename.fixer.hook.FixupIncorrectUsageOfDotsInTableNames'
* restart HiveServer2
