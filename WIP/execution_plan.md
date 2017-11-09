--otherwise it might result in a strange error message
set  serveroutput off
--in order to receive all statistics see more in v$statistics_level
alter session set statistics_level = 'ALL';

--maybe without the actual query output
--set autotrace traceonly

--execute the statement with the hint that it should collect information

select /*+ gather_plan_statistics */
  * 
from dual;

--now use the following table function for viewing the execution plan
select  * 
from table (dbms_xplan.display_cursor(null,null,'ALLSTATS LAST +peeked_binds'));
