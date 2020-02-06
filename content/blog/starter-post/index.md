---
title: Ukrainian in Vim
date: "2020-02-05"
description: Creating a Ukrainian keyboard layout in vim
---

Today I feel like I finally did something that I've always wanted to do with vim, I updated my vimrc so that I can easily transition to writing Ukrainian on an english keyboard without having to relearn all the letter positions of a normal keyboard setup.

In order to do this I created 3 functions in my vimrc

1. Function 1 is the function that sets all the mappings
2. Function 2 is the one that unsets all the mappings function 1 set
3. Function 3 uses function 1 and 2 and a variable to create a toggle for the mappings


The main take aways are that in order to input the ukrainian characters into the vimrc in the first place you need to find their unicode character on https://en.wikipedia.org/wiki/Ukrainian_alphabet afterwards you can type them in by using "ctrl+v u" + the character code. EG: typing ctrl+v u0424 gives you this Ф

To map all the characters you need in the first function you use your selection of characters using this function:
    
imap f ф	

Do that with all characters and you find that quite a few translate over very nicely, but I knew that I would run out of english characters to overwrite and I decided that I usually don't use numbers when I'm writing so I overwrote them all other than 1,5,0. 1 I left due to the exclamation point and the others are leftovers. You can also use a dead key and have a key combinations for some characters. EG:

imap ii ї

Once thats done you can copy over the entire function to create the unmapping function then you change every instance of imap to iunmap, and remove anything after the replacement character, it should look like this:

iunmap a

If you have any trailing spaces after the 'a' you will probably get an error when you try to unmap as vim will probably think you are unmapping a + spacebar

The final function looks something like this:

```vimscript

let g:ukrainian\_not\_mapped=1
function ToggleUkrainian()
    if g:ukrainian\_not\_mapped
        call SetUkrainain()
        let g:ukrainian\_not\_mapped=0
    else
        call UnSetUkrainain()
        let g:ukrainian\_not\_mapped=1
    endif
endfunction
```
