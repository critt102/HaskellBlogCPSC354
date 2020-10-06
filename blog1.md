# Haskell for Beginners
## Blog 1
### 10/05/20

When I first installed Haskell on my computer, it didn't go as smooth as expected. Unlike many of the programming languages I had used in the past, I was told to run the installation command from the terminal of my computer.  
I have a Macbook, which means I was trying to download Haskell onto macOS, and therefore used terminal. According to haskellstack.org, I could install Haskell by running the following in my terminal.

>curl -sSL https://get.haskellstack.org/ | sh

However, when I did this, I got a lot of errors. Which led to a lot of google searching. What I discovered is that my computer did not have the macOS developer tools, which means it lacked the command line developer tools it needed to compile and manage Haskell. By default, most Apple products do no include these coding tools, and they need to be manually installed.

While there are many ways to install these tools, I chose to use the install function that is already present on my computer, but just needed to be invoked through terminal. By running the "make" command, or another standard development command such as "gcc" or "git," the computer should prompt you to install these command line developer tools. If not, double check in

>Macintosh HD > System > Library > CoreServices > Install Command Line Developer tools

Unfortunately, you can't launch the install directly from that folder, but calling "make" in terminal should do the trick.
