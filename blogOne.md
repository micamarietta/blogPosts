# Blog No. 1
## Installing Haskell on a Windows 10 Home Platform

In the start of our programming languages course, our first order of business was to download the Haskell programming language. Haskell was luckily both compatible with both the Windows and Linux operating systems, but there were several steps I needed to go through in order to install Haskell correctly on Windows.

Because it took several websites and several steps to successfully download the language for a Windows 10 Home Platform, I thought it would be helpful to write a sort of tutorial in this blog.

There are several websites and tutorials that go through the steps to install Haskell on Windows 10 Home, and each one seems to have different steps you should go through. I used the generic Haskell installation website for my successful install with the help of people on Stack Overflow to confirm that my install worked.

Here is the link to install for Windows: https://www.haskell.org/platform/windows.html

### Step 1
####First, you must configure "Chocolatey" on your computer. Link: https://chocolatey.org/install
Chocolatey is a software management solution on Windows, that helps you keep track of the packages you have and which version of that package you are on.

Although I have never directly interacted with Chocolatey on my computer when utilizing Haskell, it is an application you must have to complete the Haskell installation process for Windows.

The Chocolatey installation process is a simple one. Choose your installation mode, then paste the commands from the website into powershell.exe. It is imperative that you are using an administrative shell, which is reiterated on the Chocolatey website (run powershell as an administrator).

### Step 2
#### Clean the cabal configuration by running cabal user -config init -f
This step is highlighted on the Haskell installation website.

At first, I skipped this step because I hadn't had prior versions of the Haskell platform on my computer. However, with this I was UNABLE to successfully download Haskell, and the installation process in my command prompt paused and would not finish.

It took me a few tries to fully download Haskell on my Windows 10 Home platform, so this step is very helpful in ensuring the installation process will be successful (even if you don't take multiple tries to install the language).

### Step 3
#### Run "choco install haskell-dev refreshnv"

After typing this command in your command prompt, the Haskell language will take some time to install. It will show the loading progress the entire time in the terminal.

Once the installation is finished, type "ghci" (the name of the executable of the GHC compiler) in command prompt. Some websites said to type WinGHCi for a Windows operating system, but I found that typing ghci worked.  

If Haskell was successfully installed, this will appear in command prompt:

//
$ ghci
    GHCi, version 6.12.3: http://www.haskell.org/ghc/  :? for help
    Loading package base ... linking ... done.
    Prelude>
//

The prelude indicates that the Haskell system is waiting for your input.

If this does NOT appear after you type ghci, that means that Haskell was not successfully installed (or at least in my case it wasn't). This occurred a few times for me, and to fix it, I just found the file location where I had some Haskell files downloaded, deleted them/uninstalled them, and started over, making sure to complete the second step of the Haskell installation process.

If you want further tests to ensure your Haskell system is working properly, the website tryhaskell.org is helpful because it lets you type in Haskell commands with correct Haskell output. Here is the link: http://tryhaskell.org/

Hope this was helpful!
