# Kingdom-Death-Maximo-Kijan-Mod

Tabletop Simulator on Steam: 
http://store.steampowered.com/app/286160/

You can download and use the mod by subscribing to: 
https://steamcommunity.com/sharedfiles/filedetails/?id=1284555889

## Bug reports

Open bug reports here:
https://github.com/maximo1984/Kingdom-Death-Maximo-Kijan-Mod/issues

## Contributing to this project

Install Atom and use the TTS plugin: http://berserk-games.com/knowledgebase/atom-editor-plugin/

In Atom, go to File->Settings->Packages->Click on settings for tabletopsimulator-lua

Required: Set the "base path for files you wish to #include" to something "c:\git\kdm\scripts\\" which is the Git scripts folder

Recommended: Under Load/Saving, change the dropdown to "Do not automatically open any files sent from Tabletop Simulator".  This will stop Atom from automaticaly opening all the files as tabs which I find annoying.

In Atom, go to File->Settings->Packages->Click on settings for whitespace, and disable "Ensure Single Trailing Newline" option.

In Atom, go to File | Add Project Folder and choose  "c:\git\kdm\scripts\shared\" so its easy to view and edit the shared files.  

Read about #include feature here: http://blog.onelivesleft.com/2017/08/atom-tabletop-simulator-package.html 

Restart Atom

### To update TTS with a fix made in GitHub 

* In TTS, load the starting point save
* In Atom, get the scripts from TTS as normal
* In a command prompt

```
cd c:\git\kdm
git checkout master
git pull
CopyToTTS.cmd
```

* Back in Atom, Save & Play (Ctrl-Shift-S)

### To update GitHub with fix made in Atom

* In Atom, get the scripts from TTS as normal
* In Atom, edit the scripts as desired
* Fork and clone into this github repro if you haven't already
* In command prompt

```
cd c:\git\kdm
git checkout master
git pull
git checkout -b someBranchName
CopyFromTTS.cmd
git add .
git commit -m "Some description you like"
git push --set-upstream origin someBranchName
```

There's some other useful command tools you should know about:
```
git status
git gui
gitk
```

* Go to https://github.com/maximo1984/Kingdom-Death-Maximo-Kijan-Mod and you'll see a button to create a pull request button for the branch in your fork that you just pushed

If you have merge conflicts, do:

```
git pull
git merge origin/master
git mergetool HEAD .
and then fix your merge conflicts in your git merge tool.
git push
```

After you're done with the pull request, you should go back to master branch, so your ready to make other bug fixes
```
cd c:\git\kdm
git checkout master
git pull
```

