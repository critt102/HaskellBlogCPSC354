# Creating and Loading Files in Haskell
## Blog 2 - 10/12/20

### Writing files for Haskell
When I first started using Haskell, one of my first assignments was to create and load a file into Haskell using Terminal (I am a Mac user, which means I use Terminal, but the equivalent for Windows users is Command Prompt). I was given a program and was told to save it in a file called "recursion_fib.hs" and then to run the program in Haskell. It seemed simple enough, but then I realized I didn't really know what I was dealing with. What was hs? How to I make an hs file? And once it is made, how do I run it in Haskell? So I began to google search.

With a simple google search of "what is .hs file type," the first result told me that .hs is a Haskell Script file, which acts as source code for a program written in Haskell. From here, I had to figure out how to make one. In the past, I have written in various programs that are used as text editors for code, such as Atom and Visual Studio Code. But the professor did not mention the need of either of these, so I felt like there was another way to do it.

My first instinct was to see if I could write and save these files in Terminal, as this is what we were taught to use when running Haskell. After messing around in Terminal, both in and outside of the Haskell program, I still couldn't figure out how to create a .hs file, and decided that Terminal probably wasn't the way to go.

My next instinct was to use TextEdit (this is Apple's standard text editor, as the name suggests), as I had used the program in the past to write README files. When you first open TextEdit, the default formatting is a "Rich Text" file, and when I tried to save a file as file.hs, it would convert it to file.hs.rtf. Since that didn't work, I used TextEdit's settings to change the default file type to a "Plain text" file:

>Format > Make Plain Text || Cmd+Shift+T

From here I tried to save my file as file.hs, but I ran into the same issue, where the file became file.hs.txt. So back to the internet I went. The problem was, that whenever I google searched "How to make a .hs file" or "How to save file as .hs" all that came up was articles about how to open .hs files. So after some further digging, I found a website that listed the supported file types of TextEdit. While .hs was on the list, it didn't say how I could get the program to save in that format. So after a few hours of research, I realized there was a simple solution that was hidden in plain sight. When you go to save a file in TextEdit, there is a drop down tab that lists text encoding types, and right below that drop down is a check box that reads:

>If no extension is provided, use .txt

By default, that box is checked, which means that when I save my file as file.hs, it automatically provides the .txt file extension, making my file file.hs.txt. When you uncheck the box, it not longer forces the .txt file extension onto your saved file, and the file will save as the .hs file type. It was frustratingly simple, so much so that the internet decided that no one would ever be searching for it, which is why I struggled so much to figure it out. But alas, I prevailed.

From here, I decided I would no longer use TextEdit. This makes all my work and research seem a bit redundant, but what I realized is that programs like Atom and Visual Studio codes were just other types of text editors, like TextEdit, but I was more familiar with their formatting and they work well with writing code. So since then, I have been using Atom, and can write .hs files, and .md files like this one and save them with ease.

### Loading Files into Haskell
When it comes to loading files into Haskell, there is a few steps that need to be taken before doing so. First, open Terminal (or Command Prompt if you are a Windows user). Then figure out where you file you want to load is saved. I personally keep all my .hs files in a folder on my desktop. In terminal, use the "cd" function to get your terminal into the folder where your file is located. If you do not direct your terminal to the right location before attempting to load a file, it will return an error.

><no location info>: error: can't find file: len.hs  
>Failed, no modules loaded.

So instead, cd into the folder where your files are located, and use "ls" to double check that you are in the right folder and can see the file you want to load. For example:

>% cd desktop/haskell_files  
>% ls  
>file.hs      test.hs       README.md

Also, if you are unsure what location you are currently in, you can use "pwd" and it will tell you where you are.

>% pwd  
>/Users/marykatecrittenden/desktop/haskell_files

Once you are in the correct folder, use "stack exec ghci" to start up Haskell. Then you can load files using ":load". It is important to include the ":" before the load, otherwise the function will not work (I mention this because I failed to do so and it took me a while to realize why my files weren't loading). If you run and load a file successfully, it will look like this:

>Prelude> :load file.hs  
>[1 of 1] Compiling Main             ( file.hs, interpreted )  
>Ok, one module loaded.  
>\*Main>

From here, you should be able to call information from the file, such as functions or variables. When these files are loaded, Haskell compiles them, just like when you compile any other program. So if the file fails to load, and it is not because you are in the wrong location, it is likely a compiling error. There are lots of different errors, and most of them have to be dealt with by fixing the code in the file itself.
