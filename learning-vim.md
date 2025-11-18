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
* i lied there's a couple more things. it bothers me that i dont know how to go to the beginning and end of a file. there seems to be a few commands to do it -- as in, many ways. anyways. gg goes to the beginning. G goes to the end but only last line, at its beginning, not at the real end. apparently :$ does it. it looks like an emoticon lol. or ]]. ill try both. so wait. it says ]] but i had to press shift ] shift ] aka }}. who knows. but it does what i want so it's nice
* there's also two more things. 1) i got recommended vim easy motions and rainbow pharentesis. ill add them to the todo list. and the other one is that i dont know how to move whatever is after my cursor in a new line, kinda like pressing enter. ill add that too
* ill also need to start adding these keys to anki to memorise them properly…

# Day 3!

* i always forget how to go to the beginning and the end of the line. it's 0 for beginning, $ for the end. not the most intuitive.
* i was searching how to move the current line im in down or up. in the meantime i found `dd` and then p or P to paste it. didnt' know dd was cut and not just delete. nice.
* so apprently it's :m +1, or -2 to put it up. dunno why it's -2 it doesnt make sense. and also, i think it's time to enable the line numbers i've seen people jump to lines directly and i want to do that. 
* i've enabled them, but i'm trying just the relative ones. i guess it makes it easier to jump to them. but it's a bit odd that :8 goes to the absolute 8 line and not what's showing as 8. but it also makes sense given i can just do eg :-8. nice emoticon lol
* ill be honest, i've spent a good chunk of this session setting up tmux today. HOWEVER. i've done it all via vim. so i think it's still not too bad! and i've learned a couple more keys.

# day 4

* going through vimhero. it's like an interactive tutorial, i'm at the operators part. dw deletes a word. d$ to the end of line. ie d is the operator and then you add the motion.
* i gave it a try and i think the really nice thing is that i don't actually seem to have like a "timer". it will wait. nice, but i can see how it would go wrong too.
* dd deletes the entire line -- this i knew. D deletes from where i am to end of line. i like it. quicker than d$ like the website says
* some more crazy stuff: dj deletes current and below line dk and above. then you have 3dd which removes 3. lemme try if it works for any arbitrary number of lines
* it does! crazy. wonder if there's an up to. i guess -?. no. because if i do - it jumps to that line
* last lesson in vimhero (nice website btw!): yy or Y copies the current line. and p pastes below, P above. i remember those.
* i had a very nice moment just now. had a bunch of bs lines i entered to test stuff in this doc. saw them and wanted to delete them. i see the relative line number too and see it counts to five. i do `5dd` without thinking about it too much, and it deletes them! … except i missed one because it starts from 0, so they were actually 6 lines. but still, it felt nice, like im actually using the power of vim. no one taught me that "combination" in a way, it was an emergent behaviour
* im going through vimtutor now. rapid fire of keys i either forgot or learned: x to delete under the cursor
* i don't actually know how to abort an operator. eg i just pressed f for some reason when i actually wanted to press d. lemme add a todo

# day 5!

* [diego from the future] i have managed to delete a couple of lines and i dont know how i did it. deleting, as in, i just had to read add `# day 5` etc as i nuked them. ha!. i know there's like a fully history but it's fine for now.
* oh so the number prefix 3dd 3 works with all operators or motions i think. 3w goes 3 words forward
* i like r to replace the character, but x deletes it wouthout replacing and without coming out of normal mode
* for undo: u does undo. U is u but for the whole line. control r is re-do (undo the undo)
* d$ deletes the line after the cursor, d0 before! to remind myself: dd is the whole line, d$ line after cursor, d0 before. d2w two rwords after, d7b 7 words back. very powerful
* i think i will want to add a visual line break of like 120 as i am trying to run vim (via tmux) fullscreen and if vim is the only thing open it's crazy long
* gg goes to beginning of file. G to end. how did i not know this before??? i was doing }} and {{…
* something else related to that: gg to go to beginning of the file, V to enter visual mode, G to go to end, y to yank (copy). i have not yet explored visual mode but it looks super interesting
* also, a bit less progress today as i spent a couple of hours reading up on neovim and configuring it for swift. i think i will only really learn vim if i end up using it like that, so i want to try my best to use it for ios -- and at least python too

# day 6

* I really need to get into the visual mode, as i'm lacking all the stuff to select lines etc. but that's for later
* in the meantime i'm installing catpuccin to have a decent them. it's good enough
* i dont love the purple background but ill change it later
* i also need to 1) make it so that telescope is triggered by a single key 2) install the tree navigator stuff. let's do both
* i also need autocompletion / indentation for lua. dont think i have it

# day ???

* it's time to learn the visual/visual block stuff
* okay so fundamentally it's: option v -- which enters the mode, then you do some actions (eg I for insert at beg of line), then escape. i am not sure if escape is always needed
* not a lot more it seems like
* i've also finally started anki for vim! there's a nice shared deck in ankiweb, but i'm also adding my own -- mostly for plugins like the commentator one.
* super super super useful: control o (back) i (forward) gets the cursor back where it was. eg i wanted to go to the previous {, and pressed shift [. which goes at the top of paragragh-ish. control o puts the cursor back to where i was!
* `aw` marks a word. i saw this in anki, but i don't fully get it as `a` just inserts immediately. okay, i think it's in visual mode only
* i still dont really know the difference between visual and visual block modes
* also i have suggestions in enter via `blink`, but it's annoying when i just want to enter for new line and not accept the suggestions. i think i'll change it to tab

TODOs:
- [x] I need to remember to sync my vim config to all macs / add it to the dot files
- [ ] install vim easymotion
- [ ] install rainbow pharentesis
- [ ] put whatever is after my cursor in a new line, ie enter to newline
- [x] add keys to anki deck
- [ ] how do i "abort" an operator, eg d?
- [ ] how do i abort a command in normal mode
- [ ] add a 120 max line visually
