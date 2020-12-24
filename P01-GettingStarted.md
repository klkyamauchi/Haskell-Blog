# Entry #1: Getting Started - Installing Haskell

Before taking this course, I had never been asked to install a language via the command line. With the instructions that were given, it seemed like it would only take a few minutes- simple and easy. 

The first think I did was head over to the homepage of the Haskell Platform. From there I chose the option to install Haskell onto my macOS system by opening up terminal and pasting in the following line: 

<pre><code>curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh
</code></pre>

After following the prompts to download HLS, I chose to opt out of automatically adding the path to my bash shell as it seemed to be failing to do so when I chose the "YES" option. 

After the installation was complete I was prompted with the following message in my terminal: 

<pre><code>All done!

To start a simple repl, run:
  ghci

To start a new haskell project in the current directory, run:
  cabal init --interactive

To install other GHC versions, run:
  ghcup tui
</code></pre>

I was then able to launch the Haskell repl by typing, `ghci` 
into the terminal. Once this is done, you should see the following: 

<pre><code>GHCi, version 8.8.4: https://www.haskell.org/ghc/  :? for help
Prelude> 
</code></pre>

Once in the Haskell repl, you may test basic arithmetic functions like addition, subtraction, multiplication, etc. I did so below and it looked something like this: 

<pre><code>Prelude> 1+1
2
Prelude> 2+2
4
Prelude> 2-3
-1
Prelude> 4-2
2
Prelude> 4*4
16
Prelude> 2*3
6
Prelude> 4/2
2.0
Prelude> 2/2
1.0
Prelude> 
</code></pre>