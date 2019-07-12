# SQL*Plus Hash Command
## This is just a qicky about how I use the Hash Command in SQL*Plus for my Demos

Here is some example code

```
Let's use 
--Demo WITHOUT # 

pause

create or replace procedure very_long
as
 v varchar2(100);
begin

select 'This is what I want to highlight in my testcase' 
into v
from dual;

--just 
--some 
--random 
--code 
--that
--is
--necessary
--but
--for
--demoing
--not
--worth
--to
--show
--it
--to
--the
--audience


end;
/

pause
cl scr

--Same demo WITH #PAUSE :-)

pause
cl scr

create or replace procedure very_long
as
 --stop here! I want to show something
#pause
 v varchar2(100);
begin

select 'This is what I want to highlight in my testcase' 
into v
from dual;
#pause

--just 
--some 
--random 
--code 
--that
--is
--necessary
--but
--for
--demoing
--not
--worth
--to
--show
--it
--to
--the
--audience
#cl scr
end;
/
```
Here is how I execute it in SQL*Plus. Unfortunately, when I recently tried to switch to SQLcl the script failed.

![alt text](https://raw.githubusercontent.com/gassenmj/gassenmj.github.io/master/img/sql.gif)
