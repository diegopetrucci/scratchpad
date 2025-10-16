# so what i've learned so far

* pressing `i` goes into the typing mode
* pressing esc goes back
* in normal mode: h left one letter, j goes down i think, k goes up, l goes right
* in normal mode: w next word, e end of next word, b back one word
* bonus from the future: shift W E and B do the same but eg `func()` it applies to all, while lowercase would stop at c i believe
* esc u undoes in normal mode
* pasting is a bit insane: you need to do "+p. but it's from normal mode i think. let's try
* only `"*p` seems to be working
* i somehow seem to have a `e` at the cursor point that i dont know how to get rid of
* `au BufNewFile,BufFilePre,BufRead *.md set filetype=markdown` in the vim config makes it so that it can highlight .md files
* i cant do option delete to delete words
* shift i goes interactive but at the beginning of the line. shift a to the end
* o "opens" a new empty line below your cursor, shift O above
* oh and it goes straight into interactive mode. nice
* some more crazy ones: x deletes the character under the cursor but stays in edit. s same but goes interactive. r replaces with whatever character you write next. let's try 

okay i would say this marks the end of the first session. good stuff! i need to continue tomorrow. it's nice. lemme add day 1 or something at the top

## session 2!

* i think im going to start by continuing the tutorial [here](https://www.vim-hero.com/lessons/moving-by-upper-word), i never actually finished it
* i cant figure out what to press to undo an undo, ie redo. i am reading control r but it does not work? ah okay i was pressing control u not r lol
* line controls: 0 beginning of line, $ end, _ to first word of line
* oh these ones are cool: f character to find the first one of that character. eg f a would go to `a`re cool. F (uppercase) goes back. ; goes next find. the tutorial says `These motions are frequently used to jump to symbols such as ( and {.`
* something that is bothering me is that pressing i from normal takes out the last character/where i am…
* okay so it's like this: i for insert before cursor. a for after. I for beg line. A for end. cool!
* similar to f char you have t char which moves (un)til just before that character. T char for backwards
* smaller session today but i think it's fine. im getting to the point where i can use vim now. not that well but i have basic motions + copy paste. not a lot but enough!
* actually i dont know how to copy yet haha. only paste. but the next tutorial section is `operators` which i believe should help




TODOs:
- [ ] I need to remember to sync my vim config to all macs / add it to the dot files
