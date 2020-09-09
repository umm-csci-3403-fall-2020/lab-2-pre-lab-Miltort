# Leak report
The reason that there is a memory leak is that the calloc used at line 41 is never freed. It is handed up until it makes it all the way to the isclean function, but then never gets freed. I believe that is where it should be freed. 
