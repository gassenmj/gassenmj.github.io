TL;DR: Scroll to the second part of that blog post and I show You how You can create Your own custom SQLFORMATs with SQLcl. 

It all started with an idea that [Sven](https://svenweller.wordpress.com/) created in the [SQL Developer Change Forum](https://apex.oracle.com/pls/apex/f?p=43135:7:9503816231429::NO:RP,7:P7_ID:46941). The idea basically describes a way how You would query a table in SQL Developer that includes a special hint (similar to the /*csv*/-Hint). The result of such a query would be a formatted output so that the data in the table can be shared with a colleague / friend that could help You with writting a SQL Statement.

I tweeted about it and it did not take long until a very intersting discussion about pros and cons started.

If You read through the whole [conversation](https://twitter.com/gassenmj/status/1059849697777672193) on Twitter You will recognize that the cons are all very valid points. I won't discuss them in my post here, but in my eyes it still depends on the mindset of the developer in front of the keyboard whether an ad-hoc query should be executed against the database or not. The baseline is: If You will run such an query against a table with a million records You might want to might want to grap a coffee and re-think why You are just exporting a million records in that format. 

The use case is for rather small I quickly repeat the use case and then show how I solved it.


Now let's go through that whole thing step by step :-).


--- I dedicate this post to [Jeff](https://twitter.com/thatjeffsmith/status/1059850150573731840) 
