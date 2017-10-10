# This is just a ```/* comment */ ```on the ```--comment ```
## ...because it is ODC Appreciation Day

Let's use this wonderful [#ThanksODC](https://twitter.com/hashtag/ThanksODC?src=hash) initiative by [Tim Hall](https://oracle-base.com/blog/2017/09/25/odc-appreciation-day-2017-thanksodc/) to do my first blog post.

I do not want to discuss the pros and cons like 
* long vs. short comments or 
* developers not having time to document their work properly 

For sure there are a lot more aspects to cover, but here is just a quick version of why I think **comments** in all kind of flavours deserve a portion of applause at ODC Appreciation Day.

I love them because developers can prettify code. Also, we hear a lot about best practices. But sometimes in real live they just do not fit to the current situation. 
Whenever I faced that situation in the past, I tried to force myself to at least provide some quick comments why I chose such an approach in my code.

Also some complex SQL queries can get annoying when not having the initial thoughts of a developer. I try to divide complex queries into some smaller parts. I do a kind of docu for each part of the SQL then by adding comments.

There is more: Hopefully it is known that commenting on objects is possible, e.g. columns or tables:

```comment on column my_tab.col_a '...this is useful information for any developer'; 
comment on table my_tab is '...this is useful information for any developer';
```

But hey, did You know? You can even write Your comments on Editions (EBR)...check it out Yourself 
https://docs.oracle.com/database/121/SQLRF/statements_4010.htm#SQLRF01109

Well, and I personally love this SQL Developer Feature:
If You go Tools -> Preferences -> Shortcut Keys -> search for "Toggle Line Comments" You are able to define Your own shortcut to comment/uncomment a lot of lines.

I don't know if that still counts as a comment but we might want to talk about the value of nice commit messages when checking code into version control systems.
For sure there are other useful developer written messages. But nobody RTFM ;-)

There are also the funny aspects: 
* https://stackoverflow.com/questions/184618/what-is-the-best-comment-in-source-code-you-have-ever-encountered
* https://twitter.com/iamdevloper/status/657130347109351424

There are some quotes I like, for example You this one by [Martin Fowler](https://en.wikiquote.org/wiki/Martin_Fowler) 
> "Any fool can write code that a computer can understand. Good programmers write code that humans can understand."

mm...and hey developers! Do not forget to adopt the comment next time when changing the underlying piece of code ;-)...that might confuse me! 

```--no more comments :-)```
