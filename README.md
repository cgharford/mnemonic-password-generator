Mnmonic Password Generator

I wrote my program in python and thus did not include a makefile 
compile my program. Initially, I wrote my program with a few 
tranformations and ran it with the following command: 

    $ ./pemdas ~/passwords/texts/artofwar.txt > results.out 

I then ran my results through my checker to see how many of the 
professor's hashes I had generated using this command: 

    $ nice ./checker results.out ~/passwords/mnemonic_hashes

The checker reported that my solution generated only ~8% of the 
professor's passwords. 

I spent a few hours trying to modify my tranformations to match 
more than 8%, but did not succeed. 

I then realized that I needed to be generating mnemonic passwords 
for both The Art of War and The Raven and checking the combination
of this output. Thus, I ran the following commands: 

    $ ./pemdas ~/passwords/texts/artofwar.txt > results.out 
    $ ./pemdas ~/passwords/texts/theraven.txt >> results.out
    
Concatenating the mnemonic passwords for both files. 

I tested the results by running my checker program again: 

    $ nice ./checker results.out ~/passwords/mnemonic_hashes

This time, the checker reported a 31% match. 

I added more transformations, ran the tester program again, and 
the checker reported a 58% match. A lot closer! 

I then started going through The Raven and The Art of War line 
by line, looking for words that could possibly be represented by 
different, more creative symbols. I also looked at some examples 
of leet speak online at https://simple.wikipedia.org/wiki/Leet to 
get some more ideas. This took awhile because if I added too many 
incorrect transformations, my checker would take forever to run so
I had to add different transformations slowly and check every time.  

After adding more tranformations, I ran my checker again and it 
reported a 78% match. Success! 
  
