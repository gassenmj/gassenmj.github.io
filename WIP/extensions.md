# SQLcl - Gotta love that tool (Reason 1 out of n)

TL;DR: Scroll to the last part of that blog post and I show You how You can create Your own custom SQLFORMAT with SQLcl. 

## Motivation for a custom SQLFORMAT
It all started with an idea that [Sven](https://svenweller.wordpress.com/) created in the [SQL Developer Change Forum](https://apex.oracle.com/pls/apex/f?p=43135:7:9503816231429::NO:RP,7:P7_ID:46941). The idea basically describes a way how You would query a table in SQL Developer that includes a special hint (similar to the /*csv*/-Hint). The result of such a query would be a formatted output so that the data in the table can be shared with a colleague / friend that could help You with writting a SQL Statement.

I tweeted about it and it did not take long until a very intersting discussion about pros and cons started.

If You read through the whole [conversation](https://twitter.com/gassenmj/status/1059849697777672193) on Twitter You will recognize that the cons are all very valid points. I won't discuss them in my post here, but in my eyes it still depends on the mindset of the developer in front of the keyboard whether an ad-hoc query should be executed against the database or not. The baseline is: If You will run such an query against a table with a million records You might want to might want to grap a coffee and re-think why You are just exporting a million records in that format. The use case is for rather small tables where You would like to provide quick and dirty test data - no create table statement, hence no DDL nessecary for the buddy You share Your test data with.

## How the result looks like
Enough digressing! Here is a clear example what I would imagine:

Developer 1 has a problem to write her SQL. He would like to get advice by Developer 2, but Developer 2 has no access to the database of Dev 1. So Dev 1 opens her SQLcl and types:

```
script C:\scripts\withCl.js
set sqlformat withCl
select * from tab;
```

The result looks like the following:
```
WITH tst_data as (
select ... from dual union all 
select ... from dual union all 
...
select ... from dual 
)
select * from tst_data;
```


## How I build my custom SQLFORMAT
 Let's check the code.


Now let's go through that whole thing step by step :-).

## Happy to see Your [tweets](https://twitter.com/gassenmj/)

-> I dedicate this post to [Jeff](https://twitter.com/thatjeffsmith/status/1059850150573731840) 

<sup>[Beam me up, Scotty](https://gassenmj.github.io)<sup>


