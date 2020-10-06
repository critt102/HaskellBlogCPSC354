# Haskell for Beginners
## Blog 1 - 10/05/20

When I first installed Haskell on my computer, it didn't go as smooth as expected. Unlike many of the programming languages I had used in the past, I was told to run the installation command from the terminal of my computer.  
I have a Macbook, which means I was trying to download Haskell onto macOS, and therefore used terminal. According to haskellstack.org, I could install Haskell by running the following in my terminal.

>curl -sSL https://get.haskellstack.org/ | sh

However, when I did this, I got a lot of errors. Which led to a lot of google searching. What I discovered is that my computer did not have the macOS developer tools, which means it lacked the command line developer tools it needed to compile and manage Haskell. By default, most Apple products do no include these coding tools, and they need to be manually installed.

While there are many ways to install these tools, I chose to use the install function that is already present on my computer, but just needed to be invoked through terminal. By running the "make" command, or another standard development command such as "gcc" or "git," the computer should prompt you to install these command line developer tools. (These can simply be run by typing the word "make" into the first line of your terminal). If you do not get the prompt, double check for the *"Install Command Line Developer Tools"* application in:

>Macintosh HD > System > Library > CoreServices

Unfortunately, you can't launch the install directly from that folder, but calling "make" in terminal should do the trick. Once these command lines developer tools were installed, I was able to install Haskell. From there, I was able to start Haskell by using:

>stack exec ghci

Which then caused the following lines to appear:

>GHCi, version 8.8.4: https://www.haskell.org/ghc/  :? for help
>Prelude>

From here, I was able to run the basic functions of Haskell, such as basic mathematical functions (addition "+", subtraction "-", division "/" and multiplication "\*") and variable assignment (a=2, b=3, a+b will return 5).
Below is some example code and how it looks/functions in Haskell.

>Prelude> 2+2  
>4  
>Prelude> 2+2  
>4  
>Prelude> 3*3  
>9  
>Prelude> a=2  
>Prelude> b=4  
>Prelude> a  
>2  
>Prelude> b  
>4  
>Prelude> a+b  
>6  
>Prelude> a-3  
>-1
