TableName fixer

Since HIVE-16907 the '.' was forbiddne from table names because that was not really an intentional extension of the standard.

To help migrating from `db.table` formatted queries this hook can be used to fix table-names on-the-fly.

installation:

* put the jar to HS2's classpath by adding it to the hive.aux.jars.path
* set the property 'hive.semantic.analyzer.hook' to include 'experimental.FixupIncorrectUsageOfDotsInTableNames'
