# The perfect Commit

Making a perfect commit consists of two main aspects :
* Adding the right changes
* Compose a good commit message

## 1. Adding the right changes

This is nothing but using the **staging area** to the best way possible.

When making a commit, all the changes we are doing in a single commit must refer to the same topic (or) an unique idea. Never add all changes as bulk in a single commit.

This will help us to ensure a better structure and increases the understanding of whats happening for all the project contributors and even if something goes wrong in future, we can simply check the commits and make the neccessary changes and fixes and  get it back to working.

Let's understand how to add changes by taking an example :

let's say, we have three files : FileA, FileB, FileC

Case 1:
* changes in FileA and FileB combinedly refers to one topic and changes in FileC refers to other topic.
* In such case , commit changes of FileA, FileB together and changes of FileC in other commit.

Case 2:
* changes in FileA and some part of changes in FileB combinedly refers to one topic and changes in remaining part of FileB and changes in FileC combinedly refers to other topic.
* In such case , commit changes of FileA and part of FileB together and remaning part changes of FileB, FileC together in another commit.

Let's see how to do the first commit:

```
git add fileA
git add -p fileB    (Here, p stands for patch level)
```
This -p option allows us to select which chunks of code we want to add from the fileB.<br>
In the same way we can do the second commit too.

## 2. Compose a good commit message :
A complete commit message consists of two parts:

1. Subject :
 * concise summary about commit.
 * we often refer it explicitly as commit message.
2. Body (or) comment:
   It's a good description of changes happened and how they affect.

	Writing a commit message and its body using vscode:
    ```
    git config --global core.editor "code --wait"
    git commit
    ```
	Now it will open the vscode, there we can write the commit message.

    ![GIF](https://i.stack.imgur.com/pd4eq.gif)

	There has to be an empty line between the commit message and the commit body. Empty line helps vscode to seperately identify the body from the commit subject.

Pro-tip : Make extensive use of markdown in issues and prs or wherever possible in the github workflow.
