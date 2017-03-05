Reference version used for this fork:
DeSmuME 5345 from February 2016 
https://sourceforge.net/p/desmume/code/5345/tree/trunk/ 
aka
https://github.com/TASVideos/desmume/commit/65c0eec88406a582c9977fdb88ecdb5787aa29b5

Compiler: vs2015


Changes:
------------

1) Brought back functionality as it was in svn4039, had to disregard some commits. To do that especially the following commits were partially ignored:
** 4040 - 4044
** 4102 - 4105
** 4138
** 4665 (that was a tricky one, see comments in NDSSystem.cpp and main.cpp)
** 5346

*2)Added sensible WFC profile defaults and added code to save in game DNS settings into desmume.ini as new default.



What works:
----------------

You can trade Pokemon over the GTS (also from two local games of the same generation if you start your DeSmuME twice, just make sure only one is connected to the server at the same time)
Not sure what else is working.


Open Issues:
----------------
* Saving WFC connection data between DeSmuME restarts. (In the Pokemon universe we are asking the AltWFC server for new Friendship codes for the same MAC all over, as it is currently. Not good!)
* Documentation what is really working or not (Are Trade evolutions supposed to work?).
* More documentation on the communication dependencies between Server and Nintendo DS
(In the beginning the communication is base64 encoded;
 At the first real connection the Nintendo DS is sending the userid (the Nintendo WFC Connection ID) to the server, not the other way around as maybe expected.)



