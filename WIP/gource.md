# Visualizing Projects with [Gource](https://github.com/acaudwell/Gource) 
## ...or make Your Project Manager smile towards the end of the Year :-)

Actually [Martin Giffy D'Souza](https://twitter.com/gassenmj/status/900351771486420994) motivated me to write this blog post. Thanks Martin! 
The idea behind Gource is genious:
* It reads from the logs in Your software version control
* Every action by a developer it somehow represented there
* After the analysation of those logs a cool graph is visualizing what has been done in Your project during a specified timeframe

Cool, hm?

Here is a basic example how to run gource, once You have downloaded it from Git. You will start gource from the command line and pass some parameters:
The README.txt file gives a clear understanding of what is possible!
```
gource gource_input.log -s 2 -a 0.2
```


You don't have enough of the good stuff? Here is more:
We had a look into the file format that gets written after analysing the SVN/Git logs. The format is pretty neat. look what I also found in the README.txt

>Custom Log Format:



>If you want to use Gource with something other than the supported systems,

>there is a pipe ('|') delimited custom log format:



>    timestamp - A unix timestamp of when the update occured.

>    username  - The name of the user who made the update.

>    type      - initial for the update type - (A)dded, (M)odified or (D)eleted.

 >   file      - Path of the file updated.

 >   colour    - A colour for the file in hex (FFFFFF) format. Optional.

```
sqlplus -s /nolog @gource_db_spool.sql %1
gource gource_input.log -s 2 -a 0.2
```

```
set pages 0
set lines 400
set longc 1000
set long 1000
set heading off
set feedback off
set trimspool on 
set termout off
--set sqlformat delimited '|';
SET COLSEP '|'
spool gource_input.log
@&1
spool off
exit
```


<sup>[Beam me up, Scotty](https://gassenmj.github.io)<sup>
