Instructions on how to get set-up
=================================
Getting up and going is pretty straight forward.  
  <code>
  mkdir -p ~/Library/Application\ Support/TextMate/Bundles  
  cd ~/Library/Application\ Support/TextMate/Bundles  
  git clone git://github.com/jpatzer/Rotor.tmbundle.git
  osascript -e 'tell app "TextMate" to reload bundles'  
  </code>
  
How to enable multiline comments
================================
The trick to getting this to work is to tell TextMate to recognize your comments preference. To do this, you'll have to open up your bundle editor (*Bundles > Bundle Editor > Show Bundle Editor*) and navigate to the Source bundle. Open it and find the comments preference. In the **Scope Selector** write source.rotor. 

Now you can do multiline comments with 'command + /' key combo (or any other that you'd like to define on your own).

At some point I may figure out a better way to do this (I'm probably missing something), but until then you'll have to go about things this way.

If you want to make changes to the bundle
=========================================
When you make changes to your Git-ified bundle in the Bundle Editor, you’ll need to Reload Bundles for the changes to show up in your repository. Then you’ll need to git add . and commit / push as you would a normal repository.