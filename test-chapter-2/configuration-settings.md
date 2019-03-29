# Git configuration settings

## General configuration

For git to be able to speak with the Bitbucket repos and to pass internal web policies you would need to setup the user name and email to match your work id for git to work correctly on your machine.

## Global Settings

Setting up the user name and email id

1. Open a bash command prompt

![Select the Git Bash command prompt](../.gitbook/assets/image%20%2815%29.png)

2. The bash prompt looks like this

![Git bash prompt](../.gitbook/assets/image%20%2832%29.png)

3. Type the following commands

```text
git config --global user.name "firstname_lastname"
git config --global user.email firstname.Lastname@db.com
```

{% hint style="info" %}
Notice that the email does not have quotes around it.
{% endhint %}

## Other Global settings

Usually when working with git the default editor is  vim. This is important when we write commit messages for committing our work into the repository as git explicitly asks for entering some text whenever you commit some code. Though vim is quite a powerful editor it is not in everyones interest to understand how it works.

![Here is my git configuration run with command &quot;vim ~/.gitconfig&quot; or &quot;git config --global --edit&quot; in bash shell](../.gitbook/assets/image%20%283%29.png)

If not comfortable with vim then best solution is to use an editor which you personally prefer. To change these editor settings please follow the following steps.

Enter the following command if you prefer using the application Notepad++ \(another powerful editor which can be installed from the Automated Software Distribution webpage\)

```text
git config --global core.editor "'C:/Program Files (x86)/Notepad++/notepad++.exe' -multiInst -nottabba
r -nosession -noPlugin"
```

The config file will now have the editor set to notepad++ to open

![Editor settings now changed from vim to Notepad++](../.gitbook/assets/image%20%2825%29.png)

The editor which opens when committing code will now default to Notepad++

![Notepad++ editor to write your commits](../.gitbook/assets/image%20%2827%29.png)

If you prefer to use the simpler windows notepad instead set the editor to

```text
git config --global core.editor "notepad.exe"
```

If you want to default back to vim then just remove the line editor=\*\*\*\*\* from the .gitconfig file. In the future chapters I will show the commit messages written in the vim editor as it is my editor of choice but of course it is completely reproducible in your editor of choice too.

2. Getting rid of control line feed issues. When writing content in a file saved on a windows machine, the file tends to add two characters at the end of every line i.e. a carriage return \(cr\) and a line feed \(lf\). This goes way back to the old days of the typewriter where one had to physically move the carriage from left to right to be able to start at the beginning of the line and at the same time move one step down. This physical act carried out both commands i.e. carriage return and fed a new line. Unix on the other hand implied both with one command i.e. the line feed. The familiar "\n" string is what is used in computer parlance these days. 

1. **Checkout Windows-style, commit Unix-style \(recommended setting\)**

   Git will convert LF to CRLF when checking out text files. When committing text files, CRLF will be converted to LF. For cross-platform projects, this is the recommended setting on Windows \("core.autocrlf" is set to "true"\)

2. **Checkout as-is, commit Unix-style**

   Git will not perform any conversion when checking out text files. When committing text files, CRLF will be converted to LF. For cross-platform projects this is the recommended setting on Unix \("core.autocrlf" is set to "input"\).

3. **Checkout as-is, commit as-is**

   Git will not perform any conversions when checking out or committing text files. Choosing this option is not recommended for cross-platform projects \("core.autocrlf" is set to "false"\)

```text
git config --global core.autocrlf true
```



