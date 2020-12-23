# Entry #5 - Installing BNFC

I remember having a bit of trouble when I went to first install BNFC onto my system. I think reinstalled it maybe eight times trying to get it to work. Hopefully this post will help you avoid the extra seven attempts :) 

First be sure to head over to the [BNFC homepage](http://bnfc.digitalgrammars.com/) and download whatever version is compatible with your system. This tutorial will be for a macOS. 

#### Easy installation with Homebrew
If you do not already have it, I would highly recommend installing Homebrew for your system. It will help you install the packages need that Mac systems do not usually come with.   

To install Homebrew, head to their page [here](https://brew.sh/) or open up your terminal and copy in the following: 

<pre><code> /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
</code></pre>

After this, you can use Homebrew to install BNFC by running the following once again in your terminal: 
<pre><code> brew install bnfc </code></pre>

You can then run `bnfc --version` to check whether it has successfully installed. 

#### Installing Cabal
Now we are going to want to install Cabal. More instructions can be found on their [homepage](https://www.haskell.org/cabal/). We will again use Homebrew to install Cabal since it is a bit easier this way. 

Run the following in your terminal:
<pre><code> brew install cabal </code></pre>
We can again verify the installation using the `cabal --version` command similar to what we did above with BNFC. 

#### Almost there...
There are only... **THREE** more things to install from here. These three include, ghcup, Alex, and Happy. Luckily we can do this all in one go by pasting the following in your terminal: 

<pre><code>curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh
cabal install alex 
cabal install happy </code></pre>
Perfect! Now that everything is installed, hopefully everything is working and you can go ahead and test BNFC following the steps at the webpage below. 

#### Testing BNFC
[These are the steps](https://hackmd.io/@alexhkurz/HJVtVl068#Generating-a-Parser-from-a-Context-Free-Grammar) I completed to ensure BNFC was working on my system. This page was written by the professor for the course I learned Haskell for. If you scroll down the page, you will find Assignment #1, which we will go over briefly in the next post! 